# Scanner de Dados: Um Painel para Análise Inicial Rápida
Um script em Python para automatizar a Análise Exploratória de Dados (EDA) de múltiplos arquivos.
## O Problema

Todo profissional de dados conhece a rotina: ao receber um novo conjunto de dados (muitas vezes dividido em múltiplos arquivos), o primeiro passo é sempre uma **análise exploratória (EDA)** para entender sua estrutura e qualidade.  

Esse processo, embora crucial, pode ser repetitivo e demorado. É preciso verificar:

- **O número de linhas e colunas**
- **A presença de dados duplicados**
- **A quantidade e a localização de valores nulos**
- **Os tipos de dados de cada coluna para identificar inconsistências**
- **O uso de memória, especialmente em datasets grandes**

Fazer isso manualmente para cada arquivo consome um tempo valioso que poderia ser usado em análises mais profundas.

---

## A Solução

Este repositório contém uma função Python **`analisar_dataframes`**, projetada para automatizar e centralizar a etapa inicial de Análise Exploratória de Dados (EDA).  

Ela recebe uma lista de **DataFrames** e gera um **painel de controle consolidado**, permitindo uma visão geral e rápida da “saúde” de todos os seus dados de uma só vez.

---

## Principais Funcionalidades

A função gera um **DataFrame de resumo** com as seguintes informações para cada dataset analisado:

- **Estrutura Básica** — Contagem de linhas e colunas.
- **Dados Duplicados** — Quantidade de linhas completamente duplicadas.
- **Uso de Memória** — Estimativa do consumo de memória (formatado em KB ou MB).
- **Análise de Nulos**  
  - Contagem total de valores nulos.  
  - Percentual sobre o total de células.  
  - Número de colunas afetadas.  
  - Detalhamento por coluna com valores ausentes.
- **Análise de Tipos** — Resumo dos tipos de dados (`dtypes`) presentes, ajudando a identificar colunas com tipos mistos ou incorretos.

---

## Demonstração

A seguir, um exemplo do uso da função **`analisar_dataframes`** e das etapas realizadas.

### 1. Processamento dos Dados
![Processamento](img/processamento.jpeg)  
*Execução da análise e consolidação das informações em um único DataFrame de resumo.*

### 2. Definição da Função
![Definição da função](img/def.jpeg)  
*Implementação da função responsável por processar e analisar múltiplos DataFrames.*

### 3. Execução da Função
![Execução da função](img/funcao.jpeg)  
*Chamada da função passando a lista de DataFrames que serão analisados.*

### 4. Salvando o Resultado
![Salvando o resultado](img/salvando.jpeg)  
*Exportação do resultado final para um arquivo, facilitando o compartilhamento ou armazenamento.*
