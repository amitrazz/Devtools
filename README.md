# Devtools
Docker Compose setup for development
# 🛠️ Dev Tools for Local Development

This folder contains Docker Compose setups for essential developer tools used in fullstack and DevOps workflows. Each service is isolated and self-contained for easy use, testing, and persistence.

---

## Services & Usage

### General Usage

To run any tool:

```bash
docker compose -f ./<service>/docker-compose.yml up -d

To stop:
docker compose -f ./<service>/docker-compose.yml down

Tools Overview
| Tool              | Port(s)     | Access URL                                                              | Notes                        |
| ----------------- | ----------- | ----------------------------------------------------------------------- | ---------------------------- |
| **PostgreSQL**    | 5432        | —                                                                       | Use with pgAdmin             |
| **MySQL**         | 3306        | —                                                                       | Use with MySQL Workbench     |
| **MongoDB**       | 27017       | —                                                                       | Use with Mongo Express       |
| **Redis**         | 6379        | —                                                                       | Redis cache + queue store    |
| **RabbitMQ**      | 5672, 15672 | [http://localhost:15672](http://localhost:15672)                        | guest / guest                |
| **Kafka**         | 9092, 8080  | [http://localhost:8080](http://localhost:8080)                          | Kafka + UI + Zookeeper       |
| **LocalStack**    | 4566        | [http://localhost:4566/\_localstack](http://localhost:4566/_localstack) | AWS services emulation       |
| **MinIO**         | 9000, 9001  | [http://localhost:9001](http://localhost:9001)                          | S3-compatible local storage  |
| **Grafana**       | 3000        | [http://localhost:3000](http://localhost:3000)                          | admin / admin                |
| **Prometheus**    | 9090        | [http://localhost:9090](http://localhost:9090)                          | Metrics collection           |
| **Kibana**        | 5601        | [http://localhost:5601](http://localhost:5601)                          | Elasticsearch UI             |
| **Elasticsearch** | 9200, 9300  | [http://localhost:9200](http://localhost:9200)                          | Full-text search engine      |
| **Redis Insight** | 5540        | [http://localhost:5540](http://localhost:5540)                          | Redis UI                     |
| **Mongo Express** | 8081        | [http://localhost:8081](http://localhost:8081)                          | MongoDB UI                   |
| **pgAdmin**       | 5050        | [http://localhost:5050](http://localhost:5050)                          | PostgreSQL UI                |
| **MeiliSearch**   | 7700        | [http://localhost:7700](http://localhost:7700)                          | Lightweight full-text search |
| **Storybook**     | 6006        | [http://localhost:6006](http://localhost:6006)                          | UI component explorer        |

Notes
All services store persistent data in ./<tool>/data/

.gitkeep is used to retain empty data folders in Git

All docker-compose.yml files are versioned separately per service

Secrets, tokens, and credentials are set to safe dev-mode defaults

📁 Folder Structure
dev-tools/
├── postgres/
├── mysql/
├── redis/
├── redis-insight/
├── mongodb/
├── mongo-express/
├── rabbitmq/
├── kafka/
├── localstack/
├── minio/
├── grafana/
├── elasticsearch/
├── meilisearch/
├── storybook/
└── README.md

.gitignore Tip
*/data/*
!*/data/.gitkeep

