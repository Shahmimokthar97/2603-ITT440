# Performance Testing and Bottleneck Analysis of DummyJSON Products API Using Apache JMeter

Course: ITT440 - Network Programming \
Group: NBCS2555A \
Name: Muhamad Shahmi Bin Mokthar \
Matrix No.: 2024727655

---
## Project Overview
This project evaluates the performance and scalability of the DummyJSON Products API using Apache JMeter.

The project focuses on analyzing API behavior under different concurrent user loads using Load Testing, Stress Testing, and Spike Testing techniques.

---

## Tool Used

- Apache JMeter 5.6
- Java JDK
- Windows 11

---

## Target API

REST Countries API \
https://dummyjson.com/products

---

## Objectives

- Evaluate API performance under different workloads
- Analyze response time and throughput
- Identify bottlenecks during high traffic
- Observe API behavior during sudden traffic spikes

---

## Test Types

### 1. Load Test
Purpose:
Evaluate API performance under normal traffic conditions.

| Setting | Value |
|---|---|
| Users | 50 |
| Ramp-up | 30 seconds |
| Duration | 5 minutes |

---

### 2. Stress Test
Purpose:
Determine system behavior under excessive load.

| Setting | Value |
|---|---|
| Users | 150 |
| Ramp-up | 60 seconds |
| Duration | 5 minutes |

---

### 3. Spike Test
Purpose:
Analyze API response during sudden traffic spikes.

| Setting | Value |
|---|---|
| Initial Users | 20 |
| Spike Users | 150 |
| Spike Time | 5 seconds |
| Duration | 3 minutes |


---

## HTTP Request Configuration

| Field | Value |
|---|---|
| Protocol | https |
| Server Name | dummyjson.com |
| Method | GET |
| Path | /products |

---

## Key Performance Indicators (KPIs)

- Average Response Time
- Throughput
- Error Rate
- Latency
- 95th Percentile Response Time

---

## Project Structure

```plaintext
MUHAMAD SHAHMI BIN MOKTHAR\
│
├── README.md
├── screenshots/
├── results/
├── jmeter/
└── report.pdf
```

## Sample Results

| Test Type | Avg Response Time | Throughput | Error Rate |
|---|---|---|---|
| Load Test | 220 ms | 60 req/sec | 0% |
| Stress Test | 1100 ms | 85 req/sec | 6% |
| Spike Test | 1800 ms | 70 req/sec | 11% |

---

## Bottleneck Analysis

Potential bottlenecks identified:

- Network latency
- API throttling
- Request queue congestion
- Server processing delays

---

## Recommendations

- Implement caching mechanisms
- Use CDN services
- Optimize API response handling
- Apply load balancing strategies

---

## Conclusion

This project successfully evaluated the performance and scalability of DummyJSON Products API using Apache JMeter.

The results indicate that the API performs efficiently under moderate workloads but experiences increased latency and error rates under excessive traffic conditions.

---
