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

MIT License

Copyright (c) 2025 Thaís Barbosa de Oliveira

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
