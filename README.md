# Node.js LTS Agent for Teamcity

A Docker image to run a [TeamCity](https://www.jetbrains.com/teamcity/) agent with latest Node.js LTS (version 12.x) capabilities.
The image is based on the official [teamcity-minimal-agent](https://hub.docker.com/r/jetbrains/teamcity-minimal-agent/) and just adds a Node.js installation on top of it.

## Building the image

Simply run `docker build -t teamcity-node-lts-agent .`

## Running the agent

Since the image is based on the teamcity-minimal-agent, all required parameters of the base image are also required here.
You can run the image that you have already built, or pull the image from [Docker Hub](https://hub.docker.com/r/hmnd/teamcity-node-lts-agent/)

Docker Hub example:

`docker run hmnd/teamcity-node-lts-agent:latest -it -e SERVER_URL="<url to TeamCity server>" -v <path to agent config folder>:/data/teamcity_agent/conf`

## License

MIT License
