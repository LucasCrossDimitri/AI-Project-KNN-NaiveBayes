
# Reconhecimento Óptico de Dígitos Manuscritos 

## Objetivo - Comparação de dois modelos de IA

O objetivo deste projeto é realizar a comparação de dois modelos, diferentes, de algoritmos de classificação, utilizando uma mesma base de dados para apoio. A base selecionada para esta tarefa foi a “Conjunto de dados de reconhecimento óptico de dígitos manuscritos” (Optical Recognition of Handwritten Digits Data Set), que foi criada em 1998 e está disponível no repositório de machine learning de UCI. Os modelos de machine learning selecionados para a realização da análise comparativa foram o KNN (K-Nearest Neighbors) e Naive Bayes.

### O Caminho:

Durante o Projeto definimos funções, [@Guilherme Ternorio](https://github.com/) foi responsável por montar o KNN e definir o banco de dados, e com isso definido foi necessário achar uma opção entre as muitas para fazer o comparativo, que eu [@Lucas ](https://github.com/LucasCrossDimitri) tendo visão que nosso banco de dados teria que suportar esse método com isso inicialmente tentei pegar e executar o SVM no nosso banco de dados para fazer o comparativo, depois de vários testes cheguei a conclusão que não seria possivel, pois o SVM não suporta o banco de dados, e com isso continuei para a próxima opção que foi o Naive Bayes, seguindo tutoriais e exemplos chegamos ao que precisamos de informação para montar o comparativo. 

### Escopo do problema de classificação

O reconhecimento ótico de caracteres é de extrema importância, sua utilização em aplicativos de edição de texto como o Microsoft Word, o Google Docs ou o Notes (da Apple) tem sido cada vez mais comum de se encontrar no dia a dia, sendo capaz de realizar a tradução de imagens em textos. A principal problemática com o sistema de reconhecimento de dígitos está em selecionar o melhor algoritmo de classificação e uma base de dados com volume expressivo o suficiente para que seja realizado o treinamento do algoritmo, além do pré-processamento da intensidade dos pixels das imagens em números reais. Para a realização do treinamento e do teste das classificações, será utilizado a biblioteca do Scikit-Learn, que dispõe de uma base de dados pré-processada de dígitos manuscritos. Ademais, para averiguar a acurácia dos dois modelos de machine learning, utilizaremos a comparação entre as matrizes de confusão de ambos os algoritmos.

## Requisitos da Análise

### Conceitos dos algoritmos 
Os algoritmos que foram escolhidos são um deles do tipo de classificação e o outro do tipo supervisionado, sendo estes algoritmos selecionados pois possuem como objetivo classificar as amostras de acordo com as características observadas e contam com diversos dados já classificados para o treinamento.

### KNN
É um algoritmo do tipo classificador que possui o seu aprendizado focado nas similaridades dos pontos de dados. Sua forma de classificação, como o próprio nome diz, é baseada nos “k” vizinhos mais próximos, contando com um sistema de votação para predição. O KNN não é paramétrico, ou seja, não faz fortes suposições sobre a forma da função de mapeamento e tem fácil implantação para muitos casos de machine learning. Na sequência temos alguns dos passos para a sua implantação:

* Recebe dados classificados para treinamento;
* Escolher o melhor “k” para comparação dos vizinhos;
* Escolhe melhor função para encontrar distância entre os vizinhos;
* Recebe dados não classificados;
* Classifica de acordo com os “k” vizinhos mais próximos através de votação.

### Naive Bayes

Este algoritmo é um dos modelos de utilização mais popular no aprendizado de máquina (machine learning). O algoritmo realiza uma classificação probabilística dos eventos que virão a ocorrer, sendo recomendado que seja utilizado em conjunto com atributos discretos. O termo “Naive” (ingênuo) refere-se a ideia de que o algoritmo desconsidera as correlações entre as variáveis, e o termo “Bayes” é uma referência ao “Teorema de Bayes”.

Na fase de treinamento, o modelo Naive Bayes recebe uma base de dados e cria uma tabela de probabilidade, em que analisa a correlação entre as variáveis presentes. Quando um novo registro é apresentado, o algoritmo o compara a essa tabela e o resultado é baseado na semelhança entre o registro desconhecido e o que mais se assemelha a tabela de probabilidade.

## Resultado Obtidos

### KNN
O algoritmo KNN obteve 98,70% de acurácia, utilizando o melhor “k”. Para a escolha correta do número de vizinhos, foi criado loop que escolhe o melhor parâmetro, em que a acurácia seja a mais alta e o valor seja maior que um.

<p align="center">
  <img src="https://github.com/LucasCrossDimitri/AI-Project-KNN-NaiveBayes/blob/main/KNN_Acuracia.png?raw=truee" />
</p>

No gráfico acima podemos verificar que quanto maior o número de vizinhos a serem comparados, menor é a acurácia. Sendo assim, foi escolhido pela estrutura de loop o “k” igual a cinco.

### Naive Bayes

O algoritmo teve uma acurácia de 83,33%, isso se deve pelo fato de que o Naive Bayes tem como objetivo analisar diversas variáveis e estabelecer relações entre elas através da tabela de probabilidade.

### Matriz de Confusão

A matriz de confusão é uma tabela que possibilita obter métricas que auxiliam na avaliação da classificação dos modelos de machine learning, quando a variável resposta é categórica. Abaixo a matriz de confusão dos dois modelos do projeto. 

<p align="center">
  <img src="https://github.com/LucasCrossDimitri/AI-Project-KNN-NaiveBayes/blob/main/Matriz_de_Confusão.png?raw=truee" />
</p>

## Conclusão

Realizando uma análise entre os dois algoritmos utilizados, pudemos chegar a conclusão que o algoritmo KNN possui uma melhor classificação de acurácia frente ao Naive Bayes, sendo, respectivamente, 98,70% e 83,33% a acurácia dos modelos supracitados. Essa diferença entre os algoritmos se deve ao modo como os dois modelos funcionam. O modelo Naive Bayes possui como princípio desprezar as características que relacionam os dados entre si, considerando apenas os atributos discretos para fazer uma análise probabilística. O modelo KNN possui em seu núcleo de funcionalidade o foco a similaridade e as distâncias entre cada dado. Devido essas distinções dos modelos e as acurácias analisadas, pode-se afirmar que as características entre as imagens, ou seja, os padrões, têm grande relevância no algoritmo para a base de dados aplicada. 
## Badges

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Jupyter_logo.svg/1200px-Jupyter_logo.svg.png" width="64"/>



## Documentation

* [Banco De dados - Optical Recognition of Handwritten Digits Data Set](https://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits)
* [SVM](https://medium.com/turing-talks/turing-talks-12-classifica%C3%A7%C3%A3o-por-svm-f4598094a3f1)
* [KNN](https://medium.com/brasil-ai/knn-k-nearest-neighbors-1-e140c82e9c4e)
* [Naive Bayes](https://www.digitalhouse.com/br/blog/naive-bayes/)


## Authors

- [@Lucas Patrick Casara](https://github.com/LucasCrossDimitri)
- [@VitorWolf](https://github.com/victorwolff39/)
- [@Guilherme Lamin](https://github.com/GBLamim/)
- [@Guilherme Ternorio](https://www.linkedin.com/in/gui-tenorio/)
- [@Miguel](https://www.linkedin.com/in/miguel-bertemes-costa-809257171/)
- [@Jhonathan](https://www.linkedin.com/in/jonathan-joao-de-souza-bb0491160/)
