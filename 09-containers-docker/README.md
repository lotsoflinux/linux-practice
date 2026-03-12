# Chapter 9 — Containers & Docker

This chapter introduces Docker and how to run containers for reproducible environments.

## ✅ Exercises
- List images: `docker images`
- List running containers: `docker ps`
- Run a container:
  ```bash
  docker run --rm -it -v $(pwd):/workspace -w /workspace ubuntu:24.04 bash
  ```
- Build an image from a Dockerfile (if you create one): `docker build -t myimage .`

## 📋 Example commands
```bash
cd /workspace/09-containers-docker
docker run --rm -it -v $(pwd):/workspace -w /workspace ubuntu:24.04 bash
``` 

## 📝 Files in this folder
- `docker-compose.yml` — example compose file (no real services).

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/09-containers-docker
docker-compose config
```