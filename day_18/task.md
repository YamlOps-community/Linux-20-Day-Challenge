## Day 18: Final Project

### Tasks:

__Videos:__
- [Building containers from scratch](https://www.youtube.com/watch?v=GFUpXhft8zA)
- [Containers from scratch](https://www.youtube.com/watch?v=8fi7uSYlOdc)

__Reading:__  
- BLOG: [Building your container from sctach](https://medium.com/@nowonlywork/building-your-container-from-scratch-on-ubuntu-a-deep-dive-a73eb76f4125)
- BLOG: [Building an Application Isolation Environment on Linux](https://medium.com/@foluwadaniel_8570/building-an-application-isolation-environment-on-linux-without-docker-7d88dd1c8404)

__Activity:__
- Complete this project
_NB: Please use the resources as refrence materials_

__🐧 Project Title: Run a FastAPI App within Minimal Linux Container Runtime__

__📄 Description__

This project demonstrates how to build a __lightweight container-like system__ that runs a Python __FastAPI__ application in an isolated and secure environment using only __Linux primitives__ and a __Bash script__ as the orchestrator.

You’ll gain hands-on experience with the core technologies that power containers by using:

- __Filesystem isolation__ via `chroot`
- __Process and namespace isolation__ using `unshare`
- __Resource limitation__ via `cgroups`

The FastAPI application will run inside this minimal container, showcasing how containers work under the hood.

---

__✅ Project Requirements__

__🗂️ Filesystem Isolation__
- Use `chroot` to create an isolated root filesystem for the container.

__🧠 Process & Namespace Isolation__
- Use Linux namespaces (`unshare` or equivalent) to isolate:
  - Process ID namespace
  - Mount namespace
  - Network (optional)
  - UTS and IPC

__⚙️ Resource Limitation__
- Use `cgroups` to limit:
  - CPU usage
  - Memory usage

__🖥️ Bash Wrapper Script__
A Bash script that:
- Sets up the isolated environment
- Launches the FastAPI app inside the container
- Handles cleanup automatically after exit
- Includes clear comments and error handling

__🚀 FastAPI Application__
- A minimal Python FastAPI app that:
  - Exposes a simple health check route at `/health`
  - Returns a JSON response


### Deliverables:
- Submit link to the project repo, demo video or script

__1. Bash Script__
- Automates the full lifecycle: __setup__, __run__, and __teardown__
- Includes detailed comments and basic error handling

__2. FastAPI App__
- A Python script/app ready to run inside the container
- Responds to HTTP requests (e.g., `GET /health → {"status": "ok"}`)

__3. Root Filesystem__
- Instructions to build or set up the root filesystem using:
  - `debootstrap`, or
  - Manual copying of required binaries, libs, and dependencies

__4. Documentation__
- Overview of how it works
- System requirements:
  - Recommended Linux distro (e.g., Ubuntu)
  - Bash version
  - `cgroups` version
- Step-by-step guide to run the full setup

**Suggested Blog Post structure:**

1. Intro: What is containerization?
2. What tools did I use (chroot, namespaces, unshare)?
3. Step-by-step walkthrough (commands & explanations)
4. What I achieved (screenshot of `httpd` running)
5. What Docker automates beyond this manual process

__5. Demo & Testing Instructions__
- How to run the setup
- How to send HTTP requests to test the FastAPI app (e.g., with `curl` or a browser)