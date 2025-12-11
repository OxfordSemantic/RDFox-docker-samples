# Basic Compose sample

A basic sample for deploying RDFox using a Compose template. Includes:
1. `rdfox-init` - This container initializes an RDFox server directory. It runs with standard system configuration.
2. `rdfox` - The main RDFox container meant to serve user requests. Can run with limited system permissions ("capabilities") for enhanced security - see "cap_drop" in `compose.yaml`.

## Starting the deployment
1. Install and start either Docker engine or an alternative like Podman.
2. Install `docker-compose`.
3. Copy your `RDFox.lic` file into this directory.
4. Run `docker-compose up`.

## Stopping the deployment
1. Run `docker-compose down`
2. If you would like to delete the persisted data, clear the `server-directory` folder.

## Interacting with RDFox
When your deployment is running, you can interact with RDFox via the exposed 12110 port:
1. In browser, go to http://localhost:12110/console
2. Call the REST API (see: https://docs.oxfordsemantic.tech/apis.html#basics-of-the-restful-api)
3. Use RDFox's "remote shell" mode for a CLI experience (see: https://docs.oxfordsemantic.tech/rdfox-executable.html#remote)
