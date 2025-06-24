## 🚀 DevOps Internship Assignment – Nginx Reverse Proxy + Docker Compose

## 👋 About

This project demonstrates a multi-container setup using **Docker Compose**. It includes:

- 🟢 A **Go (Golang)** backend service (`service1`)  
- 🐍 A **Python Flask** backend service (`service2`)  
- 🌐 An **Nginx** container acting as a **reverse proxy**

All services run under a single port via **Nginx path-based routing**.




---

### 🔧 Setup Instructions
Clone the repository:


```bash
git clone https://github.com/sahni1/devops-Intern-assignment.git
cd devops-Intern-assignment
```
Run the complete system:
```bash
docker-compose up --build
```
To stop the system:
```bash
docker-compose down
```
## 🌐 How Routing Works
Nginx handles the following reverse proxy rules:

http://localhost:8080/service1 → Routes to Go app on service1:8001

http://localhost:8080/service2 → Routes to Flask app on service2:8002

🔍 Logging: All incoming requests are logged with timestamp and path in Nginx logs.

---

🎁 Bonus Implemented
  -  Health checks for both services using /ping endpoint
  -  Nginx logs every request (timestamp + path)
  -  Modular setup with 3 separate Dockerfiles
  -  Custom bridge network
  -  Clean folder structure and simple orchestration

---

### 📁 Project Structure

```
.
├── docker-compose.yml
├── nginx
│   ├── default.conf
│   └── Dockerfile
├── service_1
│   ├── app.py
│   └── Dockerfile
├── service_2
│   ├── app.py
│   └── Dockerfile
└── README.md
```

---

## Screenshots
### 1. 
![image](https://github.com/user-attachments/assets/08c9a73b-6dac-4bc3-acd2-bbceb7b3cbed)
### 2.
![image](https://github.com/user-attachments/assets/55e3b7af-5644-414b-a544-09dc337f436a)



