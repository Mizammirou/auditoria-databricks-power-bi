# Checklist para publicar no GitHub

## Configuração do repositório

- **Nome sugerido:** `auditoria-databricks-power-bi`
- **Descrição:** `Dashboard de auditoria com dados simulados do Databricks, desenvolvido em Power BI com Power Query, DAX e modelagem dimensional.`
- **Visibilidade:** público
- **README inicial:** não é necessário criar, pois este pacote já contém `README.md`

## Tópicos sugeridos

```text
power-bi
data-analysis
databricks
business-intelligence
data-governance
dax
power-query
portfolio
```

## Antes do upload

- abrir `docs/revisao_power_bi.md`;
- corrigir o nome da medida e os títulos indicados no Power BI;
- salvar o PBIX corrigido sobre o arquivo deste pacote;
- reexportar o dashboard e substituir o PDF correspondente;
- abrir o `README.md` e conferir a visualização das imagens.

## Upload

1. Criar o repositório no GitHub.
2. Extrair o arquivo ZIP deste pacote no computador.
3. Em **Add file → Upload files**, arrastar todo o conteúdo da pasta extraída.
4. Usar a mensagem de commit: `Publica projeto de auditoria do Databricks`.
5. Confirmar se as pastas `assets`, `data` e `docs` foram mantidas.

## Conferência final

- o README aparece na página inicial;
- a imagem do dashboard é exibida;
- os links para PBIX, Excel e PDFs funcionam;
- o aviso sobre dados fictícios está visível;
- nenhum arquivo ultrapassa o limite de upload do GitHub.

