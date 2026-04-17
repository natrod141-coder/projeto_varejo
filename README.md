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
- [x]  Qual o total de itens vendidos (somar a quantidade de todos os itens)? 5.495,941 itens vendidos.
- [x]  Qual o valor total de vendas? 52.455.220,40 vendas.
- [x]  Quantos itens cada **Store_type** vendeu e quantos % representa do total de itens vendidos?
| Store_Type | Total_Items | Percentual |
| :--- | :--- | :--- |
| Convenience Store | 918.049 |16.70% |
| Department Store | 915.635 | 16.66% |
| Pharmacy | 917.729 | 16.69% |
| Specialty Store | 914.950 | 16.64% |
| Supermarket | 915.772 | 16.66% |
| Warehouse Club | 913.806 | 16.62% |

- [x]  Qual o total de custo por **Store_type** e qual o % do total de custos.
| Store_Type | Total_Cost | % do Custo Total |
| :--- | :--- | :--- |
| Convenience Store | 8.731.901,36	| 16,65% |
| Department Store | 8.731.555,57 | 16,65% |
| Pharmacy | 8.766.679,01 | 16,71% |
| Specialty Store | 8.701.600,22 | 16,59% |
| Supermarket | 8.763.455,21 | 16,71% |
| Warehouse Club | 8.760.029,03 | 16,70% |
 
- [x]  Qual método de pagamento é mais usado e qual é menos usado? Mais: Cash, Menos: Mobile Payment.
- [x]  Qual o método escolhido para as compras mais caras? Cash.
- [x]  Qual a quantidade de vendas por hora.
As vendas apresentam uma distribuição extremamente uniforme ao longo das 24 horas, com uma média de aproximadamente 417 mil itens por hora.
Hora com mais vendas: 10h (42.021 itens). Hora com menos vendas: 11h (41.154 itens).
Insight: A variação entre o pico e a mínima é de apenas 2%, indicando uma operação que não sofre com horários de pico acentuados, mantendo um fluxo constante de saída.

- [x]  Qual a quantidade de vendas por dia da semana. 
Assim como na análise horária, o volume de vendas por dia é equilibrado, com destaque para o início da semana:
Dia com mais vendas: Segunda-feira (Monday) com 142.435 itens
Segundo colocado: Terça-feira (Tuesday) com 142.317 itens.
Dia com menos vendas (dos visíveis): Domingo (Sunday) com 142.092 itens.

- [x]  O dia e hora com mais venda por cidade? 
Cidade: Atlanta | Dia: Thursday | Horário: 21h | Total: 654 vendas
Cidade: Boston | Dia: Wednesday | Horário: 13h | Total: 661 vendas
Cidade: Chicago | Dia: Thursday | Horário: 23h | Total: 684 vendas
Cidade: Dallas | Dia: Monday | Horário: 16h | Total: 666 vendas
Cidade: Houston | Dia: Thursday | Horário: 2h | Total: 664 vendas
Cidade: Los Angeles | Dia: Friday | Horário: 18h | Total: 650 vendas
Cidade: Miami | Dia: Saturday | Horário: 18h | Total: 668 vendas
Cidade: New York | Dia: Thursday | Horário: 20h | Total: 658 vendas
Cidade: San Francisco | Dia: Thursday | Horário: 21h | Total: 652 vendas
Cidade: Seattle | Dia: Friday | Horário: 5h | Total: 663 vendas

### 2. Investigação Profunda por Setor 
*Setor escolhido: [Convenience Store]*
- [x]  Escolher um **Store_type** e vai fazer as próximas análises no setor escolhido
- [x]  Filtre ou recorte o dataset com o setor da sua escolha
- [X]  Na coluna **Product** temos mais de um item vendido por transação; você vai separar esses itens e agrupar por item. 
*Queremos saber:*
- [X]  Qual item no seu setor vendeu mais (apareceu com mais frequência)? Toothpaste com 12.175 vendidos
- [X]  Qual item no seu setor vendeu menos (apareceu com menos frequência)? Pasta
- [x]  Qual item cada perfil de cliente compra mais? Todos preferem Toothpast.

### 3. Modelo de Recomendação (Machine Learning) 
Implementação de modelos de associação para identificar itens comprados juntos:
- [x] **Técnicas:** Estudo dos algoritmos Apriori, FP-Growth.
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