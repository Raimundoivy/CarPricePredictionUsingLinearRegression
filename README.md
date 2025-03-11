## Previsão de Preço de Carros com Regressão Linear

## Descrição

Este projeto centra-se na previsão do Preço de Venda ao Público Sugerido pelo Fabricante (Manufacturer's Suggested Retail Price - MSRP) de carros, utilizando um modelo de regressão linear. A análise engloba a exploração de dados, pré-processamento, engenharia de atributos, treino do modelo e avaliação. O projeto é implementado num script Jupyter Notebook (`car_prediction.ipynb`).

## Instalação

Este projeto requer as seguintes bibliotecas Python:

*   pandas
*   numpy
*   scikit-learn
*   seaborn
*   matplotlib

Instale estas dependências utilizando o `pip`:

```bash
pip install pandas numpy scikit-learn seaborn matplotlib
```

### Conjunto de Dados

Descarregue o arquivo `data.csv`. O script assume que os dados estão localizados em `C:\Users\Raimu\PastaMain\Documentos\car_prediction_linear_sklearn\data.csv`. Certifique-se de que este caminho existe e é acessível, ou modifique o caminho do arquivo dentro do script `car_prediction.ipynb` para corresponder à localização do seu conjunto de dados.

## Utilização

O script `car_prediction.ipynb` executa todo o fluxo de trabalho. Ele está estruturado conceptualmente como um Jupyter Notebook, com "células" a executar tarefas específicas. Para executar o script:

1.  **Instalar Dependências:** Certifique-se de que todas as bibliotecas necessárias estão instaladas (ver "Instalação").
2.  **Obter o Conjunto de Dados:** Descarregue `data.csv` e coloque-o no diretório correto (ou atualize o caminho do arquivo no script).
3.  **Executar o Script:** Execute o script Python a partir da sua IDE :)

## Guia Passo-a-Passo do Script e Saída Esperada

O script executa os seguintes passos, organizados conceptualmente como "células":

**Células 1 e 2: Importar Bibliotecas e Carregar Dados**

*   **Importações:** pandas, numpy, scikit-learn, seaborn, matplotlib.
*   **Carrega:** O conjunto de dados de carros a partir do arquivo CSV.
*   **Define:** As colunas de atributos iniciais.

**Célula 3: Visão Geral Básica dos Dados**

*   **Imprime:**
    *   Formato do conjunto de dados (linhas, colunas).
    *   Primeiras 5 linhas dos dados.
    *   Tipos de dados de cada coluna.
    *   Contagens de valores em falta por coluna.
    *   Estatísticas descritivas (numéricas e categóricas).

**Células 4 e 5: Análise Univariada - MSRP**

*   **Visualiza a distribuição do MSRP:**
    *   Histograma e gráfico KDE do MSRP bruto.
    *   Histograma e gráfico KDE do MSRP transformado em log (`np.log1p`).

**Célula 6: Análise Univariada - Atributos Numéricos**

*   **Gera:** Histogramas e gráficos KDE para: `'Year'`, `'Engine HP'`, `'Engine Cylinders'`, `'highway MPG'`, `'city mpg'`, `'Popularity'`.

**Célula 7: Análise Multivariada - Correlação**

*   **Cria:** Um mapa de calor de correlação (atributos numéricos vs. MSRP).

**Células 8-10: Pré-processamento de Dados**

*   **Trata valores em falta:**
    *   Atributos numéricos: Imputação pela média.
    *   Atributos categóricos: Imputação pelo valor mais frequente (moda).
*   **Executa:** Codificação one-hot em atributos categóricos.

**Células 11-13: Divisão de Dados**

*   **Divide os dados:** 80% treino, 20% teste (`train_test_split`).
*   **Trata:** Potenciais discrepâncias de colunas (codificação one-hot).

**Células 14 e 15: Treino e Avaliação do Modelo**

*   **Treina:** Um modelo `LinearRegression`.
*   **Faz:** Previsões no conjunto de teste.
*   **Avalia e imprime:**
    *   Erro Quadrático Médio (MSE)
    *   R-quadrado (R2)
    *   Erro Absoluto Médio (MAE)

**Célula 16: Distribuição Real vs. Prevista**

*   **Exibe:** Um histograma: MSRP Real vs. MSRP Previsto.

**Células 17-19: Engenharia de Atributos e Retreino - 'Engine HP Squared'**

*   **Cria:** Atributo `'Engine HP Squared'`.
*   **Retreina e reavalia:** O modelo (imprime MSE, R-quadrado, MAE).
*   **Exibe:** Histograma atualizado de MSRP real vs. previsto.
*   **Imprime:** As primeiras 5 linhas e informações sobre as colunas do dataframe de treino atualizado.

**Células 20-22: Engenharia de Atributos e Retreino - Log e Rácio**

*   **Cria:** Atributos `'Engine HP Log'` (`log + 1`) e `'Popularity per HP'`.
*   **Retreina e reavalia:** O modelo (imprime MSE, R-quadrado, MAE).
*   **Exibe:** Histograma atualizado de MSRP real vs. previsto.
*   **Imprime:** As primeiras 5 linhas e informações sobre as colunas do dataframe de treino atualizado.

### Saída do Console:

*   Resumos do Dataframe (formato, cabeçalho, dtypes, valores em falta, describe).
*   Métricas de avaliação (MSE, R-quadrado, MAE) para os modelos inicial e modificado.
*   Tabela formatada representando as primeiras 5 linhas do dataframe atualizado, juntamente com informações sobre cada uma das colunas.

### Gráficos:

*   Histogramas: MSRP (bruto e transformado em log).
*   Histogramas: Atributos numéricos individuais.
*   Mapa de calor de correlação.
*   Histogramas: MSRP Real vs. Previsto (inicial e após engenharia de atributos).

## Dependências

*   pandas
*   numpy
*   scikit-learn
*   seaborn
*   matplotlib
    *   *(Versões específicas não foram rastreadas; versões recentes devem funcionar.)*
