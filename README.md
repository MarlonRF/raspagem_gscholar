# Raspagem de dados G Scholar

Jupyter Notebook com passo a passo para raspagem de dados do Google Scholar.


__Input:__ lista de nomes dos pesquisadores, em arquivo formato xls(Excel) ou planilha do Google Sheet.

__Ouput:__ duas tabelas com os dados, para xls ou Google Sheet. Primeira tabela com dados dos profiles dos pesquisadores, e a segunda tabela com dados das publicações dos pesquisadores.

## Proxy

Para usar servidor proxy, executar o notebook localmente, ou seja, baixar o notebookna sua máquina, fora do COLAB.

Único serviço de proxy que funcionou foi o Scraper API. Cadastro é gratuito, com limite de 1000 acessos ao mês por conta. Esse limite parece fictício.
A classe ScraperAPI já está incluída na parte de funções no notebook.

Basta adicionar o código abaixo no notebook antes de fazer qualquer raspagem.

Lembre-se de pegar o token no Site do Scraper API e substituir na 2ª linha deste código.

```python
pg = ProxyGenerator()
pg = ScraperAPI('token do site do ScraperAPI')
scholarly.use_proxy(pg)
scholarly.set_timeout(120)
```
