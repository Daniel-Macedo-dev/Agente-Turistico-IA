# 🧭 Agente Turístico IA

Aplicação **automatizada** desenvolvida com **N8N** e **WAHA (WhatsApp API)** para atuar como um **assistente de viagens em São Paulo**, capaz de **atender turistas**, **fornecer recomendações personalizadas** e **automatizar respostas via WhatsApp**.

O sistema é totalmente **containerizado com Docker Compose**, incluindo **N8N**, **WAHA**, **PostgreSQL** e **Redis**, funcionando como um **ecossistema inteligente de atendimento turístico**.

## 🧱 Tecnologias Utilizadas

* **N8N** – Automação de fluxos e integração com APIs
* **WAHA (WhatsApp HTTP API)** – Comunicação via WhatsApp
* **PostgreSQL** – Banco de dados relacional
* **Redis** – Cache e persistência de sessões
* **Docker Compose** – Orquestração dos serviços

## 📁 Estrutura do Projeto

```
Agente-Turistico-IA/
├── docker-compose.yml       # Configuração dos containers
└── workflows/               # Fluxos exportados do N8N
```
## 🚀 Funcionalidades

* Atendimento automatizado via **WhatsApp**
* Recomendação de **pontos turísticos, restaurantes e eventos**
* Respostas personalizadas com **Gemini 2.5 Flash**
* Integração com **bancos de dados locais**
* Painel visual de fluxos no **N8N**
* Sessões e mídia gerenciadas automaticamente pelo **WAHA**

## ⚙️ Execução do Projeto

### 🔹 Subindo os Containers

Na raiz do projeto, execute:

```bash
docker compose up -d
```
Após o processo de inicialização:

* **N8N:** [http://localhost:5678](http://localhost:5678)
* **WAHA Dashboard:** [http://localhost:3000](http://localhost:3000)

## 💾 Volumes Persistentes

Os dados são salvos automaticamente através dos volumes do Docker:

| Serviço    | Volume                        | Função                      |
| ---------- | ----------------------------- | --------------------------- |
| PostgreSQL | `pgdata`                      | Armazena dados do banco     |
| WAHA       | `waha_sessions`, `waha_media` | Sessões e arquivos de mídia |
| N8N        | `n8n_data`                    | Workflows e credenciais     |
| Redis      | `redis_data`                  | Cache de sessão             |

## 🧠 Conceito

O **Agente Turístico IA** é um **assistente automatizado** que atua no WhatsApp para **ajudar viajantes em São Paulo**, oferecendo informações sobre:

* Pontos turísticos
* Restaurantes locais
* Eventos e atrações
* Dicas de transporte e hospedagem

Tudo isso através de **fluxos inteligentes criados no N8N**, com **respostas em linguagem natural** geradas pela **IA 2.5 Flash**.

## 🧩 Estrutura de Integração

| Serviço        | Função                                       |
| -------------- | -------------------------------------------- |
| **N8N**        | Criação e orquestração dos fluxos            |
| **WAHA**       | Envio e recebimento de mensagens do WhatsApp |
| **Redis**      | Cache de sessões                             |
| **PostgreSQL** | Armazenamento de dados persistentes          |

---

## 🌐 Deploy

O projeto pode ser hospedado em qualquer serviço que suporte Docker, como **Render**, **Railway**, **VPS** ou **AWS EC2**.
Basta copiar o `docker-compose.yml` e executar:

```bash
docker compose up -d
```
## 📄 Licença

Este projeto está licenciado sob a **MIT License**.
