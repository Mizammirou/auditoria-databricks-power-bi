# Revisão recomendada antes da publicação final do PBIX

Os dados e KPIs principais foram reconciliados. Os ajustes abaixo são de nomenclatura e clareza de escopo dentro do Power BI Desktop.

## 1. Corrigir o nome de uma medida

No modelo, a medida aparece como `Totral de Falhas`.

Renomear para:

```text
Total de Falhas
```

Confirmar que os cartões e gráficos continuam funcionando após a alteração.

## 2. Explicitar o escopo dos gráficos da página “Análise de Falhas”

Os dois primeiros visuais utilizam o recorte do RH, enquanto os três visuais seguintes utilizam RH + Colaborador 37.

Títulos recomendados:

- `Falhas por usuário — RH`;
- `Falhas por faixa de expediente — RH`;
- `Falhas por ação — Colaborador 37`;
- `Falhas por objeto — Colaborador 37`;
- `Falhas por cluster — Colaborador 37`.

## 3. Ajustar a conclusão da página

Texto recomendado:

> O RH apresentou a maior taxa proporcional de falhas: 6,05%, totalizando 30 ocorrências. Dessas, 19 aconteceram dentro do expediente e 11 fora dele. Dentro do RH, o Colaborador 37 concentrou 11 falhas. Em seu recorte, Read Table foi a ação mais frequente, `tb_funcionarios` foi o objeto mais afetado e os clusters DEV e PROD lideraram entre os eventos com cluster identificado.

## 4. Reexportar o dashboard

Após os ajustes:

1. salvar o PBIX;
2. exportar novamente as três páginas para PDF;
3. substituir `docs/dashboard_auditoria_databricks.pdf` no repositório;
4. confirmar se os títulos permanecem legíveis na exportação.

