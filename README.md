## Setup Instructions

### Prerequisites:
- Running a [server with the following installed](https://marketplace.digitalocean.com/apps/docker):
  - git
  - [docker (>= 20.0)](https://www.simplilearn.com/tutorials/docker-tutorial/how-to-install-docker-on-ubuntu)
  - [docker compose (>= 2.0.0)](https://docs.docker.com/compose/install/linux/#install-the-plugin-manually)
- ETH wallet (private key) with:
  - ETH balance (for signing transactions)
  - SARCO balance (for bonding your archaeologist to curses)
- RPC URL (Infura, Alchemy, etc.)

_If running on Goerli (chain id = 5), then you will need Goerli ETH + Goerli SARCO._

---

### Initial Setup Instructions

1. Clone this repo:

   `git clone https://github.com/sarcophagus-org/quickstart-archaeologist`


2. Copy example env file, and fill out the env file values.

   `cp .env.example .env`

3. Create blank peer ID file.

   `touch peer-id.json`

4. **If you have not yet registered your archaeologist:**
   > `COMPOSE_PROFILES=register docker compose run -rm register`  
   
_(or `docker-compose` for older versions of docker compose)_

5. Run the service
   >  `COMPOSE_PROFILES=service docker compose up`

### Registering your archaeologist
If this is your first time running the service, you will be prompted to register your archaeologist.

Follow the prompts to register your archaeologist.

### CLI
To run the CLI: 
1. If the service is not started, start the service with `docker compose up`,
2. Jump into the container with: `docker compose exec archaeologist sh`
3. Run `cli help` for available commands, or `cli help <command>` for help with a given command.

### Further instructions
To update the service to the latest version:
`docker-compose pull`
