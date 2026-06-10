# 💇 BeautyFlow 👨‍💻

> [!NOTE]
> Sistema de gerenciamento de salão de beleza que centraliza agendamentos, controle de profissionais, registro de atendimentos e geração de relatórios gerenciais.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O <b>BeautyFlow</b> é um sistema desenvolvido para digitalizar e centralizar os processos operacionais de um salão de beleza. O sistema abrange o <i>agendamento de serviços</i>, o <i>gerenciamento de profissionais</i>, o <i>registro de atendimentos e pagamentos</i> e a <i>geração de relatórios gerenciais</i>. O objetivo é proporcionar maior <b>eficiência operacional</b> para a equipe do salão e uma experiência mais <b>conveniente e prática</b> para os clientes. Este projeto foi desenvolvido como trabalho final da disciplina de <b>Engenharia de Software</b>, cobrindo modelagem de domínio, diagramação UML completa e arquitetura do sistema.
      </div>
    </td>
    <td>
      <div>
        💇‍♀️
      </div>
    </td>
  </tr>
</table>

---

## 🚧 Status do Projeto

[![Versão](https://img.shields.io/badge/Versão-v1.0.0-blue?style=for-the-badge)](https://github.com/beautyflow/beautyflow/releases)
![Node.js](https://img.shields.io/badge/Node.js-20.x-007ec6?style=for-the-badge&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-18.x-007ec6?style=for-the-badge&logo=react&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-007ec6?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-007ec6?style=for-the-badge&logo=docker&logoColor=white)
![PlantUML](https://img.shields.io/badge/PlantUML-Diagramas-007ec6?style=for-the-badge)
[![Licença](https://img.shields.io/badge/Licença-MIT-green?style=for-the-badge)](#licença)

---

## 📚 Índice
- [Links Úteis](#-links-úteis)
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
- [Diagramas UML](#-diagramas-uml)
- [Instalação e Execução](#-instalação-e-execução)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Modelos de Dados](#-modelos-de-dados)
- [Autores](#-autores)
- [Agradecimentos](#-agradecimentos)
- [Licença](#-licença)

---

## 🔗 Links Úteis
* 📖 **PlantUML:** [https://plantuml.com](https://plantuml.com) — Ferramenta utilizada para todos os diagramas do projeto.
* 📖 **Documentação da API:** [Swagger/OpenAPI](<link-para-docs>) — Documentação dos endpoints REST.
* 🌐 **Demo Online:** [Acesse a Aplicação](<link-da-demo>) — Ambiente de demonstração do sistema.

---

## 📝 Sobre o Projeto

O **BeautyFlow** surgiu da necessidade de modernizar a gestão de salões de beleza, que ainda dependem de agendas físicas, planilhas e processos manuais. O sistema resolve os seguintes problemas:

- **Agendamentos desorganizados:** conflitos de horários, esquecimentos e falta de confirmação automática.
- **Falta de controle financeiro:** dificuldade em acompanhar faturamento por serviço ou profissional.
- **Gestão ineficiente de profissionais:** sem visibilidade clara da agenda e disponibilidade de cada um.
- **Experiência ruim do cliente:** sem histórico de atendimentos ou lembretes automáticos.

O sistema atende quatro perfis de usuário — **Cliente**, **Recepcionista**, **Profissional** e **Administrador** — cada um com funcionalidades específicas para sua função no salão.

---

## ✨ Funcionalidades Principais

- 📅 **Agendamento Online:** Clientes agendam serviços escolhendo profissional, horário e data disponíveis.
- 🔔 **Notificações Automáticas:** Confirmações e lembretes enviados por e-mail ou SMS.
- 💈 **Gestão de Atendimentos:** Profissionais registram serviços realizados e finalizam atendimentos.
- 💳 **Registro de Pagamentos:** Suporte a dinheiro, cartão de crédito/débito e PIX, com emissão de recibo.
- 📊 **Relatórios Gerenciais:** Faturamento por período, desempenho por profissional e serviços mais realizados.
- 👥 **Gestão de Profissionais:** Cadastro, ativação, férias, suspensão e vínculo com serviços oferecidos.
- 🗓️ **Controle de Agenda:** Visualização da agenda diária por profissional com status de cada atendimento.
- 📂 **Histórico do Cliente:** Consulta completa de atendimentos passados e agendamentos futuros.

---

## 🛠 Tecnologias Utilizadas

### 💻 Front-end
* **Biblioteca:** React 18.x
* **Linguagem:** TypeScript
* **Estilização:** Tailwind CSS
* **Build Tool:** Vite

### 🖥️ Back-end
* **Runtime:** Node.js 20.x
* **Framework:** Express.js
* **Banco de Dados:** PostgreSQL 16
* **ORM:** Prisma
* **Autenticação:** JWT
* **Cache:** Redis

### ⚙️ Infraestrutura & DevOps
* **Containerização:** Docker / Docker Compose
* **Proxy Reverso:** Nginx
* **Notificações:** SendGrid (e-mail) / Twilio (SMS)
* **Pagamentos:** Stripe / PagSeguro

### 📐 Modelagem
* **Diagramação:** PlantUML
* **Metodologia:** UML 2.0

---

## 🏗 Arquitetura

O BeautyFlow adota uma arquitetura em camadas (**Layered Architecture**) organizada em:

- **Interface Layer:** Aplicação Web (React) e App Mobile (React Native)
- **API Layer:** API REST com Gateway, Controllers, Services e Repositories
- **Data Layer:** PostgreSQL para persistência e Redis para cache de sessões
- **External Services:** Gateway de pagamento e serviço de notificações

A separação em camadas garante baixo acoplamento, alta coesão e facilidade de manutenção. O padrão **Repository** isola o acesso a dados, o **Service Layer** concentra as regras de negócio e os **Controllers** cuidam exclusivamente do roteamento HTTP.

---

## 📐 Diagramas UML

Todos os diagramas foram elaborados em **PlantUML**. Os arquivos `.puml` estão disponíveis na pasta `/docs/diagramas`.

### Modelos de Usuário e Requisitos

| Diagrama | Arquivo |
| :--- | :--- |
| Casos de Uso | `/docs/diagramas/UC-BeautyFlow.puml` |
| Sequência do Sistema — UC-01: Agendar Serviço | `/docs/diagramas/SD-UC01-AgendarServico.puml` |
| Sequência do Sistema — UC-02: Gerenciar Profissionais e Serviços | `/docs/diagramas/SD-UC02-GerenciarProfissionaisServicos.puml` |
| Sequência do Sistema — UC-03: Registrar Atendimento e Pagamento | `/docs/diagramas/SD-UC03-RegistrarAtendimentoPagamento.puml` |
| Sequência do Sistema — UC-04: Consultar Histórico e Relatórios | `/docs/diagramas/SD-UC04-ConsultarHistoricoRelatorios.puml` |

### Modelos de Projeto

| Diagrama | Arquivo |
| :--- | :--- |
| Arquitetura UML | `/docs/diagramas/ARQ-UML-Arquitetura.puml` |
| Componentes | `/docs/diagramas/DC-Componentes.puml` |
| Implantação | `/docs/diagramas/DI-Implantacao.puml` |
| Classes | `/docs/diagramas/DC-Classes.puml` |
| Sequência de Projeto — UC-01 | `/docs/diagramas/DSP-UC01-AgendarServico.puml` |
| Sequência de Projeto — UC-02 | `/docs/diagramas/DSP-UC02-GerenciarProfissionaisServicos.puml` |
| Sequência de Projeto — UC-03 | `/docs/diagramas/DSP-UC03-RegistrarAtendimentoPagamento.puml` |
| Sequência de Projeto — UC-04 | `/docs/diagramas/DSP-UC04-ConsultarHistoricoRelatorios.puml` |
| Comunicação — UC-01 | `/docs/diagramas/COM-UC01-AgendarServico.puml` |
| Comunicação — UC-02 | `/docs/diagramas/COM-UC02-GerenciarProfissionaisServicos.puml` |
| Comunicação — UC-03 | `/docs/diagramas/COM-UC03-RegistrarAtendimentoPagamento.puml` |
| Comunicação — UC-04 | `/docs/diagramas/COM-UC04-ConsultarHistoricoRelatorios.puml` |
| Estados — Agendamento | `/docs/diagramas/DE-Agendamento.puml` |
| Estados — Pagamento | `/docs/diagramas/DE-Pagamento.puml` |
| Estados — Atendimento | `/docs/diagramas/DE-Atendimento.puml` |
| Estados — Profissional | `/docs/diagramas/DE-Profissional.puml` |
| Estados — Serviço | `/docs/diagramas/DE-Servico.puml` |
| Modelo de Dados (ER) | `/docs/diagramas/MD-EsquemaBancoDados.puml` |

---

## 🔧 Instalação e Execução

### Pré-requisitos

* **Node.js:** Versão LTS (v20.x ou superior)
* **Docker** e **Docker Compose**
* **Extensão PlantUML no VSCode** (`jebbs.plantuml`) para visualizar os diagramas

### 🔑 Variáveis de Ambiente

Crie um arquivo **`.env`** na raiz do projeto com as seguintes variáveis:

| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `SERVER_PORT` | Porta do servidor | `3000` |
| `DATABASE_URL` | URL de conexão PostgreSQL | `postgresql://postgres:senha@localhost:5432/beautyflow` |
| `JWT_SECRET` | Chave secreta para tokens JWT | `chave_super_segura` |
| `REDIS_URL` | URL de conexão Redis | `redis://localhost:6379` |
| `SENDGRID_API_KEY` | Chave da API SendGrid | `SG.sua_key_aqui` |
| `STRIPE_SECRET_KEY` | Chave secreta Stripe | `sk_live_sua_key_aqui` |

### 📦 Instalação de Dependências

1. **Clone o Repositório:**
```bash
git clone https://github.com/seu-usuario/beautyflow.git
cd beautyflow
```

2. **Instale as Dependências:**
```bash
# Front-end
cd frontend
npm install
cd ..

# Back-end
cd backend
npm install
cd ..
```

### 💾 Inicialização do Banco de Dados

```bash
docker run --name beautyflow_db \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=senha123 \
  -e POSTGRES_DB=beautyflow \
  -p 5432:5432 -d postgres:16
```

```bash
cd backend
npx prisma migrate dev
```

### ⚡ Como Executar

**Terminal 1 — Back-end:**
```bash
cd backend
npm run dev
```
🚀 API disponível em **http://localhost:3000**

**Terminal 2 — Front-end:**
```bash
cd frontend
npm run dev
```
🎨 Front-end disponível em **http://localhost:5173**

### 🐳 Execução com Docker Compose

```bash
docker-compose up --build -d
```

---

## 📂 Estrutura de Pastas

```
beautyflow/
├── README.md
├── docker-compose.yml
│
├── /docs
│   └── /diagramas              # 📐 Todos os arquivos .puml do projeto
│       ├── UC-BeautyFlow.puml
│       ├── SD-UC01-AgendarServico.puml
│       ├── DC-Classes.puml
│       ├── MD-EsquemaBancoDados.puml
│       └── ...
│
├── /frontend                   # 💻 Aplicação React
│   ├── /src
│   │   ├── /components
│   │   ├── /pages
│   │   ├── /services
│   │   └── /hooks
│   └── package.json
│
└── /backend                    # 🖥️ API Node.js / Express
    ├── /src
    │   ├── /controllers
    │   ├── /services
    │   ├── /repositories
    │   ├── /models
    │   └── /config
    ├── /prisma
    │   └── schema.prisma
    └── package.json
```

---

## 🗄 Modelos de Dados

O banco de dados é composto pelas seguintes tabelas principais:

| Tabela | Descrição |
| :--- | :--- |
| `clientes` | Dados dos clientes do salão |
| `profissionais` | Dados dos profissionais |
| `servicos` | Catálogo de serviços e preços |
| `profissional_servico` | Vínculo N:M entre profissionais e serviços |
| `horarios_disponiveis` | Grade de horários de cada profissional |
| `agendamentos` | Agendamentos realizados |
| `atendimentos` | Registro de atendimentos executados |
| `atendimento_servicos` | Serviços realizados em cada atendimento |
| `pagamentos` | Pagamentos registrados |
| `recibos` | Recibos emitidos |
| `usuarios` | Usuários do sistema (recepcionistas e administradores) |
| `relatorios` | Relatórios gerados |

O esquema completo está disponível em `/docs/diagramas/MD-EsquemaBancoDados.puml`.

---

## 👥 Autores

| 👤 Nome | :octocat: GitHub |
|---------|-----------------|
| David Olinda Pomine | ([https://github.com/seu-usuario)](https://github.com/DavidOlinda) |

---

## 🙏 Agradecimentos

* [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo apoio institucional e estrutura acadêmica.
* [**Prof. Dr. João Paulo Aramuni**](https://github.com/joaopauloaramuni) — Pelos ensinamentos sobre Arquitetura de Software e Padrões de Projeto.
* [**PlantUML**](https://plantuml.com) — Pela ferramenta de diagramação utilizada em todo o projeto.

---

## 📄 Licença

Este projeto é distribuído sob a **[Licença MIT](./LICENSE)**.
