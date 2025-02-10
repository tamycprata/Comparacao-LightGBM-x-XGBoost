# Comparacao-LightGBM-x-XGBoost
# Previsão de Renda com Machine Learning

## Descrição

Este projeto tem como objetivo construir uma máquina preditiva que, a partir de dados históricos, faça a previsão da renda de colaboradores de uma empresa. 

Utilizamos algoritmos de Machine Learning, especificamente XGBoost e LightGBM, para treinar modelos capazes de classificar indivíduos em diferentes faixas de renda. O projeto inclui etapas de pré-processamento dos dados, treinamento dos modelos e avaliação do desempenho.

## Dataset

O dataset utilizado é o "Adult" da UCI, disponível em: [http://archive.ics.uci.edu/ml/datasets/Adult](http://archive.ics.uci.edu/ml/datasets/Adult). 

Este dataset contém informações sobre idade, escolaridade, estado civil, ocupação, etc., de indivíduos adultos, juntamente com a informação sobre a renda (acima ou abaixo de 50k).

## Análise dos Dados

A análise dos dados está representada no arquivo Analise dos Dados.ipynb. E consolidado no arqivo Registro da Análise e  Limpeza dos dados.

## Pré-processamento

As seguintes etapas de pré-processamento foram realizadas:

* Remoção de linhas duplicadas.
* Codificação de variáveis categóricas usando OneHotEncoder.
* Transformação da variável alvo "salary" em valores numéricos (0 e 1).
* Divisão dos dados em conjuntos de treino e teste.

## Modelos

Foram treinados dois modelos de Machine Learning:

* **XGBoost:** Um algoritmo de boosting baseado em árvores de decisão, conhecido por sua alta performance e eficiência.
* **LightGBM:** Outro algoritmo de boosting baseado em árvores de decisão, com foco em velocidade e menor uso de memória.

## Avaliação

Os modelos foram avaliados com base nas seguintes métricas:

* **Acurácia:** Mede a proporção de previsões corretas em relação ao total de previsões.
* **ROC AUC Score:** Mede a capacidade do modelo de distinguir entre as classes, considerando a taxa de verdadeiros positivos e a taxa de falsos positivos em diferentes thresholds.

## Resultados
Essas metricas foram obtidas SEM limpeza dos dados. Essa execução está em ML_Comparacao LightGBM e XGBoost.ipynb.
| Métrica | XGBoost | LightGBM |
|---|---|---|
| Acurácia | 82.30% | 82.20%	 |
| ROC AUC Score | 78.92% | 79.16% |
| Tempo de Execução |  0:00:01.024304 | 0:00:00.240119 |

Essas métricas foram obtidas COM a limpeza dos dados. Essa execução está em ML_Comparacao LightGBM e XGBoost v2.ipynb.
| Métrica | XGBoost | LightGBM |
|---|---|---|
| Acurácia | 86.04% | 86.15% |
| ROC AUC Score | 69.92%	 | 69.67%	 |
| Tempo de Execução |  00:00:00.456402 | 00:00:00.318086 |


## Conclusões

O LightGBM apresentou um desempenho levemente superior em termos de acurácia e ROC AUC Score, além de ser consideravelmente mais rápido que o XGBoost para treinar o modelo. Portanto, para este problema específico, o LightGBM seria a escolha preferida.

## Próximos Passos

* Explorar hiperparâmetros para otimizar ainda mais o desempenho dos modelos.
* Avaliar outras métricas, como precisão, recall e F1-score.
* Realizar uma análise mais aprofundada dos erros dos modelos.
* Explorar técnicas para melhorar a interpretabilidade do modelo.


## Como Executar

1. Instale as bibliotecas necessárias: `pip install pandas scikit-learn xgboost lightgbm`
2. Faça o download do dataset "Adult" da UCI e salve-o como `adult.data`.
3. Execute o código Python do projeto.

## Autor

Tamy Prata
