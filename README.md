# docker-cheatsheet-
A simple and complete Docker command reference guide for beginners and DevOps learners.

---

# 🐳 Docker Cheat Sheet

### 📌 Overview

Quick reference for daily Docker commands: building images, running containers, pushing/pulling, inspecting, and cleaning up.

---

## 🚀 Getting Started

**Install & Check Version**

* `sudo apt install docker.io` → Install Docker on Ubuntu
* `docker --version` → Check Docker CLI + daemon version

---

## 🧱 Building & Tagging Images

* `docker build -t username/image:tag .` → Build and tag image
* `docker build --no-cache -t name .` → Build fresh without cache
* `docker tag source_image username/image:tag` → Rename or re-tag existing image

📝 **Note:**

* Always use lowercase for image names even if your Docker Hub username has uppercase letters
* If no tag is given, Docker uses `:latest` automatically

---

## 📦 Managing Images

* `docker images` → List all images
* `docker rmi image_name` → Remove an image
* `docker image prune` → Remove dangling (unused) images
* `docker image prune -a` → Remove all unused images

---

## 🔄 Pushing & Pulling Images

* `docker login` → Login to Docker registry
* `docker push username/image:tag` → Upload image to Docker Hub
* `docker pull username/image:tag` → Download image from Docker Hub
* `docker search image_name` → Search for images on Docker Hub

---

## 🧩 Running Containers

* `docker run image` → Run a container in foreground
* `docker run -d image` → Run in background (detached)
* `docker run -it --name name image sh` → Run interactively with terminal
* `docker run -p host:container image` → Map ports (host to container)
* `docker run -v /path:/path image` → Mount volume from host

---

## 🔍 Container Management

* `docker ps` → Show running containers
* `docker ps -a` → Show all containers (running + stopped)
* `docker start container` → Start a stopped container
* `docker stop container` → Stop a running container
* `docker restart container` → Restart container
* `docker kill container` → Force stop (kill)
* `docker attach container` → Attach to running container
* `docker exec -it container bash` → Execute command inside container
* `docker logs container` → View container logs
* `docker inspect container` → Detailed container info in JSON
* `docker stats` → Real-time usage of containers
* `docker port container` → View port mappings
* `docker diff container` → See changes inside container

---

## 🧹 Cleanup & System Info

* `docker system info` → Docker daemon info
* `docker system df` → Docker disk usage summary
* `docker system prune` → Remove unused containers/images/networks
* `docker system prune -a` → Remove everything not currently used
* `docker container prune` → Remove stopped containers
* `docker network prune` → Remove unused networks
* `docker volume prune` → Remove unused volumes

---

## ⚙️ Optional Advanced Commands

* `docker cp container:/path/to/file ./file` → Copy file from container to host (or vice versa)
* `docker commit container new_image_name` → Create image from running container state
* `docker save -o image.tar image_name` → Save image as a `.tar` archive
* `docker load -i image.tar` → Load image from `.tar` file
* `docker network ls` / `create` / `inspect` → Manage container networks
* `docker volume ls` / `create` / `inspect` → Manage persistent volumes

---

## 🧱 Docker Compose (for multi-container apps)

**Used only when you have a `docker-compose.yml` file**

* `docker-compose up` → Start all services
* `docker-compose up -d` → Start in background
* `docker-compose down` → Stop and remove containers
* `docker-compose build` → Build all services
* `docker-compose logs` → View service logs

---

## 📚 Bonus Tips

* Use lowercase for all image names (Docker Hub is case-sensitive)
* Use tags like `v1`, `prod`, `latest` for better image versioning
* Regularly run `docker system prune` to free up disk space
* Use `docker inspect` to debug container issues
* Use `docker-compose` for easier handling of multiple containers

---

