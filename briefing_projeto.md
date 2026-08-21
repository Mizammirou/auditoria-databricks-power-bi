# Briefing do Projeto — Auditoria de Uso do Databricks

## Contexto

Uma empresa utiliza o Databricks em diferentes departamentos para consultar tabelas, executar notebooks e jobs e administrar clusters. Para fins de estudo, foi criada uma base fictícia que representa eventos de auditoria desse ambiente.

## Problema

Os registros isolados não oferecem uma visão rápida sobre uso, falhas e comportamentos que merecem investigação. O desafio é transformar esses eventos em indicadores e recortes compreensíveis para gestores e equipes técnicas.

## Objetivo

Desenvolver um dashboard no Power BI para:

- acompanhar utilização e falhas;
- comparar volume e taxa proporcional por departamento;
- investigar usuários, ações, objetos, clusters e horários;
- consultar eventos detalhados;
- apoiar perguntas de governança e monitoramento operacional.

## Escopo analítico

### Visão geral

- total de eventos;
- usuários com atividade;
- logins;
- falhas e taxa de falhas;
- tempo total de execução;
- distribuição por departamento e ação.

### Análise de falhas

- comparação entre departamentos;
- investigação do RH;
- detalhamento do Colaborador 37;
- distribuição por ação, objeto e cluster;
- análise dentro e fora do expediente.

### Detalhamento operacional

- consulta por departamento, usuário, status e período;
- verificação de horário, ação, objeto, cluster, duração e endereço IP simulado.

## Dados e granularidade

- base inteiramente fictícia;
- 5.000 eventos entre janeiro e julho de 2026;
- uma linha por evento de auditoria;
- modelo dimensional em esquema estrela.

## Entregáveis

- base Excel simulada;
- modelo e relatório Power BI;
- exportação do dashboard em PDF;
- carrossel para apresentação do projeto;
- README e documentação para GitHub.

## Critérios de qualidade

- KPIs reconciliados com a base;
- diferença entre volume e taxa explicitada;
- escopo dos filtros identificado em cada análise;
- achados apresentados como sinais investigativos, não como prova de incidente;
- declaração visível de que os dados são simulados.

