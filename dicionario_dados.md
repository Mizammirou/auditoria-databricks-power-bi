# Dicionário de Dados

## Tabela fato — F_AuditLogs

| Campo | Descrição |
| --- | --- |
| EventID | Identificador único do evento |
| EventTime | Data e hora do evento |
| DateID | Chave de relacionamento com a dimensão de data |
| UserID | Chave do usuário |
| DepartmentID | Chave do departamento |
| ActionID | Chave da ação executada |
| ObjectID | Chave do objeto associado, quando aplicável |
| ClusterID | Chave do cluster associado, quando aplicável |
| StatusID | Situação do evento: sucesso ou falha |
| DurationSeconds | Duração simulada do evento em segundos |
| IPAddress | Endereço IP fictício do evento |
| FaixaExpediente | Classificação dentro ou fora do expediente |

## Dimensões

| Tabela | Conteúdo |
| --- | --- |
| DimDate | Data, ano, mês, trimestre, dia da semana e final de semana |
| DimUser | Nome fictício, e-mail fictício, cargo, departamento e status |
| DimDepartment | Departamentos da empresa simulada |
| DimAction | Tipos de ação registrados |
| DimObject | Notebooks, tabelas, views e jobs |
| DimCluster | Clusters e respectivos ambientes |
| DimStatus | Sucesso ou falha |

## Regras de interpretação

- campos de objeto ou cluster podem ficar vazios quando a ação não utiliza esses elementos;
- “usuários ativos” no dashboard significa usuários distintos com pelo menos um evento no período, não necessariamente usuários com cadastro marcado como ativo;
- taxa de falhas é calculada como falhas divididas pelo total de eventos no mesmo contexto de filtro;
- tempo total corresponde à soma de `DurationSeconds`, convertida para horas.

