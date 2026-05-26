# 🍰 GastroFlow 👨‍🍳

> [!NOTE]
> **GastroFlow** é um SaaS de gestão financeira e operacional para confeitarias e *dark kitchens*.
> Calcule o custo real das suas receitas, gerencie pedidos em tempo real e nunca mais fique sem insumos.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O <b>GastroFlow</b> é uma plataforma SaaS desenvolvida para resolver os principais gargalos operacionais de confeiteiros, doceiros e proprietários de <i>dark kitchens</i>. A ferramenta unifica em uma única interface o <b>cadastro de insumos e receitas</b>, o <b>cálculo automático de custos e margens</b>, o <b>painel de produção KDS</b> (Kitchen Display System) e a <b>geração automática de lista de compras</b>. O sistema foi projetado para ser altamente <i>sticky</i>: uma vez que o usuário cadastra suas receitas e insumos, toda a operação da cozinha passa a depender da plataforma, criando uma barreira natural de saída e fidelização orgânica.
      </div>
    </td>
    <td>
      <div align="center">
        <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f370/512.gif" alt="Logo GastroFlow" width="120px"/>
      </div>
    </td>
  </tr>
</table>

---

## 🚧 Status do Projeto

[![Versão](https://img.shields.io/badge/Versão-v1.0.0-2C6E49?style=for-the-badge)](https://github.com/seu-usuario/gastroflow/releases)
![Next.js](https://img.shields.io/badge/Next.js-15.x-007ec6?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-007ec6?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-20.x-007ec6?style=for-the-badge&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-007ec6?style=for-the-badge&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-5.x-007ec6?style=for-the-badge&logo=prisma&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-24.x-007ec6?style=for-the-badge&logo=docker&logoColor=white)
[![Licença](https://img.shields.io/badge/Licença-MIT-007ec6?style=for-the-badge&logo=opensourceinitiative)](LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/seu-usuario/gastroflow?style=for-the-badge&logo=clockify)](https://github.com/seu-usuario/gastroflow/commits/main)

---

## 📚 Índice
- [🔗 Links Úteis](#-links-úteis)
- [📝 Sobre o Projeto](#-sobre-o-projeto)
- [✨ Funcionalidades Principais](#-funcionalidades-principais)
- [🛠 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [🏗 Arquitetura](#-arquitetura)
- [🔧 Instalação e Execução](#-instalação-e-execução)
  - [Pré-requisitos](#pré-requisitos)
  - [🔑 Variáveis de Ambiente](#-variáveis-de-ambiente)
  - [📦 Instalação de Dependências](#-instalação-de-dependências)
  - [💾 Inicialização do Banco de Dados](#-inicialização-do-banco-de-dados-postgresql)
  - [⚡ Como Executar a Aplicação](#-como-executar-a-aplicação)
  - [🐳 Execução com Docker Compose](#-execução-local-completa-com-docker-compose)
- [🚀 Deploy](#-deploy)
- [📂 Estrutura de Pastas](#-estrutura-de-pastas)
- [🎥 Demonstração](#-demonstração)
- [🧪 Testes](#-testes)
- [🔗 Documentações Utilizadas](#-documentações-utilizadas)
- [👥 Autores](#-autores)
- [🤝 Contribuição](#-contribuição)
- [🙏 Agradecimentos](#-agradecimentos)
- [📄 Licença](#-licença)

---

## 🔗 Links Úteis

* 🌐 **Demo Online:** [Acesse a Aplicação Web](https://gastroflow.vercel.app)
  > 💻 **Descrição:** Aplicação hospedada na Vercel (frontend) com backend na AWS EC2. Use as credenciais de demonstração: `demo@gastroflow.com` / `Demo@1234`.

* 📖 **Documentação da API:** [Swagger / OpenAPI](https://api.gastroflow.com/docs)
  > 📚 **Descrição:** Documentação interativa de todos os endpoints REST da plataforma, gerada automaticamente via Swagger UI.

* 📖 **Documentação de Projeto:** [Documentação UML Completa](./docs/GastroFlow_Documentacao_Projeto.docx)
  > 📚 **Descrição:** Documento com diagramas PlantUML (Casos de Uso, Sequência, Classes, DER, Estados, Comunicação e Implantação).

---

## 📝 Sobre o Projeto

O **GastroFlow** nasceu da observação de uma dor real e muito comum entre pequenos produtores alimentícios: **a maioria dos confeiteiros e donos de dark kitchens não sabe exatamente quanto custa cada produto que produz**, e por isso trabalham com margens de lucro desconhecidas ou até negativas.

**Por que ele existe:**
Ferramentas de gestão como ERPs são caras e complexas demais para microempreendedores. Planilhas Excel são frágeis, não rodam em tablet na cozinha e não se atualizam automaticamente quando o preço de um insumo muda.

**Qual problema ele resolve:**
O GastroFlow ataca três problemas simultâneos:
1. **Precificação errada** — o sistema calcula o custo real e sugere o preço de venda com a margem desejada.
2. **Caos na produção** — o painel KDS substitui papéis e anotações avulsas, organizando a fila de produção em tempo real.
3. **Falta de insumos** — a explosão de demanda cruza os pedidos da semana com o estoque atual e gera automaticamente a lista de compras.

**Contexto:** Projeto acadêmico desenvolvido na disciplina de **Projeto de Software** (PUC Minas), simulando um produto SaaS real com arquitetura, modelagem UML completa e estratégia de negócio definida.

**Por que é relevante:**
O mercado de confeitaria artesanal e delivery de comida no Brasil cresceu mais de 30% pós-pandemia. O GastroFlow serve este nicho com uma proposta de valor clara, onboarding guiado e stickiness natural pela centralização de dados da operação.

---

## ✨ Funcionalidades Principais

- 🧾 **Ficha Técnica & Precificação:** Cadastro de receitas com cálculo automático de custo por grama/unidade e sugestão de preço de venda baseada em margem configurável.
- 📦 **Gestão de Insumos:** CRUD completo de insumos com unidade de medida, preço pago e quantidade da embalagem — o sistema calcula o custo unitário automaticamente.
- 📋 **Gestão de Pedidos:** Criação de pedidos vinculando produtos, cliente e data de entrega, com cálculo automático do valor total.
- 🖥️ **Painel KDS (Kitchen Display System):** Interface otimizada para tablet/monitor na cozinha com cards de pedidos em três colunas: *A Receber*, *Em Preparo* e *Pronto/Embalagem* — atualização em tempo real via WebSocket.
- 🛒 **Lista de Compras Automatizada (Explosão de Demanda):** Cruzamento automático entre pedidos do período e estoque atual, gerando a quantidade exata de cada insumo a comprar.
- 📊 **Relatórios Financeiros:** Visualização de receita, custos e margem por período.
- 🔐 **Autenticação Segura:** Login com JWT e suporte a OAuth2 (Google).
- 🚀 **Onboarding Guiado:** O sistema detecta o segmento do usuário (Confeitaria, Doceiro, Dark Kitchen) e pré-carrega os 30 insumos mais comuns com preços médios de mercado.
- 💳 **Assinaturas via Stripe/Asaas:** Cobrança recorrente de planos diretamente pela plataforma.

---

## 🛠 Tecnologias Utilizadas

### 💻 Front-end

* **Framework:** [Next.js v15](https://nextjs.org/) — SSR e geração estática para melhor SEO e performance
* **Biblioteca UI:** [React v19](https://react.dev/)
* **Linguagem:** TypeScript 5.x
* **Estilização:** Tailwind CSS v4
* **Gerenciamento de Estado:** Zustand
* **Comunicação em Tempo Real:** Socket.IO Client (painel KDS)
* **Build Tool:** Turbopack (nativo do Next.js 15)

### 🖥️ Back-end

* **Runtime:** Node.js v20 LTS
* **Framework:** Express.js com TypeScript
* **Banco de Dados:** PostgreSQL 16
* **ORM:** Prisma v5
* **Autenticação:** JWT + OAuth2 (Passport.js)
* **WebSocket:** Socket.IO (atualizações KDS em tempo real)
* **Validação:** Zod

### ⚙️ Infraestrutura & DevOps

* **Containerização:** Docker + Docker Compose
* **Cloud:** AWS (EC2 para backend, RDS para PostgreSQL, S3 para arquivos)
* **Frontend Deploy:** Vercel
* **CI/CD:** GitHub Actions
* **Pagamentos:** Stripe / Asaas

---

## 🏗 Arquitetura

O GastroFlow adota **Arquitetura em Camadas** (*Layered Architecture*) no backend, combinada com o padrão **MVC** e **Repository Pattern** para acesso a dados. O frontend segue a estrutura de componentes do Next.js App Router com separação clara entre páginas, componentes reutilizáveis e serviços HTTP.

**Principais decisões arquiteturais:**
- **WebSocket para o KDS:** A atualização de status dos pedidos precisa ser em tempo real para todos os dispositivos conectados na cozinha. Socket.IO foi escolhido pela facilidade de integração com Node.js e suporte a reconexão automática.
- **Prisma ORM:** Tipagem forte no acesso ao banco garante consistência nos cálculos financeiros, que são o core do produto.
- **PostgreSQL:** As relações complexas entre Insumos → Receitas → Pedidos → Itens exigem um banco relacional com suporte a transações ACID.
- **Monorepo:** Frontend e backend no mesmo repositório facilita o desenvolvimento solo e acadêmico.

**Trade-offs:** A escolha de Node.js sobre Java/Spring Boot sacrifica robustez em processamentos pesados em favor de agilidade no desenvolvimento e menor custo de infraestrutura para o MVP.

### Diagramas de Arquitetura

Os diagramas abaixo foram gerados com **PlantUML**. Para visualizá-los interativamente, acesse [plantuml.com](https://plantuml.com/) e cole o código disponível em [`/docs`](./docs/).

| Diagrama | Descrição |
| :---: | :---: |
| **Arquitetura C4 — Contêineres** | **Diagrama de Classes** |
| <img src="./docs/img/arquitetura_c4.png" alt="Arquitetura C4 Contêiner" width="320px"> | <img src="./docs/img/diagrama_classes.png" alt="Diagrama de Classes" width="320px"> |
| **DER — Banco de Dados** | **Diagrama de Estados — Pedido** |
| <img src="./docs/img/der.png" alt="Diagrama Entidade-Relacionamento" width="320px"> | <img src="./docs/img/estados_pedido.png" alt="Diagrama de Estados do Pedido" width="320px"> |
| **Diagrama de Componentes** | **Diagrama de Implantação** |
| <img src="./docs/img/componentes.png" alt="Diagrama de Componentes" width="320px"> | <img src="./docs/img/implantacao.png" alt="Diagrama de Implantação AWS" width="320px"> |

---

## 🔧 Instalação e Execução

### Pré-requisitos

* **Node.js:** Versão LTS **v20.x** ou superior
* **npm** v10+ ou **yarn** v1.22+
* **Docker** e **Docker Compose** (recomendado para o banco de dados)
* **Git**

---

### 🔑 Variáveis de Ambiente

#### Back-end (`/backend/.env`)

| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `PORT` | Porta do servidor Express | `3001` |
| `DATABASE_URL` | URL de conexão Prisma/PostgreSQL | `postgresql://gastro:senha123@localhost:5432/gastroflow` |
| `JWT_SECRET` | Chave secreta para assinatura JWT | `chave_super_segura_base64` |
| `JWT_EXPIRES_IN` | Tempo de expiração do token | `7d` |
| `STRIPE_SECRET_KEY` | Chave secreta da API Stripe | `sk_live_...` |
| `GOOGLE_CLIENT_ID` | Client ID OAuth2 Google | `xxxxx.apps.googleusercontent.com` |
| `GOOGLE_CLIENT_SECRET` | Client Secret OAuth2 Google | `GOCSPX-...` |
| `AWS_S3_BUCKET` | Nome do bucket S3 para uploads | `gastroflow-uploads` |
| `AWS_REGION` | Região AWS | `sa-east-1` |

#### Front-end (`/frontend/.env.local`)

| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `NEXT_PUBLIC_API_URL` | URL base da API backend | `http://localhost:3001/api` |
| `NEXT_PUBLIC_SOCKET_URL` | URL do servidor WebSocket | `http://localhost:3001` |
| `NEXT_PUBLIC_STRIPE_PK` | Chave pública Stripe | `pk_live_...` |
| `NEXTAUTH_SECRET` | Segredo para NextAuth | `uma_chave_muito_longa_e_segura` |
| `NEXTAUTH_URL` | URL da aplicação | `http://localhost:3000` |

**Exemplo para produção na Vercel:**

```
NEXT_PUBLIC_API_URL=https://api.gastroflow.com/api
NEXT_PUBLIC_SOCKET_URL=https://api.gastroflow.com
NEXTAUTH_SECRET=uma_chave_muito_longa_e_segura
NEXTAUTH_URL=https://gastroflow.vercel.app
```

---

### 📦 Instalação de Dependências

1. **Clone o repositório:**

```bash
git clone https://github.com/seu-usuario/gastroflow.git
cd gastroflow
```

2. **Instale as dependências do Front-end:**

```bash
cd frontend
npm install
cd ..
```

3. **Instale as dependências do Back-end:**

```bash
cd backend
npm install
cd ..
```

---

### 💾 Inicialização do Banco de Dados (PostgreSQL)

**Via Docker (recomendado):**

```bash
docker run --name gastroflow_db \
  -e POSTGRES_USER=gastro \
  -e POSTGRES_PASSWORD=senha123 \
  -e POSTGRES_DB=gastroflow \
  -p 5432:5432 \
  -d postgres:16
```

**Execute as migrações Prisma:**

```bash
cd backend
npx prisma migrate dev --name init
npx prisma db seed   # Carrega insumos padrão por segmento (onboarding)
```

---

### ⚡ Como Executar a Aplicação

Execute em **dois terminais separados**:

#### Terminal 1: Back-end (Express + Node.js)

```bash
cd backend
npm run dev
```

🚀 *API disponível em **http://localhost:3001** | WebSocket em **ws://localhost:3001***

#### Terminal 2: Front-end (Next.js)

```bash
cd frontend
npm run dev
```

🎨 *Front-end disponível em **http://localhost:3000***

---

### 🐳 Execução Local Completa com Docker Compose

Para subir o ambiente completo (frontend + backend + banco de dados) com um único comando:

```bash
# Certifique-se que o Docker está em execução
# Linux:
sudo systemctl start docker

# Suba todos os serviços
docker-compose up --build -d
```

Verifique se os containers estão saudáveis:

```bash
docker ps
docker logs gastroflow_backend
```

Acesse em: **http://localhost:3000**

Para encerrar:

```bash
docker-compose down
```

---

## 🚀 Deploy

1. **Build dos artefatos:**

```bash
# Front-end — gera /frontend/.next (deploy via Vercel CLI ou push no GitHub)
cd frontend
npm run build

# Back-end — gera /backend/dist (deploy via AWS EC2 ou Railway)
cd ../backend
npm run build
```

2. **Configuração de produção:** Configure as variáveis de ambiente no painel da **Vercel** (frontend) e como variáveis de ambiente do sistema no **EC2** (backend).

3. **Execução em produção:**

```bash
# Back-end (Node.js compilado)
cd backend
node dist/server.js

# Front-end — servido automaticamente pela Vercel após o push na branch main
```

> [!IMPORTANT]
> Configure as variáveis `DATABASE_URL` (apontando para o AWS RDS), `JWT_SECRET` e as chaves do Stripe no ambiente de produção antes do primeiro deploy.

---

## 📂 Estrutura de Pastas

```
gastroflow/
├── .github/                        # 🤖 CI/CD com GitHub Actions
├── .gitignore                      # 🧹 Arquivos não versionados
├── README.md                       # 📘 Documentação principal
├── CONTRIBUTING.md                 # 🤝 Guia de contribuição
├── LICENSE                         # ⚖️ Licença MIT
├── docker-compose.yml              # 🐳 Orquestração completa dos containers
│
├── /docs                           # 📚 Documentação técnica e diagramas
│   ├── GastroFlow_Documentacao_Projeto.docx  # 📄 UML completo (PlantUML)
│   └── /img                        # 🖼️ Imagens dos diagramas exportados
│
├── /frontend                       # 📁 Aplicação Next.js
│   ├── .env.example                # 🧩 Variáveis de ambiente (exemplo)
│   ├── Dockerfile                  # 🐳 Build do frontend
│   ├── next.config.ts              # ⚙️ Configuração do Next.js
│   ├── tailwind.config.ts          # 🎨 Configuração do Tailwind
│   ├── /public                     # 📂 Arquivos estáticos
│   └── /src
│       ├── /app                    # 📄 App Router (Next.js 15)
│       │   ├── /(auth)             # 🔐 Rotas de autenticação
│       │   ├── /dashboard          # 📊 Painel administrativo
│       │   ├── /receitas           # 🧾 Ficha técnica e precificação
│       │   ├── /pedidos            # 📋 Gestão de pedidos
│       │   ├── /kds                # 🖥️ Painel KDS (cozinha)
│       │   └── /estoque            # 📦 Gestão de insumos e estoque
│       ├── /components             # 🧱 Componentes reutilizáveis
│       ├── /hooks                  # 🎣 Hooks personalizados (useSocket, usePedidos)
│       ├── /services               # 🔌 Chamadas HTTP (axios)
│       ├── /store                  # 🗃️ Estado global (Zustand)
│       └── /utils                  # 🛠️ Funções utilitárias (formatCurrency, etc.)
│
├── /backend                        # 📁 API Express + Node.js
│   ├── .env.example                # 🧩 Variáveis de ambiente (exemplo)
│   ├── Dockerfile                  # 🐳 Build do backend
│   ├── /prisma
│   │   ├── schema.prisma           # 🗄️ Schema do banco de dados
│   │   ├── /migrations             # 📜 Histórico de migrações
│   │   └── seed.ts                 # 🌱 Dados iniciais (insumos por segmento)
│   └── /src
│       ├── server.ts               # 🚀 Entry point (Express + Socket.IO)
│       ├── /routes                 # 🛣️ Definição das rotas REST
│       ├── /controllers            # 🎮 Handlers das requisições HTTP
│       ├── /services               # ⚙️ Lógica de negócio (PrecificacaoService, etc.)
│       ├── /repositories           # 🗄️ Acesso a dados via Prisma
│       ├── /middlewares            # 🛡️ Auth JWT, validação, tratamento de erros
│       ├── /dto                    # ✉️ Data Transfer Objects (Zod schemas)
│       └── /websocket              # 📡 Handlers do Socket.IO (KDS em tempo real)
│
└── /scripts                        # 📜 Scripts de automação
    ├── dev.sh                      # 🚀 Sobe ambiente completo de desenvolvimento
    └── deploy.sh                   # ☁️ Deploy em produção
```

---

## 🎥 Demonstração

### 🌐 Aplicação Web

| Tela | Captura de Tela |
| :---: | :---: |
| **Tela de Login / Onboarding** | **Dashboard Principal** |
| <img src="./docs/img/screen_login.png" alt="Tela de Login" width="320px"> | <img src="./docs/img/screen_dashboard.png" alt="Dashboard" width="320px"> |
| **Ficha Técnica & Precificação** | **Painel KDS (Cozinha)** |
| <img src="./docs/img/screen_ficha_tecnica.png" alt="Ficha Técnica" width="320px"> | <img src="./docs/img/screen_kds.png" alt="Painel KDS" width="320px"> |
| **Lista de Compras Automatizada** | **Gestão de Pedidos** |
| <img src="./docs/img/screen_lista_compras.png" alt="Lista de Compras" width="320px"> | <img src="./docs/img/screen_pedidos.png" alt="Pedidos" width="320px"> |

### 💻 Exemplo de Saída no Terminal (API)

```bash
# Buscar ficha técnica de um produto com custo calculado
curl -X GET 'http://localhost:3001/api/v1/produtos/1/ficha-tecnica' \
     -H 'Authorization: Bearer <seu-jwt-token>'
```

**Saída Esperada:**

```json
{
  "produto": {
    "id": 1,
    "nome": "Bolo de Pote Ninho",
    "rendimento": 10
  },
  "custoTotal": 4.50,
  "custoPorUnidade": 0.45,
  "precoVenda": 15.00,
  "margemLucro": 70.0,
  "ingredientes": [
    { "insumo": "Leite Condensado (Moça 395g)", "qtdUsada": "197.5g", "custoProporcional": 1.75 },
    { "insumo": "Creme de Leite (200g)", "qtdUsada": "100g", "custoProporcional": 0.90 },
    { "insumo": "Biscoito Maisena (400g)", "qtdUsada": "80g", "custoProporcional": 0.64 }
  ]
}
```

---

## 🧪 Testes

### Testes Unitários e de Integração

```bash
# Back-end
cd backend
npm run test

# Front-end
cd frontend
npm run test
```

*Ferramentas utilizadas: **Jest** (backend) + **React Testing Library** (frontend).*

### Testes End-to-End (E2E)

```bash
npm run test:e2e
```

*Ferramenta utilizada: **Playwright** — cobre os fluxos críticos: cadastro de receita, criação de pedido e atualização de status no KDS.*

---

## 🔗 Documentações Utilizadas

* 📖 **Framework (Front-end):** [Documentação Oficial do Next.js](https://nextjs.org/docs)
* 📖 **Biblioteca UI:** [Documentação Oficial do React](https://react.dev/reference/react)
* 📖 **ORM:** [Documentação do Prisma](https://www.prisma.io/docs)
* 📖 **Banco de Dados:** [Documentação do PostgreSQL 16](https://www.postgresql.org/docs/16/)
* 📖 **WebSocket:** [Documentação do Socket.IO](https://socket.io/docs/v4/)
* 📖 **Estilização:** [Documentação do Tailwind CSS](https://tailwindcss.com/docs)
* 📖 **Containerização:** [Documentação do Docker](https://docs.docker.com/)
* 📖 **Diagramas UML:** [PlantUML — Guia de Referência](https://plantuml.com/guide)
* 📖 **Pagamentos:** [Documentação da API Stripe](https://stripe.com/docs/api)
* 📖 **Padrão de Commits:** [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

---

## 👥 Autores

| 👤 Nome | 🖼️ Foto | :octocat: GitHub | 💼 LinkedIn | 📤 Gmail |
|---------|----------|-----------------|-------------|-----------|
| Bernardo Gomes Pereira | <div align="center"><img src="https://via.placeholder.com/70x70/2C6E49/FFFFFF?text=EU" width="70px" height="70px"></div> | <div align="center"><a href="https://github.com/bernardogomes25"><img src="https://joaopauloaramuni.github.io/image/github6.png" width="50px" height="50px"></a></div> | <div align="center"><a href="https://www.linkedin.com/in/bernardogomespereira/"><img src="https://joaopauloaramuni.github.io/image/linkedin2.png" width="50px" height="50px"></a></div> | <div align="center"><a href="mailto:be.gpereira25@gmail.com"><img src="https://joaopauloaramuni.github.io/image/gmail3.png" width="50px" height="50px"></a></div> |

---

## 🤝 Contribuição

1. Faça um `fork` do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/minha-feature`).
3. Commit suas mudanças (`git commit -m 'feat: Adiciona nova funcionalidade X'`). **(Utilize [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/))**
4. Faça o `push` para a branch (`git push origin feature/minha-feature`).
5. Abra um **Pull Request (PR)**.

> [!IMPORTANT]
> 📝 **Regras:** Por favor, verifique o arquivo [`CONTRIBUTING.md`](./CONTRIBUTING.md) para detalhes sobre nosso guia de estilo de código e o processo de submissão de PRs.

---

## 🙏 Agradecimentos

* [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo apoio institucional e fomento às boas práticas de engenharia.
* [**Prof. Dr. João Paulo Aramuni**](https://github.com/joaopauloaramuni) — Pelos ensinamentos sobre **Arquitetura de Software**, **Padrões de Projeto** e pelo template de documentação que guiou este trabalho.
* [**Fernanda Kipper**](https://www.instagram.com/kipper.dev/) — Pelos ensinamentos em **Desenvolvimento Web** e melhores práticas de **Front-end**.
* [**Rodrigo Branas**](https://branas.io/) — Pela didática excepcional em **Clean Architecture** e **Clean Code**.

---

## 📄 Licença

Este projeto é distribuído sob a **[Licença MIT](LICENSE)**.

---

<div align="center">
  <sub>Feito com 🍰 para confeiteiros que merecem lucrar de verdade.</sub>
</div>
