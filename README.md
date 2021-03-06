# DApp-monitoring-data

## High-level use case explanation.

A decentralized application (DApp) is a type of distributed application that runs on a peer-to-peer (P2P) blockchain network. For a running DApp deployed in cloud environments, performance anomalies such as degraded response time, transaction failure etc. will affect user experience and QoS (Quality of Service) severely. With monitoring tools, multiple metrics can be collected and these metrics can reflect the health status of applications. Performance anomaly detection based on monitoring metrics to identify the abnormal performance behaviour and forestall future incidents is necessary. 

## What kind of data is in the package?  

For a Hyperledger Fabric based Decentralized application (DApp), we use Caliper to simulate workload generation and Prometheus to collect real-time data. When the DApp receives transaction requests stably, we add system pressures with stress-ng, especially I/O pressure to inject anomalies. We increase I/O pressure for 20 minutes every hour, keep monitoring the DApp and collect data every 15 seconds. 

The data is all about system resource metrics, such as CPU/MEM usage, system load, etc. It's a time-series dataset and it includes 7426 samples and 201 resource-related metrics. In addition, we also provide a metric that represents the number of transaction failures which can be seen as anomaly indicators. We label anomalies when the transaction failure number is not zero, which can be seen in the table. 

## Connections between IDs (vocabulary, explaining individual)

In the dataset, you can see the time which is the timestamps we collected these data, and the time interval is 15s. 

We provide performance anomaly labels based on transaction failures. It can be used for supervised machine learning or to evaluate anomaly detection accuracy. 

All other columns are system resource related metrics, such as System load, CPU/MEM/NET usage. There are 201 resource-related metrics in total. 

<!--
# Public datasets

Vichalana Anomaly Benchmark: https://github.com/Vichalana/vichalana-anomaly-benchmark.git
-->

