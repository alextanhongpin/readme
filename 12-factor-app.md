## Better documentation for repository

Some thoughts on the do's and dont's.

The dont's:
- the installation for the language. If the repo is meant for golang, it already assumes that the user has golang installed on the development machine


For the dos', let's take some inspiration from the [twelve-factor-app](https://12factor.net/):
- codebase: N/A
- dependencies: include dependency (package management version/commands etc, how to install/rebuild)
- config: the environment variables required, and where to find/generate them. Should provide a good default too
- backing services: external resources/links such as database, cloud platforms, where to find them/setup/cli tools etc
- build, release, run: proper steps/pipeline to rebuild the application and deploying/running them. Also how to test them in different environment/to know if it's working as expected (through test cases)
- processes: how to run the application/external dependencies as isolated process (use docker)
- port binding: N/A
- concurrency: N/A
- disposability: how to start/stop/cleanup application state, also how to terminate the instance. try to design a lifecycle for it.
- dev/prod parity: again, docker
- logs: logging best practices/naming/tracing through resource id etc
- run admin/management tasks as one-off processes: database migration tools, terminal commands, scripts, makefile etc.

And some others:
- application versioning
