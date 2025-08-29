# 🚗 Modelo Preditivo de Preços de Carros

## 🎯 Problema de Negócio

No mercado de carros usados, definir um preço justo e competitivo é um desafio tanto para vendedores quanto para compradores. A precificação incorreta pode levar a longos períodos de venda ou a perdas financeiras significativas. Este projeto visa resolver esse problema utilizando dados para prever o Preço de Venda Sugerido pelo Fabricante (MSRP) de um veículo.

## 💡 Solução

Este projeto implementa um modelo de **Regressão Linear** para estimar o preço de um carro com base em suas características, como ano, marca, modelo, potência do motor e quilometragem. O fluxo de trabalho abrange desde a limpeza e análise exploratória dos dados até a engenharia de features e a avaliação rigorosa do modelo, demonstrando um ciclo de vida completo de um projeto de ciência de dados.

O objetivo final é fornecer uma ferramenta baseada em dados que possa capacitar os usuários a tomar decisões de precificação mais informadas.

## 🛠️ Tecnologias Utilizadas

- **Python**
- **Pandas** para manipulação e análise de dados.
- **NumPy** para operações numéricas.
- **Matplotlib** e **Seaborn** para visualização de dados.
- **Scikit-learn** para pré-processamento, treinamento e avaliação do modelo.
- **Jupyter Notebook** como ambiente de desenvolvimento.

## 📈 Metodologia

O projeto foi desenvolvido seguindo as melhores práticas de um fluxo de trabalho de ciência de dados:

1.  **Limpeza e Pré-processamento dos Dados:** Carregamento do dataset, padronização dos nomes das colunas, tratamento de valores ausentes através de imputação (média para numéricos, moda para categóricos) e codificação de variáveis categóricas com One-Hot Encoding.

2.  **Análise Exploratória de Dados (EDA):** Análise aprofundada para entender a distribuição das variáveis, com foco especial na variável alvo (MSRP). Foi identificada uma distribuição com cauda longa, que foi normalizada usando uma transformação logarítmica (`log1p`) para melhorar o desempenho do modelo.

3.  **Engenharia de Features:** Criação de novas features a partir das existentes para capturar relações mais complexas nos dados. Foram testadas features como `Engine HP Squared`, `Engine HP Log` e `Popularity per HP`, resultando em uma melhora significativa na performance do modelo.

4.  **Treinamento e Avaliação do Modelo:** Os dados foram divididos em conjuntos de treino (80%) e teste (20%). Um modelo de Regressão Linear foi treinado e avaliado utilizando múltiplas métricas para garantir uma compreensão completa de seu desempenho.

## 📊 Resultados

O modelo foi avaliado com base em três métricas principais. A engenharia de features demonstrou um impacto positivo, melhorando a capacidade preditiva do modelo inicial.

| Métrica | Modelo Inicial | Modelo com Engenharia de Features |
| :--- | :---: | :---: |
| **R-quadrado (R²)** | 0.62 | **0.78** |
| **Erro Quadrático Médio (MSE)** | 0.45 | **0.29** |
| **Erro Absoluto Médio (MAE)**| 0.38 | **0.21** |

A visualização da distribuição dos preços previstos versus os preços reais confirmou a eficácia do modelo final.

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Python 3.7+
- Jupyter Notebook ou uma IDE compatível (ex: VS Code com a extensão Jupyter)

### Instalação e Execução

1.  **Clone o repositório:**

    ```bash
    git clone [https://github.com/Raimundoivy/CarPricePredictionUsingLinearRegression.git](https://github.com/Raimundoivy/CarPricePredictionUsingLinearRegression.git)
    cd CarPricePredictionUsingLinearRegression
    ```

2.  **Instale as dependências:**

    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib
    ```

3.  **Baixe o Conjunto de Dados:**

    - Faça o download do arquivo `data.csv` do Kaggle (ou da fonte original).
    - **Importante:** Coloque o arquivo `data.csv` na raiz do diretório do projeto.

4.  **Execute o Notebook:**
    Inicie o Jupyter Notebook e abra o arquivo `car_prediction.ipynb`.

    ```bash
    jupyter notebook car_prediction.ipynb
    ```

    Execute as células sequencialmente para replicar a análise e os resultados.

## 🙏 Agradecimentos

Este projeto foi desenvolvido aplicando os conceitos e a metodologia ensinados no **Capítulo 2** do livro **"Machine Learning Bookcamp"** de Alexey Grigorev.

## 👤 Contato

**Raimundo Araújo** - [LinkedIn](https://www.linkedin.com/in/raimundoivy/)
