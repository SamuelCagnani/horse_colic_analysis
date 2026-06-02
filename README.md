# Horse Colic Analysis

Autor: Samuel de Mello Cagnani

Trabalho Prático II da disciplina de Inteligência Artificial.

## Descrição

Este projeto tem como objetivo realizar o pré-processamento, análise exploratória de dados e modelagem preditiva utilizando a base de dados Horse Colic, disponibilizada pelo UCI Machine Learning Repository.

A base contém informações clínicas de cavalos diagnosticados com cólica, incluindo atributos fisiológicos, resultados de exames e informações sobre tratamentos realizados. O conjunto de dados apresenta atributos numéricos e categóricos, além de uma quantidade significativa de valores ausentes, tornando-o adequado para estudos de pré-processamento de dados e aprendizado de máquina.

## Objetivos

* Realizar análise exploratória dos dados;
* Identificar e tratar valores ausentes;
* Aplicar técnicas de limpeza e transformação de dados;
* Avaliar possíveis problemas de desbalanceamento;
* Treinar e comparar modelos de aprendizado de máquina;
* Avaliar o desempenho dos modelos utilizando métricas apropriadas.

## Base de Dados

Dataset: Horse Colic

Fonte:
https://archive.ics.uci.edu/dataset/47/horse+colic

O conjunto original contém 300 instâncias para treinamento e 68 instâncias para teste, com 28 atributos relacionados ao diagnóstico e tratamento de cavalos com cólica.

## Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

## Estrutura do Projeto

```text
horse-colic-project/
│
├── data/
│   ├── horse-colic.data
│   ├── horse-colic.test
│   └── horse-colic.names
│
├── notebooks/
│   └── horse_colic_analysis.ipynb
│
├── requirements.txt
├── .gitignore
└── README.md
```
