# Ensaio de Machine Learning
## Descrição
A empresa Data Money acredita que a expertise no treinamento e ajuste fino dos algoritmos, trabalhados pelos Cientistas de Dados, é o principal motivo dos ótimos resultados que as consultorias vêm entregando aos seus clientes.

## Objetivo
O objetivo desse projeto será realizar ensaios com algoritmos de Classificação, Regressão e Clusterização, para estudar a mudança de comportamento da performance, à medida que são testados diferentes valores para os principais parâmetros de controle de overfitting e underfitting.

# Planejamento da solução
## Produto final
O produto final será 8 tabelas avaliando a performance de múltiplas métricas para 3 conjuntos de dados diferentes: treinamento, validação e teste.

## Algoritmos ensaiados
### Classificação:
**Algoritmos:** KNN, Decision Tree, Random Forest e Logistic Regression.

**Métricas de performance:** Accuracy, Precision, Recall e F1-Score.

### Regressão:
**Algoritmos:** Linear Regression, Decision Tree Regressor, Random Forest Regressor, Polinomial Regression, Linear Regression Lasso, Linear Regression Ridge, Linear Regression Elastic Net, Polinomial Regression Lasso, Polinomial Regression Ridge e Polinomial Regression Elastic Net.

**Métricas de performance:** R2, MSE, RMSE, MAE e MAPE.

### Agrupamento:
**Algoritmos:** K-Means e Affinity Propagation.

**Métricas de performance:** Silhouette Score.

## Ferramentas utilizadas
Python 3.9 e biblioteca Scikit-learn.

# Desenvolvimento
## Estratégia da solução
Para ensaiar os algoritmos de Machine Learning irei escrever os códigos utilizando a linguagem Python. Para treinar cada um dos algoritmos serão testados diferentes valores para os principais parâmetros de ajuste de overfitting e assim observar o resultado final das métricas. Os valores de parâmetros que fizerem os algoritmos alcançarem a melhor performance nos dados de validação serão aqueles escolhidos para definição e uso em dados ainda não visualizados pelo algoritmo (dados de teste).

## O passo a passo
Passo 1: Divisão dos dados em treino, teste e validação.

Passo 2: Treinamento dos algoritmos com os dados de treinamento, utilizando parâmetros "default".

Passo 3: Medir a performance dos algoritmos treinados com parâmetros "default", utilizando apenas o conjunto de dados de treinamento.

Passo 4: Medir a performance dos algoritmos treinados com parâmetros "default", utilizando o conjunto de dados de validação.

Passo 5: Definir um range de valores para os principais parâmetros de controle do overfitting e treinar os algoritmos. Visualizar graficamente a alteração de performance de acordo com a
mudança de valores dos parâmetros. Definir os melhores valores para cada parâmetro a partir dos resultados das métricas sobre os dados de validação.

Passo 6: Unir os dados de treinamento e validação

Passo 7: Retreinar o algoritmo com a união dos dados de treinamento e validação, utilizando os melhores valores encontrados para os parâmetros de controle do algoritmo.

Passo 8: Medir a performance dos algoritmos treinados com os melhores parâmetros, utilizando o conjunto de dados de teste.

Passo 9: Montar as tabelas com o resultado das métricas sobre os 3 conjuntos de dados.

Passo 10: Avaliar os ensaios e anotar os 3 principais Insights que se destacaram.


# Os top 3 Insights
## Insight Top 1
A performance dos algoritmos de classificação sobre os dados de teste ficou bem próxima da performance sobre os dados de validação, o que demonstra não ter ocorrência de overfitting.
## Insight Top 2
O parâmetro de profundidade das árvores é muito importante para performance do algoritmo e o aprendizado não entrar em estado de overfitting.
## Insight Top 3
Todos os algoritmo de regressão não apresentaram boas métricas de performance, o que mostra uma necessidade de uma seleção de atributos e uma preparação melhor das variáveis independentes do conjunto de dados. As regularizações aplicadas em regressão também trazem diferenças consideráveis nos resultados.

# Resultados
## Ensaio de classificação:
### Sobre os dados de treinamento
![classificacao_treinamento](img/class_train.PNG)

### Sobre os dados de validação
![classificacao_validacao](img/class_val.PNG)

### Sobre os dados de teste
![classificacao_teste]( img/class_test.PNG)
## Ensaio de regressão:
### Sobre os dados de treinamento
![regressao_treinamento]( img/reg_train.PNG)
### Sobre os dados de validação
![regressao_validacao]( img/reg_val.PNG)
### Sobre os dados de teste
![regressao_teste]( img/reg_test.PNG)
## Ensaio de clusterização:
![clusterizacao_kmeans]( img/cluster_km.PNG)
![clusterizacao_affinity_propagation]( img/cluster_ap.PNG)

# Conclusão
Nesse Ensaio de Machine Learning adquiri experiência prática, através de testes, e consegui aprofundar o entendimento sobre o funcionamento de diversos algoritmos de classificação, regressão e clusterização. O ajuste e estudo dos hiperparâmetros de controle são fundamentais para a performance dos algoritmos estar alinhada ao problema de negócio e evitar o estado de overfitting e underfitting. A depender do objetivo de negócio deve-se trabalhar o ajuste para determinada projeção de resultados. A qualidade dos dados trabalhados em cada etapa também é determinante para os resultados.

Algoritmos baseados em árvores são sensíveis quanto à profundidade do crescimento e do número de árvores na floresta, fazendo com que a
escolha correta dos valores desses parâmetros impeçam os algoritmos de entrar no estado de overfitting.
Os algoritmos de regressão, por outro lado, são sensíveis ao grau do polinômio. Esse parâmetro controla o limite entre o estado de underfitting e overfitting desses algoritmos.

# Próximos passos
Como próximos passos desse ensaio, pretendo ensaiar novos algoritmos de Machine Learning e usar diferentes conjuntos de dados para aumentar o conhecimento sobre os algoritmos e quais cenários são mais favoráveis para o aumento da performance dos mesmos.
