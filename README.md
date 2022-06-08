# NCKH_Programming Forum

---

### REQUIREMENTS

-   [Node 16.15.1](https://nodejs.org/en/download/)
-   [Docker](https://docs.docker.com/desktop/)
-   [Hasura GraphQL Engine 2.0](https://hasura.io/docs/latest/graphql/core/hasura-cli/install-hasura-cli/#install)
-   [Golang 1.15+](https://go.dev/dl/)

### How to run

###### 1. CodeWar_FE

-   Install Dependencies
    ```bash
    yarn install
    ```
-   Build the project
    ```bash
    yarn start
    ```

###### 2. CodeWar_BE

Database design and migration

Use Hasura 2.0 CLI: https://docs.hasura.io/1.0/graphql/manual/hasura-cli/install-hasura-cli.html#install

```sh
# rename the CLI to hasura2 to avoid conflict if using Hasura v1 in parallel
sudo wget https://github.com/hasura/graphql-engine/releases/download/v2.0.9/cli-hasura-linux-amd64 -O /usr/local/bin/hasura
sudo chmod +x /usr/local/bin/hasura
```

-   Change directory
    ```bash
    cd CodeWar_BE/services/controller
    ```
-   And then migrate:

```
hasura migrate apply
hasura metadata apply
hasura seed apply
```

-   Design

```
hasura console
```
