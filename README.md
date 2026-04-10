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
- [ ] Total de itens vendidos e Valor total de vendas.
- [ ] Representatividade de vendas por **Store_type** (%).
- [ ] Custos operacionais e margens por canal.
- [ ] Métodos de pagamento mais utilizados e relação com o ticket médio.
- [ ] Sazonalidade: Vendas por hora e dia da semana.
- [ ] Desempenho geográfico (cidade com mais vendas).

### 2. Investigação Profunda por Setor 
*Setor escolhido: [INSERIR SEU SETOR AQUI]*
- [ ] Filtragem do dataset para o setor escolhido.
- [ ] Tratamento da coluna `Product` (separação de itens por transação).
- [ ] Identificação dos itens mais e menos vendidos no setor.
- [ ] Análise do perfil do cliente por consumo.

### 3. Modelo de Recomendação (Machine Learning) 
Implementação de modelos de associação para identificar itens comprados juntos:
- [ ] **Técnicas:** Estudo dos algoritmos Apriori, FP-Growth ou Eclat.
- [ ] **Métricas:** Avaliação por Suporte, Confiança e Lift.
- [ ] **Próximos Passos:** Clusterização de clientes por comportamento.

---

## Tecnologias Utilizadas
- **Python** (Pandas, Numpy)
- **Visualização:** Seaborn, Matplotlib
- **Machine Learning:** MLxtend / Scikit-Learn
- **Versionamento:** Git & GitHub

## Base de Dados
O dataset utilizado foi o **Retail Transactions Dataset**, disponível no [Kaggle](https://www.kaggle.com/datasets/prasad22/retail-transactions-dataset).

---
*Projeto desenvolvido como parte de treinamento interno em Ciência de Dados.*