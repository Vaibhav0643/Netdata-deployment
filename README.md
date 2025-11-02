# 🧠 TASK 7: Monitor System Resources Using Netdata

### 🎯 Objective
Install and run **Netdata** to visualize real-time system and container performance metrics such as CPU, memory, disk I/O, and network usage — all from a beautiful web dashboard.  
For more info, visit the [Netdata Documentation](https://learn.netdata.cloud)
---

## 🧰 Tools & Technologies
- 🐳 **Docker**
- 📊 **Netdata (Open Source Monitoring Tool)**

---

## ⚙️ Steps to Reproduce

### 1. Pull the Netdata Docker Image
```bash
docker pull netdata/netdata
```
### 2. Run the Netdata Container
```bash
docker run -d --name=netdata -p 19999:19999 netdata/netdata
```

### 3. Access the Dashboard
Once the container is running, open your browser and visit:
👉 http://localhost:19999

You’ll see live metrics such as:

- CPU utilization (per core)
- Memory & swap usage
- Disk read/write throughput
- Network traffic
- Running Docker containers

### 4. Explore Alerts & Charts
- Click on any chart to drill into real-time data.
- Navigate to "Health" → "Alerts" to view automatically configured thresholds and warnings.
- Hundreds of charts are available across categories like system, apps, disks, and network.

### 5. Check Logs
To view Netdata logs inside the container:
```bash
docker exec -it netdata bash
cd /var/log/netdata
ls
```
Logs include:
- error.log
- access.log
- health.log

### 📸 Screenshots
- All screenshots related to this task are available in the [./Screenshots](./Screenshots) folder.
