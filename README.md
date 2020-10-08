# Local Development Environment Setup

Install or setup the following elements for complete local development environment. 

1. [Editors](#editors)
2. [Git/Github](#git-github)
3. [Cloud Resources](#cloud-stuff)
4. [Docker](#docker)
5. [Local Instances of Applications/Tools for Testing](#local-instances)
6. [Python Development](#python-development)


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

## Cloud Stuff
D&A uses the following cloud-based tools:
- Azure: blob storage, virtual machines, other resources
- Postgres/Citus: cloud storage database used by applications (dev, stage, and prod instances)

## Docker
Download docker for mac for containeriation of applications and resources needed to run applications.
Once downloaded, the following commands can be used:

`docker ps -a`

- Lists all docker processes 

`docker images`

- Lists the most recently created docker images (created from Dockerfiles or downloaded)

`docker build --tag [image-name] [docker-file-location]`

- Builds the image as specified in the instructions in the Dockerfile

`docker run [image-name] -p 8080:80 --name [hello] -d`

- Runs a Docker container derived from image (image-name)
- Maps local port 8080 to port 80 of container, to expose the container to the outside world and allow access from a browser. In this case, navigate in a browser to localhost:8080 to see application running
- The -d tag tells the container to run as a process in the backgound 

`docker-compose up`

- Used when you want to run a combination of applications, databases, etc. in coordination with each other in separate containers
- This command "composes" all of the Docker containers together
- Looks at the current directory, prepends the name of the current directory to the Dockerfile image name (as specified in docker-compose.yml, or similar)
- Builds images and runs containers all in one command

## Local Instances of Applications/Tools Used for Testing
### RabbitMQ
RabbitMQ is an open-source messaging service. It accepts, stores, and forwards binary blobs of data (messages).
- Set up via the [rabbitmq docker image](https://hub.docker.com/_/rabbitmq)
- Also need to setup the management plugin, which is just a browswer-based UI to manage Rabbitmq notes and clusters

### Postgres
- Set up via the [postgres docker image](https://hub.docker.com/_/postgres)

### SonarQube
- Set up via the [sonarqube docker image](https://hub.docker.com/_/sonarqube)

## Python Development


