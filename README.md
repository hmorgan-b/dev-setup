# Local Development Environment Setup

Install or setup the following elements for complete local development environment. 

1. [Editors](#editors)
2. [Git/Github](#git-github)
3. [Cloud Resources](#cloud)
4. [Docker](#docker)


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
Lists all docker processes 
