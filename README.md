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

# AgilDev - Automações & I.A — AI Content Automation Pipeline

Pipeline de automação de conteúdo baseado em IA, desenvolvido para estruturar, gerar, renderizar e encaminhar conteúdos para aprovação de forma automatizada.

## Visão geral

Este projeto automatiza parte do processo de produção de conteúdo da AgilDev - Automações & I.A.

A partir de um fluxo agendado, o sistema consulta temas utilizados anteriormente, define um novo tema, gera o roteiro do carrossel com IA, estrutura os slides, processa a renderização dos criativos e salva o conteúdo gerado para as próximas etapas do processo.

O projeto também possui um fluxo separado de aprovação, responsável por receber o novo conteúdo, validar sua origem e encaminhar os materiais para aprovação antes da distribuição.

## O problema

A produção recorrente de conteúdo envolve diversas etapas manuais: definição de pautas, criação de roteiros, organização dos slides, renderização dos criativos, armazenamento e envio para aprovação.

O objetivo deste projeto foi transformar esse processo em um pipeline reproduzível, mantendo regras de negócio e pontos de validação ao longo da execução.

## A solução

O processo foi dividido em etapas independentes:

1. Consulta do histórico de conteúdos já utilizados.
2. Seleção de um novo tema com apoio de IA.
3. Geração estruturada do roteiro do carrossel.
4. Validação e normalização da resposta da IA.
5. Processamento individual dos slides.
6. Montagem dos criativos utilizando HTML e CSS.
7. Renderização dos slides.
8. Geração da legenda.
9. Persistência dos dados no histórico.
10. Encaminhamento do conteúdo para aprovação.
