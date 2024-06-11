# Home Lab Documentation

Welcome to my Home Lab Documentation site! This is the hub where I chronicle the journey of setting up, configuring, and optimizing my home lab. Here, you'll find detailed records of my lab environment, including hardware configurations, software installations, network setups, and troubleshooting steps. My goal is to create a comprehensive resource that not only aids my own learning and future reference but also serves as a guide and inspiration for anyone interested in building their own home lab.

## Purpose of This Site

### Learning and Experimentation
Documenting my home lab setup helps me solidify my understanding of various technologies and systems. By writing down each step, I ensure that I grasp the concepts and methodologies involved.

### Troubleshooting and Reference
Issues are bound to arise. This site acts as a repository of solutions, configurations, and best practices, making it easier to troubleshoot problems and recreate setups when needed.

### Sharing Knowledge
Knowledge grows when shared. By making my documentation public, I hope to provide valuable insights and practical guides for others who are embarking on similar home lab adventures.

## What You'll Find Here

- **Hardware Configurations**: Detailed descriptions of the hardware components in my lab, including servers, networking equipment, storage solutions, and peripherals.
- **Software Installations**: Step-by-step guides on installing and configuring various software, from operating systems to specialized applications and services.
- **Network Setups**: Diagrams and explanations of my network architecture, including VLANs, firewalls, VPNs, and other networking essentials.
- **Projects and Use Cases**: Documentation of specific projects, experiments, and use cases that I have implemented in my lab.
- **Troubleshooting Logs**: Records of issues encountered, solutions found, and lessons learned along the way.

## Join the Journey
This site is a work in progress, constantly evolving as I continue to learn and expand my home lab. I encourage you to explore, experiment, and even contribute your own insights. Feel free to reach out with questions, suggestions, or just to share your own home lab stories. Let's build and learn together!

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

1. Uncomment the ports section in the `docker-compose.yml` file:
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
