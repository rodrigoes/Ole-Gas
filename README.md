# Morning Star - Case Técnico Óleo & gás

## Contexto

Este projeto foi desenvolvido como parte do processo seletivo da Morning Star.

O objetivo foi transformar uma base de dados de poços de petróleo e gás em informações gerenciais capazes de apoiar análises operacionais, geográficas e temporais relacionadas à produção de óleo e gás.

A solução foi construída utilizando Power BI para desenvolvimento dos dashboards e Python para realização da análise exploratória dos dados.

## Objetivos do Case

A proposta consistiu em:

* Realizar o tratamento e padronização da base de dados;
* Construir visualizações para análise gerencial;
* Avaliar a distribuição geográfica dos poços;
* Analisar a evolução temporal das conclusões;
* Investigar a relação entre poços Produzindo e Injetando;
* Identificar padrões relacionados a operadores, bacias e campos;
* Desenvolver uma experiência de navegação intuitiva para os usuários do dashboard.

## Estrutura do Projeto

```text

├── dashboard/
│   ├── OleoGAS.pbix
│ 
├── data/
│   └── [Case Técnico] - Tabela de Pocos.xlsx
|
├── design/
│   ├── dashboard.fig 
│   │
│   └── backgrounds/
│       ├── tab1.png 
│       ├── tab2.png 
│       └── tab3.png 
│
├── python/
│   └── analise_exploratoria_pocos.ipynb
│

└── README.md
```
## Arquivos de Design

A pasta `design` contém os arquivos utilizados na construção visual do dashboard.

- `dashboard.fig`: arquivo editável do projeto desenvolvido no Figma;
- `tab1.png`: plano de fundo da página Overview;
- `tab2.png`: plano de fundo da página Operação;
- `tab3.png`: plano de fundo da página Evolução.

O arquivo `.fig` pode ser importado e aberto no Figma para consulta, manutenção ou evolução do design do dashboard.
## Tratamento dos Dados

As seguintes transformações foram aplicadas na base:

* Limpeza de registros nulos;
* Padronização da coluna de datas;
* Tratamento de datas inválidas;
* Remoção do prefixo numérico dos identificadores dos poços;
* Criação da coluna descritiva Terra e Mar a partir dos códigos T e M;
* Tratamento dos campos textuais nulos;
* Criação da coluna de ano para análises temporais.

Os registros sem data válida foram mantidos na base, porém excluídos apenas das análises dependentes de data.

## Dashboard Power BI

O dashboard foi organizado em três áreas analíticas.

### Overview

Visão geral dos ativos cadastrados:

* Total de poços;
* Distribuição Terra x Mar;
* Distribuição por estado;
* Principais bacias;
* Principais operadores;
* Indicadores gerais da base.
<img width="998" height="562" alt="image" src="https://github.com/user-attachments/assets/9b50a943-ef71-45c3-950b-ef021fab3590" />


### Operação

Análise da situação operacional dos poços:

* Total de poços produzindo;
* Total de poços injetando;
* Total de poços produzindo e injetando;
* Total dos demais poços;
* Distribuição das situações operacionais;
* Comparativo Produzindo x Injetando;
* Distribuição operacional por bacia;
* Indicadores relacionados à estratégia de produção.
<img width="1001" height="562" alt="image" src="https://github.com/user-attachments/assets/2526e93b-f8ac-4b3f-847a-cdc2824eca0c" />



### Evolução

Análise temporal da atividade:

* Série histórica das conclusões de poços;
* Evolução das conclusões após o ano 2000;
* Análise dinâmica dos últimos cinco anos;
* Tendências de atividade ao longo do tempo.
<img width="992" height="558" alt="image" src="https://github.com/user-attachments/assets/9be81ab2-185e-462c-927b-f0e0ed3ddca1" />


## Análise Exploratória em Python

O notebook desenvolvido contempla:

* Avaliação da qualidade dos dados;
* Identificação de valores nulos;
* Distribuição geográfica dos poços;
* Distribuição por estado e bacia;
* Análise das situações operacionais;
* Comparação entre poços Produzindo e Injetando;
* Evolução temporal das conclusões;
* Identificação de tendências recentes.

## Ferramentas Utilizadas

* Power BI
* Python
* Pandas
* Matplotlib
* Jupyter Notebook
* Figma

## Principais Insights

A análise permitiu observar:

* Predominância de poços terrestres na base analisada;
* Concentração operacional em determinadas bacias e estados;
* Forte participação da Petrobras entre os operadores;
* Maior quantidade de poços Produzindo em relação aos Injetando;
* Evidências de mudanças no ritmo de conclusão de poços ao longo dos anos;
* Distribuição geográfica concentrada em regiões historicamente relevantes para a indústria de óleo e gás.
