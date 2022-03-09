# DApp-monitoring-data

For a Hyperledger Fabric based Decentralized application (DApp), we use Prometheus to collect real-time data and Caliper to simulate workload generation. 
When the DApp receives transaction requests stably, we add system pressures with stress-ng, such as I/O pressure to inject anomalies manually. 

The data is mainly about system resource metrics, such as CPU usage, system load, etc. We increase I/O pressure for 20 minutes every hour. 
We keep monitoring the DApp and collect data every 15 seconds, resulting in 7426 samples and 201 resource-related metrics. 
In addition, a metric that represents the number of transaction failures can be seen as the anomaly indicator of the DApp. 
We label anomalies when the transaction failure number is not zero, which can be seen in the table. 

