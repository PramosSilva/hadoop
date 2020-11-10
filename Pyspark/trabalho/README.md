## Tratamento de dados - Spark  

Objetivo: Realizar o pré-processamento do dataset Movielens utilizando a linguagem de programação pyspark.

**Etapas a serem desenvolvidas:**

1. Utilizar o Dataset recomendação.csv disponibilizado no canvas:  
Schema: user_id int, item_id int, rating int, item string  

2. Utilizar a ferramenta [pydeequ](https://pypi.org/project/pydeequ/) (Links para um site externo.) para verificar se todos os dados se enquadram no schema definido acima. Imprimir o Data Quality Report gerado pela ferramenta.  
OBS: Para executar a ferramenta  
Fazer download do deequ-1.0.5.jar e salvar na pasta que será executado o pyspark  
 [Links para um site externo](https://repo1.maven.org/maven2/com/amazon/deequ/deequ/1.0.5/deequ-1.0.5.jar).  
Instalar o pydeequ via pip ou pelo [git](https://github.com/margitaii/pydeequ).   
Rodar o comando   pyspark --driver-class-path deequ-1.0.5.jar  

3. Remover do Dataset os dados incorretos.  

4. Responder as perguntas:  
. Qual o filme mais assistido?  
. Qual o usuário que mais pontuou os filmes?  
. Quantos usuários deram nota(rating) = 5?  
. Agrupe o Dataset por user e some todas as suas notas. Qual o usuário possui a maior soma dos rating?  

5. Gerar Dataset tratado para o algoritmo de recomendação no formato csv com o schema user_id, item_id, rating.  

## Sistema de recomendação - Spark

Objetivo: A empresa FlixBR está pensando em ampliar sua base de dados e melhor sua experiência com o usuário e para isso deseja realizar a implementação de um sistema de recomendação.   

**Etapas a serem desenvolvidas:**  

1. Utilizar o Dataset gerado na tarefa anterior.  
2. Desenvolver um algoritmo de recomendação de filtragem colaborativa utilizando Pyspark.  
3. Desenvolver uma apresentação que contemple os seguintes tópicos:  
. O que é um sistema de recomendação;  
. Por que utilizar um sistema de recomendação;  
. Quais as principais técnicas utilizadas pelo mercado para sistemas de recomendação;  
. Apresentar o algoritmo desenvolvido e os resultados obtidos.  
