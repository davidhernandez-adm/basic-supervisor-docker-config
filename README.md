# 🧩 Docker + Supervisor: Basic Service Management

A minimal Docker configuration demonstrating how to use **Supervisor** as a process control system within a container. This project manages an **nginx** service using Supervisor, making it ideal for multi-process Docker environments or advanced container setups.

---

## 📌 Project Overview

* **Name**: basic-supervisor-docker-config
* **Stack**: Docker, Supervisor, NGINX
* **Goal**: Launch an NGINX service inside a container using Supervisor to manage its lifecycle
* **Use Case**: Multi-service Docker containers where Supervisor is needed to control processes cleanly

---

## 📁 Project Structure

```
├── Dockerfile                  # Defines the base image, installs Supervisor and nginx
├── supervisor_services.conf    # Supervisor configuration to run nginx in the foreground
```

---

## 🚀 Getting Started

### Prerequisites

* [Docker](https://www.docker.com/products/docker-desktop)

### Installation Steps

```bash
# 1. Clone the repository
git clone https://github.com/davidhernandez-adm/basic-supervisor-docker-config.git
cd basic-supervisor-docker-config

# 2. Build the Docker image
docker build -t nginx-supervisor .

# 3. Run the container
docker run -p 8080:80 nginx-supervisor

# 4. Visit in browser
open http://localhost:8080
```

---

## 📦 Technologies Used

* **Docker** – Container runtime
* **Supervisor** – Process manager inside container
* **NGINX** – Web server running under Supervisor

---

## 🧪 Testing and Coverage

> Manual check: After running, visit `http://localhost:8080` and confirm NGINX welcome page is served.

Optional: Inspect logs using `docker logs <container-id>`

---

## 🧠 Key Challenges & Learnings

* Understood why Supervisor is needed for multiple services or foreground management
* Practiced integrating process control into minimal Docker setups
* Ensured proper config syntax (`autostart`, `autorestart`, etc.) for service stability

---

## 📷 Screenshots or Live Demo

> No UI — Service available at: [http://localhost:8080](http://localhost:8080)

---

## 📜 License

[MIT](https://opensource.org/licenses/MIT)

---

> Created by [David Hernández](https://github.com/davidhernandez-adm) for Docker-based service orchestration practice using Supervisor.
