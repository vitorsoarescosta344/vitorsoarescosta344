<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg">
  <img alt="Victor Soares, Backend e Plataforma" src="./assets/banner-light.svg" width="100%">
</picture>

<br><br>

<a href="https://www.linkedin.com/in/victorsoares2077/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:v.soares.costa2077@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<img src="https://img.shields.io/badge/Brasil-009C3B?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Brasil">

</div>

<br>

## Sobre

Desenvolvedor com foco em **backend e plataforma**. Passo a maior parte do tempo em API, modelagem de dados e no que roda por baixo: containers, deploy, backup e observabilidade.

O tipo de problema que mais me interessa é integração. Puxar dado de ERP legado sem expor o banco do cliente na internet, sincronizar app de campo que trabalha offline, colocar uma camada de IA em cima de sistema que nasceu em 2004 e continua rodando. Trabalho principalmente com **TypeScript** e **C# / .NET**, com **Go** onde precisa de binário único rodando na infra do cliente.

Boa parte do que construo é produto de empresa e mora em repositório privado, então a lista abaixo descreve os projetos em vez de linkar código.

<br>

## Stack

**Backend**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-14151A?style=flat-square&logo=bun&logoColor=white)
![Hono](https://img.shields.io/badge/Hono-E36002?style=flat-square&logo=hono&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)

**Front e mobile**

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![React Native](https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)
![TanStack](https://img.shields.io/badge/TanStack-FF4154?style=flat-square&logo=reactquery&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

**Dados**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white)

**Infra**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![DigitalOcean](https://img.shields.io/badge/DigitalOcean-0080FF?style=flat-square&logo=digitalocean&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)

<br>

## Projetos

### Orion

Plataforma multi-tenant que conecta o ERP do cliente a uma camada de IA conversacional.

A API central cuida de autenticação, gestão de tenants, orquestração de IA com tool calls, integração com WhatsApp e trilha de auditoria. Do outro lado tem um conector escrito em Go que roda dentro da infra do cliente. Ele executa apenas consultas definidas previamente (nunca SQL arbitrário), normaliza o resultado e manda para a API por conexão de saída, com heartbeat e fila de tasks. O banco do ERP nunca precisa ficar exposto para a internet e o cliente não abre porta nenhuma.

`Bun` · `Hono` · `Go` · `PostgreSQL` · `Redis` · `S3`

### AuditStock

Produto de auditoria e conferência de estoque físico para inventários.

Painel web em React 19 com TanStack Router e Query, Tailwind 4 e shadcn/ui, entregue como SPA estática em subpath com deploy scriptado. A API roda em C# / .NET sobre SQL Server e existe um app de coleta que acompanha o operador em campo. O produto atende um setor que trabalha com inventário desde 2004, então boa parte do desafio é caber em processo que já existe.

`React 19` · `TypeScript` · `C# / .NET` · `TanStack` · `Tailwind` · `Docker`

### QuickCount

Plataforma de contagem de inventário com app mobile e painel web.

O app em React Native com Expo faz leitura de código de barras e precisa funcionar em galpão sem sinal, então a operação é offline primeiro e sincroniza depois. O painel é React com Radix UI e Redux Toolkit, e o backend está dividido entre TypeScript e C# sobre SQL Server.

`React Native` · `Expo` · `TypeScript` · `C# / .NET` · `SQL Server`

### BetterAging

API de produto construída do zero em Bun com Hono.

Autenticação com Lucia e OAuth via Arctic, Prisma sobre PostgreSQL, busca vetorial em Qdrant para recuperação de contexto, integração com OpenAI, cobrança no Stripe, arquivos em S3, push com OneSignal e métricas expostas para Prometheus. É o projeto onde mais mexi com camada de IA em produção de verdade, com custo e latência importando.

`Bun` · `Hono` · `Prisma` · `PostgreSQL` · `Qdrant` · `Stripe` · `Prometheus`

### Quick Logger

Serviço de log centralizado para os apps que mantenho.

A API recebe eventos autenticados por API key, guarda em MongoDB e libera consulta com JWT. O painel é React com TanStack Router e Table. Nasceu de uma dor real: parar de depender de print de tela do cliente para entender o que quebrou em produção.

`Bun` · `TypeScript` · `MongoDB` · `JWT` · `React`

<br>

## Atividade

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=vitorsoarescosta344&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&hide_title=true&theme=github_dark&bg_color=00000000&text_color=8B949E&icon_color=58A6FF&title_color=E6EDF3" height="165" alt="Estatísticas do GitHub">

<br><br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/vitorsoarescosta344/vitorsoarescosta344/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/vitorsoarescosta344/vitorsoarescosta344/output/github-snake.svg">
  <img alt="Cobrinha comendo o grid de contribuições" src="https://raw.githubusercontent.com/vitorsoarescosta344/vitorsoarescosta344/output/github-snake.svg">
</picture>

</div>

<br>

<div align="center">
  <sub>Aberto a conversa sobre backend, integração de sistema legado e infraestrutura.</sub>
</div>
