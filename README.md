# readme

This repo provides a guide on how to write better README for developers.

- what do users seek when they come to the readme page? 
  - how to start the project immediately?
  - how to deploy?
  - how to run the tests?
  - source of documentation?

## Documentation 
There are several breakdown of documentation:

- Technical
- Non-technical
- UseCases/requirements (<- where should this belong?)
- Features
- API
- Microservie (e.g. where to deploy, where is the server hosted, the service url, who's connected to it)
- Static site (the domain where the static page is hosted)
- Deployment documentation
- Package/module/library usage
- CLI


Technical (note this is for a server, not package setup)
- Language/framework choice
- Language/framework version
- Architecture concept (web server, cron etc), which component does this belong to in a larger picture.
- How to install
- How to setup dependencies (database, message queue, how to install)
- Install external dependencies (language etc)
- Setup on different os
- How to run (usage guide)
- Environment variables
- Configuration basic/default (environment variables)
- Deployments
- Dockerizing
- Infrastructure as code, where to deploy, how to deploy, how to configure locally
- Domain name, endpoint
- Version
- Contributors

E.g.


## repo-name

A brief description of what (capability) and why (purpose) this repo exists. 

## Architecture

A sample image to show where this repo belongs to in a part of a larger system. For example, this repo may be the server component of a larger system, and it could be powering a client on a separate repo.

## Configuration

Describes the required/optional environment variables. We can use the convention `.env` (instead of `.env.sample`, this can be our base), and `.env.production`, `.env.testing`, `.env.staging`, `.env.development` will override the base based on the current environment. `config` and `secret` are not the same.

```
HOST=localhost
PORT=8080
ENV=development (default)
```

## Language

The language used for the repository, and the current version used. The version is important, especially if older versions are being used.

```bash
$ command to check the version
```

## Installation

Installation may consist of:
- internal dependency - this should be managed by a package manager, and the version of each dependency should be locked.
- external dependency - this could be tools for database migrations, language specific dependency, vendor, third party APIs.


## Start
Steps to start the local server.
```bash
$ make start
```

If there are additional infrastructure, write down the steps to start them too. This applies for different environment too (production, staging, testing etc). For e.g. we can run the database locally, as well as connecting to a hosted database, which requires different setup.

## Stop

How to stop, as well as clean temporary files that are created.

## Deployment

Should this be part of the README? If there are `commonly repeating components` such as database and so on, we can reference them to another external knowledge base (Notion, Confluence) if the setup is the same. This will keep the README DRY, as well as allow developers that already know the setup to just focus on the main thing. This applies for `installation`, `configuration`, `dockerizing`, `docs`, etc.
### Deployment badges


## Dockerizing

All projects should have a docker image build by now. But we need additional steps now to describe the build, how to start the docker, and what is required.

## Versioning

How to version the application, the strategy etc.





