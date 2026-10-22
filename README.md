# Phanidhar Reddy Guttikonda
### Cloud Backend Engineer & Distributed Systems Consultant

I architect, build, and scale production cloud backends, microservices, and asynchronous event-driven pipelines. My focus centers on high-concurrency systems, low-latency microservices, and automated AWS infrastructure provisioned via Terraform.

- 💼 **Available for:** Freelance sprints, cloud infrastructure automation, and backend scaling (15–20 hrs/week).
- 💬 **Ask me about:** AWS (ECS Fargate, RDS Proxy, 3-Tier VPC, SQS), Rust (Tokio, Axum), Go, Spring Boot, and Concurrency.
- 📬 **Reach out:** [guttikondaphanidharreddy@gmail.com](mailto:guttikondaphanidharreddy@gmail.com) | [LinkedIn](https://www.linkedin.com/in/phanidhar-reddy-guttikonda-321817233/) | [Portfolio](https://phani.services)

---

### 💻 Production Tech Stack

<p align="left">
  <img src="https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS" />
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" alt="Terraform" />
  <img src="https://img.shields.io/badge/Rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/PostgreSQL-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-%23DC382D.svg?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka" alt="Kafka" />
  <img src="https://img.shields.io/badge/Node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
</p>

- **Cloud & DevOps (AWS):** 3-Tier VPC, ECS Fargate, ALB, RDS PostgreSQL, RDS Proxy, Lambda, SQS, EventBridge, Secrets Manager, CloudWatch, Terraform (IaC)
- **Languages & Frameworks:** Rust (Axum, Tokio), Go, Java (Spring Boot), TypeScript, Node.js (Express), SQL
- **Databases & Messaging:** PostgreSQL 16, Redis (Atomicity, Clustering, Pub/Sub), Apache Kafka, gRPC (HTTP/2), WebSockets
- **Reliability & Architecture:** Docker, GitHub Actions CI/CD, Pino Structured Logging, Dead-Letter Queues (DLQ), Multi-Tenant RBAC

---

### 🚀 Featured Production Projects

#### 1. Paatam — Enterprise AI SaaS & Cloud Infrastructure
*Architected and provisioned the enterprise backend, AWS infrastructure, and CI/CD pipelines from HLD to production.*
- **Cloud Topology:** 3-tier isolated VPC (`ap-south-2`), containerized TypeScript on AWS ECS Fargate behind an ALB, fully codified via modular Terraform.
- **Database Resilience:** PostgreSQL 16 schema with Sonyflake 64-bit distributed IDs and RDS Proxy connection multiplexing to stop connection exhaustion during traffic bursts.
- **Decoupled Async Pipeline:** 4 SQS queues with 15-minute visibility timeouts, 4 DLQs (14-day retention), 5 Lambda workers, and an EventBridge self-healing sweeper cron.
- **Deployment & QA:** Automated GitHub Actions CI/CD pipeline with 230 passing tests and rolling zero-downtime container deployments to AWS ECR.

#### 2. Real-Time Distributed Auction Platform (Rust / Tokio)
*High-throughput real-time bidding backend sustaining 10 concurrent auction rooms and 100+ WebSocket connections at 200ms intervals.*
- Built with stateless **Rust (Axum)** and Redis atomic operations to eliminate race conditions[cite: 1, 19].
- Engineered non-blocking disk-write execution via Tokio MPSC channels and DLQ retries, lowering message latency to **274ns** and saving **11ms** blocking DB overhead[cite: 1, 19].
- Reduced p99 latency by **1.7x (85.2ms → 48.7ms)** while processing **1,200+ bids/sec** at 67.1 MB RAM under load[cite: 1, 19].
- [Live Demo](https://ipl-auction.phani.services)

#### 3. High-Throughput Microservices Platform (Java / Go / Kafka)
*Event-driven microservice ecosystem (Identity, Timeline, Notifications).*
- Built internal service-to-service communication via **gRPC over HTTP/2** with centralized REST API Gateway status mapping[cite: 1, 19].
- Implemented high-throughput feed caching with Redis fan-out and decoupled event streaming using Kafka and AWS SQS with DLQs[cite: 1, 19].
