felixroden/homelab-documentation

## Setting Up the Wiki

This repository contains a `docker-compose.yml` file for setting up the wiki using [Material for MkDocs](https://github.com/squidfunk/mkdocs-material) and [Caddy](https://github.com/caddyserver/caddy) for reverse proxy. Follow the instructions below to get started without the reverse proxy.

### Prerequisites
- Docker
- Docker Compose

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/felixroden/homelab-documentation.git
   cd homelab-documentation
   ```

2. Set up the `.env` file with your environment variables:
   ```sh
   touch .env
   # Add your environment variables here, for example:
   # MKDOCS_PORT=8000
   # PWD=/home/<USER>/docker/mkdocs
   ```
### Running without Caddy Reverse Proxy

If you prefer not to use Caddy, you can expose the MkDocs container port directly.

1. Uncomment the ports section in the `docker-compose.yaml` file:
  ```yaml
   ports:
     - "8000:8000"
   ```

2. Start the MkDocs container:
   ```sh
   docker-compose up -d
   ```

3. Access the wiki:
   Open your web browser and go to `http://localhost:8000`.

## Contributing

Contributions are welcome! If you have insights, corrections, or additions, please submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## Todo
- [ ]  Documentation for running with Caddy Reverse Proxy
