<p align="center">
  <a href="#">
    <img src="docs/AgilDev - Logo.jpg" alt="AgilDev Logo" width="220" />
  </a>
</p>

<h1 align="center">AgilDev — AI Content Automation Pipeline</h1>

<p align="center">
  <b>Strategy</b> &nbsp;•&nbsp; 
  <b>Generation</b> &nbsp;•&nbsp; 
  <b>Rendering</b> &nbsp;•&nbsp; 
  <b>Approval</b>
</p>

<p align="center">
  Pipeline de automação de conteúdo baseado em IA, responsável por transformar uma pauta em um carrossel estruturado, renderizado e preparado para aprovação.
</p>

<p align="center">
  <a href="https://n8n.io/"><img src="https://img.shields.io/badge/n8n-Automation-FF6D5A?style=flat-square&logo=n8n&logoColor=white" alt="n8n" /></a> &nbsp;&nbsp;
  <a href="https://openai.com/"><img src="https://img.shields.io/badge/OpenAI-LLM-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI" /></a> &nbsp;&nbsp;
  <a href="https://supabase.com/"><img src="https://img.shields.io/badge/Supabase-Database-3ECF8E?style=flat-square&logo=supabase&logoColor=white" alt="Supabase" /></a> &nbsp;&nbsp;
  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"><img src="https://img.shields.io/badge/JavaScript-Workflow%20Logic-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript" /></a>
</p>

---

## 📌 Visão Geral

Este projeto automatiza parte do processo de produção de conteúdo da **AgilDev - Automações & I.A**.

A partir de um fluxo agendado, o sistema consulta temas utilizados anteriormente, define um novo tema, gera o roteiro do carrossel com IA, estrutura os slides, processa a renderização dos criativos e salva o conteúdo gerado para as próximas etapas do processo.

O projeto também possui um fluxo separado de aprovação, responsável por receber o novo conteúdo, validar sua origem e encaminhar os materiais para aprovação antes da distribuição.

## 🎯 O Problema

A produção recorrente de conteúdo envolve diversas etapas manuais: definição de pautas, criação de roteiros, organização dos slides, renderização dos criativos, armazenamento e envio para aprovação.

O objetivo deste projeto foi transformar esse processo em um pipeline reproduzível, mantendo regras de negócio e pontos de validação ao longo da execução.

## ⚙️ A Solução

O processo foi dividido em etapas independentes:

1. Consulta do histórico de conteúdos já utilizados no banco relacional.
2. Seleção de um novo tema inédito com apoio de IA (GPT Estrategista).
3. Geração estruturada do roteiro completo do carrossel.
4. Validação e normalização da resposta da IA via código.
5. Processamento individual dos slides via looping.
6. Montagem dos criativos utilizando HTML e CSS dinâmicos.
7. Renderização automatizada dos slides em imagens.
8. Geração da legenda otimizada para engajamento.
9. Persistência dos dados e mídias geradas no histórico.
10. Encaminhamento do conteúdo via Webhook para a camada de aprovação.

---

## 🏗️ Arquitetura do Sistema

```mermaid
graph TD
    A[Cron Schedule Trigger] --> B[(Supabase: posts_historico)]
    B -->|Busca histórico| C[GPT Estrategista]
    C -->|Define novo tema| D[GPT Roteirista]
    D -->|JSON 5 Slides| E[Parse & Normalização JS]
    E --> F[Loop de Renderização HTML/CSS]
    F -->|HCTI API| G[Upload de Imagens]
    G --> H[GPT Legenda]
    H --> I[(Supabase: Salva Post Completo)]
    I -->|Webhook Trigger| J[Approval Workflow]
    J -->|Validação Secret| K[Uazapi WhatsApp API]
    K --> L[Aprovação Humana]
