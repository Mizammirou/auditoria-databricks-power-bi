# Auditoria de Uso do Databricks com Power BI

Projeto de portfólio desenvolvido para simular o monitoramento de eventos de auditoria em um ambiente Databricks.

A solução transforma uma base fictícia de logs em indicadores e análises sobre utilização, falhas, usuários, ações, objetos, clusters e horários de acesso.

> **Transparência:** todos os dados são fictícios e foram criados exclusivamente para estudo. Não houve conexão com o Databricks nem extração de logs reais da plataforma.

![Visão geral do dashboard](./assets/dashboard_visao_geral.png)

## Problema de negócio

Gestores e equipes técnicas precisam de uma visão centralizada para acompanhar o uso da plataforma, identificar falhas e direcionar investigações.

O projeto busca responder perguntas como:

- quantos usuários utilizaram o ambiente;
- quais departamentos e ações concentraram mais eventos;
- onde ocorreu o maior volume e a maior taxa proporcional de falhas;
- quais usuários, objetos e clusters aparecem nos recortes investigados;
- quantos eventos ocorreram dentro e fora do expediente;
- quais registros precisam ser consultados em uma investigação detalhada.

## Objetivo

Construir um dashboard no Power BI com três níveis de análise:

1. **Visão geral:** KPIs executivos e panorama por departamento e ação;
2. **Análise de falhas:** investigação por departamento, usuário, ação, objeto, cluster e faixa de expediente;
3. **Detalhamento:** consulta dos eventos com filtros por departamento, usuário, status e período.

## Base de dados

- 5.000 eventos simulados;
- 44 usuários com atividade no período;
- 8 departamentos;
- período de janeiro a julho de 2026;
- ações como Login, Read Table, Run Notebook, Execute Job e Create Cluster;
- granularidade: cada linha da tabela fato representa um evento individual de auditoria.

## Modelagem

O modelo foi organizado em esquema estrela:

- **F_AuditLogs:** eventos individuais;
- **DimDate:** calendário;
- **DimUser:** usuários;
- **DimDepartment:** departamentos;
- **DimAction:** ações executadas;
- **DimObject:** notebooks, tabelas, views e jobs;
- **DimCluster:** clusters e ambientes;
- **DimStatus:** sucesso ou falha.

## KPIs reconciliados

| Indicador | Resultado |
| --- | ---: |
| Total de eventos | 5.000 |
| Usuários com atividade | 44 |
| Total de logins | 588 |
| Total de falhas | 257 |
| Taxa de falhas | 5,14% |
| Tempo total de execução | 299,53 horas |

Os valores acima foram conferidos diretamente na base disponibilizada neste repositório.

## Principais achados

### Visão geral

- **BI** apresentou o maior volume de eventos: 898;
- **BI** também teve o maior número absoluto de falhas: 46;
- **RH** apresentou a maior taxa proporcional de falhas: 6,05%;
- portanto, volume absoluto e taxa proporcional apontam para departamentos diferentes.

### Investigação do RH

- o RH registrou 30 falhas;
- 19 ocorreram dentro do expediente e 11 fora dele;
- o Colaborador 37 concentrou 11 falhas, o maior número entre os usuários do departamento.

### Recorte do Colaborador 37

- Read Table foi a ação com mais falhas: 4;
- `tb_funcionarios` foi o objeto mais afetado: 6;
- Cluster DEV e Cluster PROD tiveram 3 falhas cada;
- 3 ocorrências não tinham cluster associado, comportamento esperado para ações que não utilizam esse recurso.

> Os achados descrevem padrões na base simulada. Eles orientam uma investigação, mas não demonstram, por si só, incidente de segurança ou causa-raiz.

## Ferramentas e competências

- Power BI;
- Power Query;
- DAX;
- Excel;
- modelagem dimensional;
- análise exploratória e diagnóstica;
- validação de métricas;
- comunicação e storytelling com dados.

## Estrutura do repositório

```text
auditoria-databricks-power-bi/
├── README.md
├── Auditoria_Databricks.pbix
├── assets/
│   ├── dashboard_visao_geral.png
│   ├── dashboard_analise_falhas.png
│   └── dashboard_detalhamento.png
├── data/
│   └── base_auditoria_databricks.xlsx
└── docs/
    ├── briefing_original.pdf
    ├── briefing_projeto.md
    ├── carrossel_linkedin_auditoria_databricks.pdf
    ├── dashboard_auditoria_databricks.pdf
    ├── dicionario_dados.md
```

## Arquivos principais

- [Arquivo Power BI](./Auditoria_Databricks.pbix)
- [Base simulada](./data/base_auditoria_databricks.xlsx)
- [Exportação do dashboard](./docs/dashboard_auditoria_databricks.pdf)
- [Carrossel revisado](./docs/carrossel_linkedin_auditoria_databricks.pdf)
- [Briefing revisado](./docs/briefing_projeto.md)
- [Dicionário de dados](./docs/dicionario_dados.md)


## Limitações

- os dados foram gerados para fins educacionais;
- os indicadores não representam o funcionamento completo dos logs de auditoria do Databricks;
- o dashboard apoia monitoramento e investigação, mas não substitui controles de segurança, alertas ou auditoria formal;
- a página de análise utiliza recortes diferentes para RH e Colaborador 37; os títulos devem indicar claramente o escopo de cada visual.

## Autor

**Mizammirou Issifou**

Projeto desenvolvido para estudo e portfólio em Análise de Dados.

