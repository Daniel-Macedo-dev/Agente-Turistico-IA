# 🧭 Agente Turístico IA

Projeto automatizado desenvolvido com **N8N** e **WAHA (WhatsApp HTTP API)** para atuar como um **assistente turístico em São Paulo**, oferecendo atendimento via WhatsApp, recomendações personalizadas e automação de fluxos.

O ambiente é totalmente **containerizado com Docker Compose**, integrando **N8N**, **WAHA**, **PostgreSQL** e **Redis** em uma arquitetura voltada para atendimento conversacional automatizado.

---

## 📌 Visão Geral

O **Agente Turístico IA** foi criado para funcionar como um assistente automatizado para turistas em São Paulo, utilizando WhatsApp como canal principal de comunicação.

O projeto permite:

- atendimento automatizado via WhatsApp
- organização de fluxos com N8N
- gerenciamento de sessões e mídia com WAHA
- persistência de dados com PostgreSQL
- uso de Redis como apoio para cache e sessão
- execução completa em ambiente containerizado

---

## 🧱 Tecnologias Utilizadas

- **N8N** — automação de fluxos e integrações
- **WAHA (WhatsApp HTTP API)** — comunicação via WhatsApp
- **PostgreSQL** — banco de dados relacional
- **Redis** — cache e suporte a sessão
- **Docker Compose** — orquestração dos serviços

---

## 🏛️ Estrutura do Projeto

```text
Agente-Turistico-IA/
├── docker-compose.yml       # Configuração dos containers
└── workflows/               # Fluxos exportados do N8N
````

---

## 🚀 Funcionalidades

* Atendimento automatizado via **WhatsApp**
* Recomendação de **pontos turísticos, restaurantes e atrações**
* Orquestração visual de fluxos no **N8N**
* Gerenciamento de **sessões e mídia** pelo **WAHA**
* Persistência de dados com **PostgreSQL**
* Suporte a cache e sessão com **Redis**
* Ambiente pronto para execução com **Docker Compose**

---

## 🧩 Arquitetura de Integração

| Serviço        | Função                                       |
| -------------- | -------------------------------------------- |
| **N8N**        | Criação e orquestração dos fluxos            |
| **WAHA**       | Envio e recebimento de mensagens do WhatsApp |
| **PostgreSQL** | Persistência de dados                        |
| **Redis**      | Cache e apoio para sessão                    |

---

## ⚙️ Como Executar o Projeto

### Pré-requisitos

Antes de iniciar, tenha instalado:

* **Docker**
* **Docker Compose**

### Subindo os containers

Na raiz do projeto, execute:

```bash
docker compose up -d
```

---

## ▶️ Serviços Disponíveis

Após a inicialização:

* **N8N:** `http://localhost:5678`
* **WAHA Dashboard:** `http://localhost:3000`

---

## 💾 Persistência de Dados

Os dados são mantidos por meio de volumes Docker:

| Serviço    | Volume          | Função                           |
| ---------- | --------------- | -------------------------------- |
| PostgreSQL | `pgdata`        | Armazena os dados do banco       |
| WAHA       | `waha_sessions` | Armazena sessões do WhatsApp     |
| WAHA       | `waha_media`    | Armazena arquivos de mídia       |
| N8N        | `n8n_data`      | Armazena workflows e credenciais |

---

## 🔌 Detalhes do Ambiente

O `docker-compose.yml` configura:

* **Redis** com autenticação básica
* **PostgreSQL** com banco, usuário e senha definidos por ambiente
* **WAHA** com dashboard sem senha e webhook apontando para o N8N
* **N8N** configurado com timezone `America/Sao_Paulo`

---

## 🧠 Conceito do Projeto

O objetivo do **Agente Turístico IA** é oferecer suporte automatizado a turistas que desejam informações rápidas e contextualizadas sobre São Paulo, como:

* pontos turísticos
* restaurantes
* eventos e atrações
* dicas úteis para deslocamento e permanência

Tudo isso com atendimento via WhatsApp e automação baseada em fluxos.

---

## 🌐 Deploy

O projeto pode ser executado em qualquer ambiente com suporte a Docker Compose, como:

* VPS
* Railway
* Render
* AWS EC2

Para subir o ambiente, basta utilizar:

```bash
docker compose up -d
```

---

## 🎯 Objetivos do Projeto

Este projeto foi desenvolvido com foco em:

* automação de atendimento conversacional
* integração entre serviços containerizados
* uso de WhatsApp como canal de atendimento
* orquestração de fluxos com N8N
* prática de arquitetura com PostgreSQL, Redis e Docker Compose

---

## 📄 Licença

Este projeto está licenciado sob a **MIT License**.
