# Netdata System Monitoring using Docker

This project demonstrates how to install and run **Netdata** in a Docker container to monitor system resources in real-time.

## 📌 Objective
Install Netdata and visualize system and application performance metrics.

---

## 🚀 Steps to Execute

### 1. Install Docker
Check if Docker is installed:
```bash
docker --version
```

- If not installed:
```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl enable docker --now
```

### 2. Run Netdata Container
```bash
docker run -d --name=netdata -p 19999:19999 --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
```
<img width="650" height="250" alt="a9dbf7e4-7c45-4163-8d5b-3de62e5c3764" src="https://github.com/user-attachments/assets/dc28ef17-3457-4e63-94b0-d1252b26ed46" />


### 3. Access the Dashboard
- Open your browser and visit:
```arduino
http://localhost:19999
```
- If running on a remote server, replace localhost with the server's public IP.
<img width="1000" height="500" alt="87b846b4-8463-46e8-a80e-fdc5027f212c" src="https://github.com/user-attachments/assets/3b6623b9-10ce-4aa3-adcf-723ca2fe816a" />


### 4. Monitor Metrics
You can monitor:
- CPU usage
- Memory usage
- Disk I/O
- Network traffic
- Docker container stats
<img width="1000" height="500" alt="1c662c3d-9b7e-4f38-ba54-c773e1960d60" src="https://github.com/user-attachments/assets/ccc6e45d-98a7-45de-94ff-7208808bbe03" />


### References
[Netdata Documentation](https://learn.netdata.cloud/docs/getting-started)
<br>
[Docker Hub - Netdata](https://hub.docker.com/r/netdata/netdata)
