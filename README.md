# AnaliseLivrosAmazon
## Dataset
O conjunto de dados foi retirado do site/link [Kaggle](https://www.kaggle.com/datasets/anushabellam/amazon-reviews-dataset).
**Data de acesso: 11/19/2023**
## Sobre o dataset
O conjunto de dados apresenta reviews feitas por clientes da amazon. As informações dos comentários ajuda os clientes a terem uma análise genuina do produto e a empresa a entender o tipo de produto que está trabalhando, já que nos tempos atuais, muitas empresas como a amazon revendem produtos.
O dataset apresenta 5 arquivo do tipo csv (valores separados por vírgula), dos quais contém as seguintes colunas:
1. marketplace (string) - Location of the product (Local do produto)
1. customer_id (string) - Unique ID of the Customer (Id único do cliente)
1. review_id (string) - Reviewing ID 
1. product_id (string) - Unique ID of the product (Id único do produto)
1. product_parent (string) - Parent Product (Produtos similares)
1. product_title (string) - Title of the product reviewed ( Título do produto)
1. product_category (string) - Different products categories ( Categoria do produto)
1. star_rating (int) - Rating of the product out of 5 (Avaliação de 0 a 5)
1. helpful_votes (int) - Rating of the product which is helpful for more sales ( Avaliação de votos que ajudam a melhorar as vendas)
1. total_votes (int) - Total number of votes of the product (Número total de votos do produto)
1. review_headline (string) - heading of the review (Título da review)
1. review_body (string) - Content of the review (Conteúdo da review)
1. review_date (string) - date at which the product is reviewed (Data da review)
## Importando bibliotecas

import numpy as np # Algebra Linear

import pandas as pd # Leitor arquivo csv, processamento de dado

import matplotlib.pyplot as plt # Análise gráfica

import plotly.express as px # Análise gráfica

##Dataset importando

dataset1 = pd.read_csv(r"C:\Users\thale\Downloads\amazon_pc_Data.csv")

dataset2 = pd.read_csv(r"C:\Users\thale\Downloads\amazon_jwellery_Data.csv")

dataset3 = pd.read_csv(r"C:\Users\thale\Downloads\amazon_books_Data.csv")

dataset4 = pd.read_csv(r"C:\Users\thale\Downloads\amazon_ebook_Data.csv" )

dataset5 = pd.read_csv(r"C:\Users\thale\Downloads\amazon_grocery_Data.csv" )


## Visualizando dataset e tratamento
dataset1.head()

### Coluna Unamed não irá servir para nada, já que não existia no dataset, apenas apareceu como índice
dataset1.drop(columns='Unnamed: 0', inplace = True)
dataset1.info()

# Observações
-O projeto foi realizado utilizando jupyter notebook, assim como o visual studio code.
*Aprendizados:
-Integrar jupyter notebook, o visual studio code ao github, aprendendo a formar um readme e a trabalhar com branches.
-Resolver problemas de importação de dados do tipo csv no pandas
-Tratamento de dataset, utilizando a função info e head para ter uma amostra dos tipos de dados abordados, funcao drop para eliminar colunas que não serão uteis nesse caso, função nunique e counts para visualizar os valores de cada coluna, podendo ter colunas com apenas 1 valor ou com valores de "string" diferentes, precisando ser normalizados ex: "N" ou "Não", embora sejam a mesma coisa, precisam ser normalizados.


