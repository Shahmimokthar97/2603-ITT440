# Performance Testing and Bottleneck Analysis of REST Countries API Using Apache JMeter

Course: ITT440 - Network Programming \
Group: NBCS2555A \
Name: Muhamad Shahmi Bin Mokthar \
Matrix No.: 2024727655

---
## Project Overview
This project evaluates the performance and scalability of the REST Countries API using Apache JMeter.

The objective is to analyze API behavior under different concurrent user loads through Load Testing, Stress Testing, and Spike Testing.

---

## Tool Used

- Apache JMeter 5.6
- Java JDK
- Windows 11

---

## Target API

REST Countries API \
https://restcountries.com/v3.1/all

---

## Test Types

### 1. Load Test
Purpose:
Evaluate API performance under normal traffic conditions.

Configuration:
- Users: 50
- Ramp-up: 30 seconds
- Duration: 5 minutes

---

### 2. Stress Test
Purpose:
Determine system behavior under excessive load.

Configuration:
- Users: 150–200
- Ramp-up: 60 seconds
- Duration: 5 minutes

---

### 3. Spike Test
Purpose:
Analyze API response during sudden traffic spikes.

Configuration:
- Initial Users: 20
- Spike Users: 150
- Ramp-up: 5–10 seconds
- Duration: 3–5 minutes

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
restcountries-api-jmeter-performance-analysis/
│
├── README.md
├── screenshots/
├── results/
├── jmeter/
└── report.pdf
```

---

## JMeter Configuration

### HTTP Request

| Field | Value |
|------|------|
| Protocol | https |
| Server Name | restcountries.com |
| Method | GET |
| Path | /v3.1/all |

---

## Sample Results

| Test Type | Avg Response Time | Throughput | Error Rate |
|------------|------------------|-------------|------------|
| Load Test | 250 ms | 55 req/sec | 0% |
| Stress Test | 1900 ms | 90 req/sec | 12% |
| Spike Test | 2700 ms | 70 req/sec | 18% |

---

## Findings

- API performs efficiently under moderate traffic.
- Response time increases under excessive concurrent load.
- Sudden traffic spikes may cause temporary instability and increased latency.
- Error rates increase significantly during stress and spike testing.

---

## Recommendations

- Implement caching mechanisms
- Use CDN services
- Optimize server-side processing
- Apply load balancing strategies

---

## Conclusion

The project successfully demonstrates the use of Apache JMeter for REST API performance testing and highlights the importance of scalability and stability analysis in modern web services.

---
