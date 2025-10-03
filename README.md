# aps-veredas
Este repositório contém scripts em **R** para geração automatizada de notas técnicas da **Atenção Primária à Saúde (APS)**.  
O objetivo é preencher um template em R Markdown com informações de municípios (extraídas de planilhas Excel) e gerar relatórios formatados em **Word**.

---

## 📂 Estrutura do projeto
---

## 🚀 Como usar

### Pré-requisitos
Instale os pacotes necessários:

```r
install.packages(c(
  "flextable", "readxl", "dplyr", "glue", 
  "pander", "openxlsx", "stringi", "stringr", "rmarkdown"
))

---
# Arquivos do R
.Rhistory
.RData
.Ruserdata
.Rproj.user/
*.Rproj

# Arquivos de saída
*.docx
*.pdf
*.html
*.Rmd
*.md
*.log
*.aux
*.out
*.toc

# Pastas temporárias
.Rcheck/
_cache/
__pycache__/
*.tmp
*.swp

# Dados locais (exemplo: Excel, CSV grandes)
*.xlsx
*.xls
*.csv
*.sav
*.dta
*.parquet
*.feather

# Resultados dos relatórios
relatorio_*.Rmd
relatorio_*.docx
relatorio_*.pdf

# Sistema operacional
.DS_Store
Thumbs.db

source("R/gerar_relatorios.R")

# Para cada linha do dataframe, será gerado um arquivo Rmd:
#   relatorio_NomeMunicipio.Rmd
rmarkdown::render("relatorio_MunicipioX.Rmd",
                  output_format = "word_document",
                  output_file = "relatorio_MunicipioX.docx")

---

📜 Licença

Este projeto está sob a licença MIT
