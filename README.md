<div align="center" style="background-color: #051d41; padding: 40px; border-radius: 10px; margin-bottom: 20px;">
  <img src="docs/AgilDev - Logo.png" alt="AgilDev Logo" width="280" />
  <h2 style="color: #ffffff; margin-top: 15px; font-family: sans-serif; font-weight: 600;">AI Content Automation Pipeline</h2>
  <p style="color: #a0aec0; font-family: sans-serif; font-size: 14px;">
    <code>Strategy</code> &nbsp;→&nbsp; <code>Generation</code> &nbsp;→&nbsp; <code>Rendering</code> &nbsp;→&nbsp; <code>Approval</code>
  </p>
</div>

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
