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

## 1. Análise Exploratória (EDA)
Nesta fase inicial, analisamos o faturamento e volume de vendas global para entender a saúde do negócio:

### Métricas Gerais
* **Total de itens vendidos:** 5.495.941 itens
* **Faturamento Total:** R$ 52.455.220,40
* **Método de pagamento mais usado:** Cash (Dinheiro)
* **Método de pagamento menos usado:** Mobile Payment
* **Método preferido para compras de alto valor:** Cash

### Desempenho por Tipo de Loja (Store Type)
| Store Type | Total de Itens | Percentual (%) | Custo Total (R$) | % do Custo Total |
| :--- | :---: | :---: | :---: | :---: |
| **Convenience Store** | 918.049 | 16,70% | 8.731.901,36 | 16,65% |
| **Department Store** | 915.635 | 16,66% | 8.731.555,57 | 16,65% |
| **Pharmacy** | 917.729 | 16,69% | 8.766.679,01 | 16,71% |
| **Specialty Store** | 914.950 | 16,64% | 8.701.600,22 | 16,59% |
| **Supermarket** | 915.772 | 16,66% | 8.763.455,21 | 16,71% |
| **Warehouse Club** | 913.806 | 16,62% | 8.760.029,03 | 16,70% |

### Análise de Sazonalidade (Tempo)
* **Vendas por Hora:** Distribuição uniforme (média de ~417 mil itens/hora).
* **Pico:** 10h (42.021 itens).
 * **Mínima:** 11h (41.154 itens).
- **Vendas por Dia da Semana:** Equilibrado, com destaque para Segunda-feira (Monday) com 142.435 itens.

### Recorde de Vendas por Cidade
| Cidade | Dia da Semana | Horário | Total de Vendas |
| :--- | :--- | :---: | :---: |
| **Atlanta** | Thursday | 21h | 654 |
| **Boston** | Wednesday | 13h | 661 |
| **Chicago** | Thursday | 23h | 684 |
| **Dallas** | Monday | 16h | 666 |
| **Houston** | Thursday | 02h | 664 |
| **Los Angeles** | Friday | 18h | 650 |
| **Miami** | Saturday | 18h | 668 |
| **New York** | Thursday | 20h | 658 |
| **San Francisco** | Thursday | 21h | 652 |
| **Seattle** | Friday | 05h | 663 |

---

## 2. Investigação Profunda por Setor
**Setor selecionado:** `Convenience Store`

* **Tratamento de Dados:** Itens separados por transação e agrupados por frequência.
* **Item mais vendido:** `Toothpaste` (12.175 unidades).
* **Item menos vendido:** `Pasta`.
* **Perfil do Cliente:** Todos os perfis demonstraram preferência pelo item `Toothpaste`.

---

## 3. Modelo de Recomendação (Machine Learning)
Implementação de modelos de associação para identificar padrões de consumo:

* **Técnicas:** Estudo dos algoritmos **Apriori** e **FP-Growth**.
* **Métricas:** Avaliação por Suporte, Confiança e **Lift**.
* **Próximos Passos:** Realizar a Clusterização de clientes por comportamento de compra.

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