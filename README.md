# 🎬 CineFlow - Plataforma de Streaming (Microsserviços)

**CineFlow** é um projeto de arquitetura distribuída para plataformas de streaming, utilizando Microsserviços, Docker e RabbitMQ.

---

## 🏗 Arquitetura e Portas

O sistema é composto pelos seguintes serviços orquestrados:

| Serviço | Porta Local | Descrição |
| :--- | :--- | :--- |
| **CineFlow User** | `8001` | Criação de usuários e Consumidor de filas (RabbitMQ). |
| **CineFlow Catalog** | `8002` | Consulta de filmes (Integração com IMDB API + Mock). |
| **CineFlow Streaming** | `8003` | Orquestrador de playback e Publicador de eventos. |
| **RabbitMQ** | `5673` | Message Broker (Porta alterada para evitar conflitos). |
| **RabbitMQ Mgmt** | `15673` | Interface de gerenciamento do RabbitMQ. |

---

## 🛠 Tecnologias

* **Linguagem:** Python 3.14.0 / 3.11-slim (Docker)
* **Orquestração:** Docker Desktop (v28.5.1) & Docker Compose (v2.40.3)
* **Mensageria:** RabbitMQ (Imagem: 3-management)
* **Bibliotecas Principais:** FastAPI, Uvicorn, Pydantic, Httpx, Aio-pika.

---

## 🚀 Instalação e Execução

### 1. Clonar o Repositório
```bash
git clone [https://github.com/Raimundofiles/CineFlow-Microservices](https://github.com/Raimundofiles/CineFlow-Microservices)
cd CineFlow-Microservices
