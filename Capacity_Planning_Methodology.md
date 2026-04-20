## 📊 Capacity Planning & Performance Methodology (IBM Era)

To manage 500+ hosts effectively, I utilized a "Data-Driven" approach to avoid performance bottlenecks:

### **1. Resource Overcommitment Ratios**
* **vCPU to pCPU:** Maintained a strict 4:1 ratio for Tier-1 applications to ensure consistent CPU ready times.
* **Memory Management:** Monitored balloon driver activity and transparent page sharing (TPS) to optimize RAM utilization without impacting latency.

### **2. Storage I/O Optimization**
* **Latency Thresholds:** Established 20ms alerts on datastores to trigger storage vMotion and rebalance I/O across the SAN fabric.
* **C-Drive Expansion Protocol:** Developed a standardized workflow for expanding Windows/Linux volumes without requiring downtime.

### **3. Root Cause Analysis (RCA) Framework**
* Used VMware esxtop and performance logs to isolate "noisy neighbor" VMs and apply DRS affinity/anti-affinity rules.
