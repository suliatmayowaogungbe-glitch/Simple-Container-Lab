## Simple-Container-Lab
This project demonstrates a complete Docker containerization workflow, from writing a simple Node.js application to building an image, running it as a container, and pushing the project to GitHub.

## Overview
This repository was created as a hands-on lab to practice and understand the fundamentals of containerization with Docker. The project simulates how developers package an application into a portable, isolated environment that runs consistently regardless of the host machine. The objective was not to build a complex application but to gain practical experience with the Docker build-run-ship workflow.

## Project Purpose
This lab covers: writing a simple application, creating a Dockerfile, building a Docker image, running a container from that image, initializing a Git repository, and pushing the project to GitHub.

## What Was Accomplished
- **Project Setup** — A local working directory (`container-lab`) was created to hold the application and its Docker configuration.
- **Application Creation** — A simple Node.js script (`app.js`) was written that logs a message to the console, serving as the "application" to be containerized.
- **Dockerfile Creation** — A `Dockerfile` was added, based on the lightweight `node:18-alpine` image. It copies the application code into the image and defines the command to run it.
- **Image Build** — The Docker image was built and tagged using `docker build -t simple-container-lab:1.0 .`, producing a self-contained image with the app and its runtime bundled together.
- **Container Run** — A container was launched using `docker run --rm simple-container-lab:1.0`. It printed the expected output, confirming the image worked. The `--rm` flag ensured the container was removed automatically after finishing.
- **Git Initialization** — A local Git repository was initialized in the project folder to begin tracking version history.
- **Initial Commit** — All project files (`app.js` and `Dockerfile`) were staged and committed using `git commit -m 'feat: first container'`.
- **Remote Repository Connection** — The local repository was connected to a remote GitHub repository using `git remote add origin`.
- **Push to GitHub** — The default branch was renamed to `main`, and the project was pushed to GitHub using `git push -u origin main`.

## Prerequisites

- Docker Desktop installed and running
- Git installed and configured
- Node.js base image pulled automatically via Docker (`node:18-alpine`)
- Terminal access
- Visual Studio Code

## Skills Practiced

- Writing a minimal containerized application
- Dockerfile fundamentals (`FROM`, `COPY`, `CMD`)
- Building Docker images with tags
- Running and cleaning up containers
- Git fundamentals (init, add, commit)
- Remote repository management
- Conventional commit messages
- Pushing to GitHub via origin
## Note

This lab focused on the core Docker workflow: writing an app, containerizing it, and verifying it runs identically regardless of the host environment.

## License

MIT
