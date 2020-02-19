---
id: home
title: Quick Start
sidebar_label: Quick Start
---

## Launching the development server

1. Install dependencies

    ```bash
    $ yarn install
    ```

2. Copy the environment variables to `.env`

   ```env
   PORT=8080
   DEVELOPMENT_MODE=true
   ```

3. Launch the development server

   ```bash
   $ yarn dev
   ```

## Deploying for production

### Docker deployment

To launch a complete cluster (with a postgres database)

1. Launch the `docker-compose` cluster

   ```bash
   $ yarn docker:start
   ```

To launch just the server

1. Build the Docker image

   ```bash
   $ docker build . -t convenio:latest
   ```

2. Start the container

   ```bash
   $ docker start -p 8080:8080
   ```

### Building from source and launching

1. Install dependencies

    ```bash
    $ yarn install
    ```

2. Copy the environment variables to `.env`

   ```env
   PORT=8080
   DEVELOPMENT_MODE=true
   ```

3. Build the project

   ```bash
   $ yarn build
   ```

4. Serve the build files

   ```bash
   yarn serve
   ```