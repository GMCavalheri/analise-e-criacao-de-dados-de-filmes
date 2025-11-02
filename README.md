# Análise de Filmes

Este projeto tem como objetivo gerar e analisar os dados sobre filmes, utilizando dados fictícios, gerados aleatóriamente no Python. 

São gerados dois bancos de dados diferentes, um para treinar um recomendador de filmes e outro para algoritmos de aprendizado de máquina no geral.

Depois é utilizado o algoritmo de aprendizado de máquina APRIORI, para criar um recomendador de filmes, baseado nos filmes assistidos.

## Gerando os dados (Python)

A geração dos dados foi conduzida no Jupyter Notebook [`Gerador_de_banco_de_dados_filmes.ipynb`](Gerador_de_banco_de_dados_filmes.ipynb). A primeira função abaixo, gera o banco de dados para aprendizado de máquina no geral

![Python 1](/imagens/Python1.png)

A segunda função abaixo, gera o banco de dados específico para aprendizado de máquina de recomendação.

![Python 2](/imagens/Python2.png)


## Base de Dados

A base de dados utilizada para treinar o Algoritmo APRIORI, [`banco_de_dados_relacional_de_filmes.csv`](banco_de_dados_relacional_de_filmes.csv), e a base de dados geral  [`banco_de_dados_de_filmes.csv`](banco_de_dados_de_filmes.csv).


## Bibliotecas Utilizadas

As principais bibliotecas utilizadas, listadas em [`requirements.txt`](requirements.txt), são:

1. **[pandas](https://pandas.pydata.org/)** - Manipulação e análise de dados.

2. **[jupyter](https://jupyter.org/)** - Ambiente interativo para notebooks.

3. **[Numpy](https://numpy.org/)** - Funções matemáticas.

## Algoritmo de Recomendação (Python)



 Função que utiliza o banco de dados para treinar o modelo APRIORI, com os parâmetros suporte, confiança e lift:

1. Suporte é a frequência que um valor ou conjunto de valores, que aparece no banco de dados;

2. Confiança é a chance de escolher um valor, tendo escolhido outro

3. Lift é o parâmetro que diz se uma recomendação tem chance de ser escolhida

Como mostra a figura abaixo.

![Python 3](/imagens/Python3.png)


Uma vez escolhido os parâmetros da função, obtemos as seguintes relações de recomendação que podem ocorrer. Sendo o número do ID de cada filme assistido na coluna 'antecendents' e o filme recomendado, na coluna 'consequents'.

![Python 4](/imagens/Python4.png)

## Conclusões

O principal objetivo desse projeto, era criar um ambiente propício para treinar os modelos de aprendizado de máquina, que estou estudando no Mestrado e por conta própria. Até o momento, cheguei nas seguintes conclusões:

1- O algoritmo APRIORI é extremamente eficiente e escalável para uma grande quantidade de dados, tudo vai depender da precisão e da raridade das relações que queremos encontrar.

2 - É possível gerar bancos de dados bem completos e aleatórios, que podem ser personalizados para cada tipo de algoritmos de Aprendizado de Máquina.

3 - Novos algoritmos serão acrescentados no futuro e novos parâmetros para as funções geradoras de banco de dados, criando oportunidades para treinar algoritmos não supervionados de clusterização e classificação.
