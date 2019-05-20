# Hackstofan

### Install the Hugo cli via snap
`snap install hugo --channel=extended`

#### Docker

It is also possible to use Docker and Docker compose (see start server)

### Clone repository including submodules
`git clone --recursive git@github.com:hackstofan/hackstofan.git`

### Start server with drafts enabled
`hugo server -D`

### Start server with Docker compose

If you don't want to install hugo on your machine, you can use the
included docker-compose.yml file to run a hugo docker container:

    docker-compose up
