
# Extração de dados para criação de datasets de bairros, distritos e povoados do Brasil

Este repositório contém um notebook que realiza a coleta de dados de bairros, distritos e povoados do Brasil utilizando uma abordagem combinada entre a API do IBGE e OpenStreetMap, e bibliotecas de geoprocessamento como `osmnx` e `geopandas`.

## Entendendo o problema

Uma extração de dados utilizando a API do SIDRA, do IBGE, retorna cerca de 14.320 bairros e distritos para um total de 5.570 municípios. Ou seja, apenas 2,57 bairros por cidade. Esta abordagem mista, por outro lado, conseguiu extrair um número significativamente maior de bairros, povoados e distritos, totalizando 46.350 bairros, povoados e distritos (uma média de 8,32 bairros por municípios, 3,23x mais que o retornado pela API SIDRA), proporcionando uma visão mais abrangente das áreas urbanas e rurais no Brasil.

## Download (Kaggle)
Os datasets (um para cada estado e outro completo para todo Brasil está disponível no link abaixo, no Kaggle:
[Bairros, Povoados e Distritos do Brasil (Download dos Datasets)](https://www.kaggle.com/datasets/itallonardi/bairros-povoados-e-distritos-do-brasil)

## Requisitos

Para rodar o notebook, você precisará das seguintes bibliotecas:

- osmnx
- geopandas
- requests
- pandas

Você pode instalar essas bibliotecas usando o seguinte comando:

```bash
pip install osmnx geopandas requests pandas
```

## Como usar

1. Clone o repositório:
  ```bash
  git clone https://github.com/itallonardi/bairrosEDistritosdoBrasil.git
   ```
2. Navegue até o diretório do repositório:
  ```bash
  cd bairrosEDistritosdoBrasil
  ```
3. Abra o notebook Jupyter:
  ```bash
  jupyter notebook bairrosEDistritosDoBrasil.ipynb
  ```
4. Execute o notebook célula por célula para coletar e processar os dados.

Ou acesse o Jupyter notebook no Google Colab: [bairrosEDistritosdoBrasil no Google Colab](https://colab.research.google.com/drive/1FEHfKJtn7a8BP9PF_vko4Km7KxNn9hT7?usp=sharing)

## Estrutura dos dados

Os datasets gerados serão salvos na pasta `csv` com o padrão de nomenclatura `data_BR_UF_cidade.csv`, onde `UF` e `cidade` podem ser substituídos pela sigla do estado e o nome da cidade, respectivamente, ou `*` representando todos. Por exemplo:
- `data_BR_BA_*.csv` (todas as cidades da Bahia)
- `data_BR_*.csv` (todos os estados e cidades do Brasil)

## Autor

Este projeto foi desenvolvido por Itallo Nardi.

## Licença

Este projeto está licenciado sob a licença MIT.
