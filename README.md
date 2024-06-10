# Previsão de vendas para rede de farmácias Rossmann.
## 1) Problema de Negócio
A Rossmann é uma rede de farmácias de grande porte no mercado e atua em alguns países da Europa. Por mais que haja a centralidade enquanto grupo empresarial, a dispersão de suas várias lojas traz um comportamento específico em relação ao desempenho de vendas. 
   
As gerências de cada loja encaminharam para o time de Ciência de Dados a solicitação de estimativa de vendas para as próximas 6 semanas. Ao analisar o pedido feito, o principal stakeholder do projeto foi definido: o CFO da companhia. A demanda é implementar um plano de reforma para as lojas, e para tal se faz necessário determinar o orçamento por loja dessa reforma.
  
**Objetivo:** disponibilizar a previsão de vendas por loja em tempo real para que o CFO possa tomar as melhores decisões. A partir da análise dos dados, também será desenvolvido um painel gerencial para entendimento dos principais pontos-chave do negócio.

## 2) Premissas de Negócio
* Diferentes tipos de lojas identificadas com seu próprio id. foi o modelo de negócio assumido.

* Foi definido comportamento de vendas em análise de séries temporais por se tratar de variação ao longo do tempo.

* Dias em que as lojas estão fechadas (logo, zero vendas) foram descartados por não contribuirem na previsão de vendas futuras.

* A solução será entregue diretamente ao CFO da empresa.

## 3) Estratégia de Solução
O projeto foi executado sob a metodologia de gerenciamento cíclico "Cross Industry Standard Process for Data Science" (CRISP-DS). O CRISP-DS consiste em 8 etapas que são revisitadas a cada ciclo completo, até ser definida a solução final. As principais vantagens são: elaborar uma versão end-to-end ao final de cada ciclo; ganhar velocidade na entrega de solução; e conseguir mapear junto a outros times da empresa possíveis melhorias a serem implementadas na próxima iteração.

A partir da análise e exploração dos dados, hipóteses serão mapeadas para entender melhor o funcionamento do negócio, gerar insights valiosos, definir variáveis relevantes e preparações necessárias a serem feitas nos dados. A previsão de vendas será baseada em aprender o comportamento de vendas (variável resposta) por loja, com as variáveis disponíveis, e então generalizá-lo para o futuro (6 semanas). Algoritmos de Machine Learning para regressão serão utilizados para encontrar os valores de previsão. O resultado das previsões serão avaliados por diferentes métricas e apresentado ao responsável para avaliação e definição de possíveis melhorias para o próximo ciclo.

O resultado final do projeto será entregue em:
* consulta da previsão de vendas por loja enviada em mensagem via bot no aplicativo de mensagens Telegram.
* painel gerencial online com a previsão de vendas das lojas e análise de dados gerais do negócio.

### Etapas CRISP-DS:
**1.** Entendimento de negócio:

* Recebimento de uma requisição, mapeamento dos processos, definição do problema, causa raiz, principais stakeholders e possível solução.

**2.** Coleta dos dados:

* Para esse projeto foram utilizados dados públicos, hospedados na plataforma de Kaggle.

**3.** Limpeza dos dados:

* Descrição dos dados, ordenação de colunas, verificação de dtypes, checagem e substituição de dados faltantes, descrição estatística dos dados.

**4.** Análise Exploratória dos Dados:

* Feature Engineering: criação e validação de hipóteses, criação de features, filtragem de linhas e seleção de colunas relevantes.

* Análise univariada das variáveis: comportamento das variáveis de resposta, numéricas e categóricas. 

* Análise bivariada das variáveis: relação entre uma variável e a variável resposta.

* Análise multivariada das variáveis: correlação entre as variáveis numéricas e entre as variáveis categóricas. 

**5.** Modelagem dos dados:

* Preparação dos dados: redimensionamento, encoding e transformação de variáveis.

* Seleção de variáveis: divisão do dataset em treino e validação, seleção de variáveis relevantes através do algoritmo Boruta.

**6.** Algoritmos de Machine Learning:

* Treinar 5 modelos de algoritmos de Machine Learning aplicando o cross-validation: Regressão Linear, Regressão Linear Lasso, Regressão Linear Ridge, Random Forest Regressor e XGBoost Regressor.

* Avaliar a performance dos algoritmos comparativamente com a média móvel, utilizando as métricas: MAE, MAPE, RMSE.

* Definido algoritmo XGBoost Regressor para o projeto.

* Definição dos melhores valores para os hiperparâmetros do modelo.

**7.** Avaliação do Algoritmo:

* Avaliação e interpretação do erro.

* Avaliação das performances de negócio encontradas.

* Avaliação das performances do algoritmo de Machine Learning.

**8.** Modelo em produção:

* Programar uma API do modelo e fazer o deploy em nuvem.

* Programar uma API para o bot do Telegram e fazer o deploy em nuvem.

* Fazer o painel gerencial em nuvem.

## 4) Top 4 Insights
- As lojas têm um volume menor de vendas no sábado e domingo em comparação aos dias úteis da semana.
- Lojas com promoções ativas há mais tempo tem uma queda nas vendas com o passar do tempo, mesmo com a promoção ativa. Longos períodos promocionais não são vantajosos.
- Lojas da categoria extra (maior sortimento) vendem menos em comparação às lojas das categorias basic e extended.
- Lojas com competidores abertos há mais tempo vendem menos do que lojas com concorrência mais recente.

## 5) Produto final do Projeto
- Bot no Telegram para consulta individual da previsão de vendas por loja.
repositório api: https://github.com/thiagomeneghello/render-app-deploy-rossmann-sales-forecast
repositório bot: https://github.com/thiagomeneghello/bot-deploy-rossmann-sales-forecast 
 
- Painel Gerencial para consultar a previsão de vendas das lojas e as métricas de dados da rede.
link: https://tfmeneghello-dashboard-rossmann.streamlit.app/
repositório: https://github.com/thiagomeneghello/dashboard-rossmann

## 6) Conclusão
O objetivo desse projeto é criar a previsão de vendas para as próximas 6 semenas e entregar o acesso remoto e individual para CFO. Também será feito um painel gerencial online para o acompanhamento das métricas e das previsões.

Quanto maior a quantidade dos dados melhor o aprendizado do modelo.

## 7) Próximos Passos
- Testaria novas hipóteses
- Reduziria o número de variáveis relevantes do modelo.
- Verificaria a relação entre os dados de treino e de validação.
- Treinaria o modelo novamente.
- Para avaliações temporais, definiria um range menor de comparação.
