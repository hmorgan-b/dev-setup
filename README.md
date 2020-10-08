# Local Development Environment Setup

Install or setup the following elements for complete local development environment. 

1. [Editors](#editors)
2. [Git/Github](#git-github)
3. [Cloud Resources](#cloud-stuff)
4. [Docker](#docker)
5. [Local Instances of Applications/Tools for Testing](#local-instances)
6. [Python Development](#python-devt)

<a name="editors"></a>
## Editors
**vim**
- Comes pre-installed on mac, just need to customize to your liking 
- See .vimrc file for configuration settings for some settings that do not come as standard vim is initialized
- Access this file in a terminal by `vi ~/.vimrc` 
- Google additional vim settings to further customize

**VS Code**
- Makes programming easier at times because of ease of seeing file/folder tree in the left margin 
- Has a lot of extensions/plugins to help customize experience and provides more tools for development
- Has ability to performs linting and debugging, also has spellcheck and other features to alleviate stupid mistakes 

<a name="git-github"></a>
## Git/Github
- Create a Github account for business use, sign in 
- Upload SSH public key to allow SSH terminal access
- See Confluence pages for version control workflow, including branch naming protocols, pull requests, and code review process

<a name="cloud-stuff"></a>
## Cloud Stuff
D&A uses the following cloud-based tools:
- Azure: blob storage, virtual machines, other resources
- Postgres/Citus: cloud storage database used by applications (dev, stage, and prod instances)

<a name="docker"></a>
## Docker
Download docker for mac for containerization of applications and resources needed to run applications. A Docker image serves as a blueprint for creating containers that will host a certain application or service.
Once downloaded, the following commands can be used:

`docker ps -a`

- Lists all docker processes 

`docker images`

- Lists the most recently created docker repositories containing images (created from Dockerfiles or downloaded)

`docker build --tag [image-name] [docker-file-location]`

- Builds the image as specified in the instructions in the Dockerfile

`docker run [image-name] -p 8080:80 --name [hello] -d`

- Creates and runs a Docker container derived from image (image-name)
- Maps local port 8080 to port 80 of container, to expose the container to the outside world and allow access from a browser. In this case, navigate in a browser to localhost:8080 to see application running
- The -d tag tells the container to run as a process in the backgound 

`docker-compose up`

- Used when you want to run a combination of applications, databases, etc. in coordination with each other in separate containers
- This command "composes" all of the Docker containers together
- Looks at the current directory, prepends the name of the current directory to the Dockerfile image name (as specified in docker-compose.yml, or similar)
- Builds images and runs containers all in one command

<a name="local-instances"></a>
## Local Instances of Applications/Tools Used for Testing
### RabbitMQ
RabbitMQ is an open-source messaging service. It accepts, stores, and forwards binary blobs of data (messages).
- Set up via the [rabbitmq docker image](https://hub.docker.com/_/rabbitmq)
- Also need to setup the management plugin, which is just a browswer-based UI to manage Rabbitmq notes and clusters

### Postgres
- Set up via the [postgres docker image](https://hub.docker.com/_/postgres)

### SonarQube
- Set up via the [sonarqube docker image](https://hub.docker.com/_/sonarqube)

<a name="python-dev"></a>
## Python Development


