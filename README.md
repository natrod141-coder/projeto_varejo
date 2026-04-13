# Análise de Dados e Sistema de Recomendação - Varejo

Este projeto faz parte de um desafio de Ciência de Dados focado em entender o comportamento de compra de clientes e desenvolver um sistema de recomendação de produtos.

---

## Contexto do Projeto
O objetivo principal é transformar dados brutos de transações em insights de negócios. Através da Análise Exploratória de Dados (EDA) e modelos de Machine Learning, buscamos responder perguntas estratégicas e sugerir combinações de produtos ("quem compra X, também costuma comprar Y").

## Estrutura do Repositório
* `Data/`: Armazenamento local do dataset (arquivos .csv são ignorados pelo Git devido ao tamanho).
* `Notebooks/`: Scripts e Jupyter Notebooks com as análises.
* `README.md`: Documentação principal do projeto.

---

## Etapas de Desenvolvimento

### 1. Análise Exploratória (EDA) 
Nesta fase inicial, analisamos o faturamento e volume de vendas global para entender a saúde do negócio:
- [x]  Qual o total de itens vendidos (somar a quantidade de todos os itens): 5495941 itens
- [x]  Qual o valor total de vendas: 52455220.40
- [x]  Quantos itens cada **Store_type** vendeu e quantos % representa do total de itens vendidos
- [x]  Qual o total de custo por **Store_type** e qual o % do total de custos.
- [x]  Qual método de pagamento é mais usado e qual é menos usado.
- [x]  Qual o método escolhido para as compras mais caras.
- [x]  Qual a quantidade de vendas por hora.
- [x]  Qual a quantidade de vendas por dia da semana.
- [x]  O dia e hora com mais venda por cidade.

### 2. Investigação Profunda por Setor 
*Setor escolhido: [Convenience Store]*
- [x]  Escolher um **Store_type** e vai fazer as próximas análises no setor escolhido
- [x]  Filtre ou recorte o dataset com o setor da sua escolha
- [X]  Na coluna **Product** temos mais de um item vendido por transação; você vai separar esses itens e agrupar por item. 
*Queremos saber:*
- [X]  Qual item no seu setor vendeu mais (apareceu com mais frequência)
- [X]  Qual item no seu setor vendeu menos (apareceu com menos frequência)
- [x]  Qual item cada perfil de cliente compra mais

### 3. Modelo de Recomendação (Machine Learning) 
Implementação de modelos de associação para identificar itens comprados juntos:
- [x] **Técnicas:** Estudo dos algoritmos Apriori, FP-Growth ou Eclat.
- [x] **Métricas:** Avaliação por Suporte, Confiança e Lift.
- [x] **Próximos Passos:** Clusterização de clientes por comportamento.

---

## Tecnologias Utilizadas
- **Python** (Pandas, Numpy)
- **Visualização:** Seaborn, Matplotlib
- **Machine Learning:** MLxtend / Scikit-Learn
- **Versionamento:** Git & GitHub

## Base de Dados
O dataset utilizado foi o **Retail Transactions Dataset**, disponível no [Kaggle](https://www.kaggle.com/datasets/prasad22/retail-transactions-dataset).

---
*Projeto desenvolvido como parte de treinamento interno em Ciência de Dados.*git push origin develop1