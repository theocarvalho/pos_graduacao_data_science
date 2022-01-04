# pos_graduacao_data_science
Projeto de pós graduação BI Master (Data Science)

<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->

# Abordagem didática para iniciantes em Machine Learning

#### Aluno: [Theo Carvalho](https://github.com/theocarvalho).
#### Orientadora: [Manoela Kohler](https://github.com/manoelakohler).

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

- [Link para o código](https://github.com/link_do_repositorio/nome_do_arquivo_de_codigo). <!-- caso não aplicável, remover esta linha -->


- Trabalhos relacionados: <!-- caso não aplicável, remover estas linhas -->
    - [Gravação do vídeo](https://drive.google.com/file/d/1DvmeyTGILfP9-qb8EOIjpLnMk4IfMbL2/view?usp=sharing).
    - [Google Sheets: Abordagem didática de construção do modelo KNN](https://docs.google.com/spreadsheets/d/1APPm642Bdz5dQ72c-2a4yhz_jxlWmH50dzLXKNS7c5Q/edit#gid=1883246793).

---

### Resumo

<!-- trocar o texto abaixo pelo resumo do trabalho, em português -->

Este projeto se propõe a aproximar profissionais de diferentes ramos aos conceitos iniciais de machine learning e data science. Ter conhecimento em determinadas técnicas gera oportunidade de negócio ao mesmo tempo que aproxima a sociedade de conceitos que comumente são vistos como inacessíveis. Como técnica de facilitação, é utilizado o algoritmo k nearest neighbors (KNN) e da plataforma de acesso gratuito Google planilhas (sheets). KNN é um algoritmo conhecido por ser de pouca utilização atualmente, ao mesmo tempo que o é utilizado como uma das principais maneiras de ensinar algoritmos de machine learning supervisionados. Como base de dados, também é utilizado uma das mais populares, a denominadas 'iris dataset'. Através de uma planilha é construído desde seu princípio o algoritmo KNN com a utilização de apenas fórmulas já existentes na ferramenta. São abordados conceitos de estrutura de dados, transformação dos dados, como o algoritmo KNN funciona, a importância da divisão entre base de treino e teste e, por último, a execução da planilha comparada a um script em linguagem Python. O modelo alcança resultado de 87% de acurácia ou superior  para suas respectivas classes. E, acima de tudo, procura ensinar como esse modelo pode ser aplicado para resolver diferentes problemas nas mais diferentes áreas de conhecimentos.
Através de vídeos são aprofundados conhecimentos como normalização dos dados, distância euclidiana, taxa de erro e calibração do modelo. Das análises dos dados, há 4 atributos por amostra e comprimento da pétala sendo como um dos principais fatores de diferenciação das classes -- que podem ser setosa, virginica ou versicolor. Por último, o projeto traz uma reflexão da importância de aprendermos determinados conceitos antes de aplicarmos em escala através de linguagem de programação. A conclusão busca evidenciar que a ciência de dados pode ser compreendida por diferentes profissionais e, se bem aplicada, pode ser flexível em ajudar na resolução de variados problemas de negócio.


### Abstract <!-- Opcional! Caso não aplicável, remover esta seção -->

<!-- trocar o texto abaixo pelo resumo do trabalho, em inglês -->

This project intends to demystify the knowledge behind data science and machine learning. Getting this subject more familiar to a myriad of professionals results in business opportunities and also enables this subject to be more accessible throughout society. In order to introduce data science and machine learning content, the project applies the k nearest neighbors (KNN) algorithm via google spreadsheets and native formulas. The model is built from the ground up. Subjects such as data structures, data wrangling and KNN intricacies are discussed. Scientific approach to split between train and test are also applied and explained. The project concludes using a Python script to show how all these knowledge are intertwined whenever you are using a more scalable and popular approach. The script abstracts some complexity, which can be comprehend thanks to knowledge attained during google sheets practice. The model itself reaches 87% or more for their classes whereas it teaches fundamental mechanics to build and assess a data algorithm.
The educational video delves into data normalization, euclidean distance, error rate and model calibration. The dataset has 4 attributes by sample, being petal’s length one of its main factors to differentiate within classes — which can be Setosa, Virginica and Versicolor. Finally, the project brings an important concept of learning essential fundamentals before applying in scale via code. Data Science can be used and understood by all kinds of professional backgrounds, and if well applied, can be flexible enough to solve a vast majority of problems.


### 1. Introdução
 
A utilização do Iris dataset é pode ser feita através de diferentes maneiras, dado que é um dataset popular encontrado na comunidade de Ciência de dados. Este dataset apresenta 150 amostras. Os 4 atributos são físicos, relacionados diretamente a sua anatomia.
Com a análise exploratória é possível perceber através de, por exemplo, um gráfico de dispersão, que existem alguns atributos que ajudam a diferenciar até certo ponto uma classe da outra, como é o caso do comprimento da pétala que ajuda a determinar uma das três classes. Porém, a análise exploratória por si só é limitante. Utilizar a abordagem de aprendizado de máquina pode trazer um modelo de classificação mais pragmático e escalável para determinar as classes.
 
 
### 2. Modelagem
 
Um dos principais desafios da modelagem é conseguir aplicá-la dentro de uma planilha, utilizando de apenas fórmulas nativas da ferramenta. O primeiro desafio passa por selecionar randomicamente o dado. Para isso é criado uma fórmula de probabilidade para determinar um alvo de percentual do dataset para treino e teste. Com o dataset de treino apartado, é importante normalizar seus atributos -- obviamente, sem levar em conta os dados de treino.
A partir deste cenário, a complexidade de trazer um modelo comumente utilizado em linguagem de programação para linguagem excel/spreadsheet passa a aumentar consideravelmente. Para criar os parâmetros de distância, é criado uma matriz n por n que, utilizando a fórmula de distância euclidiana, mede a distância entre todos os membros.
Com a distância entre as amostras da base de treino, é possível iterar no parâmetro k (quantidade de vizinhos para votação da classe) e comparar os resultados. Realizar tal objetivo é uma atividade desafiadora, mas de uma certa forma, mais didática do que quando comparamos com uma iteração em linguagem de programação. Para isso, é criado uma tabela em que cada linha da amostra tem colunas, sendo elas, a quantidade de cada classe para determinado valor de k. A partir de então, é possível comparar o valor real com a classe que recebeu a maior quantidade de votos. Consequentemente, é possível medir a taxa de erro, métrica que guia para determinar o melhor valor de k.
Após análise do parâmetro k na base de treino é possível replicar na base de teste e aferir se o valor da taxa de erro está similar à base anterior.
Por último, esse mesmo reacional é utilizado na construção do script em python. Mas desta vez, é utilizado de bibliotecas e práticas conhecidas no mercado que abstraem consideravelmente toda essa construção -- o que para fins didáticos pode ser pior, mas inquestionavelmente é escalável para resolver problemas de negócio. Dentre as práticas, é perceptível a facilidade de criar um iterador para valor de k, conseguindo atribuir diferentes valores e checando sua taxa de erro.
 
### 3. Resultados
 
Acredito que esse trabalho alcançou resultados em diferentes áreas. A acurácia conseguiu chegar a valores de 87% ou superior. A performance do modelo foi satisfatória para o tamanho da base. Há ressalvas para aplicar tanto o modelo em uma planilha quanto o código quando a base chegar nas centenas de milhares e nas dezenas de milhões, respectivamente.
 
O valor de K se demonstrou com bom acréscimo marginal até por volta de k=10. A partir de então, em ambos os algoritmos, a taxa de erro apresenta uma redução crescente, no âmbito do código, saindo de abaixo de 10% para acima de 20% de taxa de erro.
 
É importante também ressaltar o que foi na verdade o principal objetivo deste trabalho, conseguir sintetizar conceitos de Machine Learning em formato mais didático e palatável para profissionais distantes do universo da Ciência de Dados. Sobre esse objetivo, foi produzido um material em planilha Google Spreadsheet, ferramenta atualmente gratuita e de utilização global, com a montagem integral desde a extração até a montagem e avaliação do modelo de machine learning funcional. Em conjunto, também há uma explicação em modelo passo-a-passo de um vídeo explicativo dividido em 7 tópicos
 
 
### 4. Conclusões
 
Com a utilização do modelo de Machine Learning supervisionado K Nearest Neighbors, foi desenvolvido um modelo com acurácia acima de 87%, o que é superior aos 33% que a completa aleatoriedade resultaria para um dataset como este -- número igual de amostras entre as três classes.
 
O exercício de simplificar e, de uma certa forma, explicar conceitos através de ferramenta popular trouxe invariavelmente uma capacidade de entender com maior profundidade uma técnica de Ciência de Dados. Sendo este método replicável e com potencial de ser ainda mais didático de absorção de conhecimento por parte de profissionais leigos no assunto.
 
Com isso, o profissional que busca trazer maiores conhecimentos sobre análise de dados, ciência de dados e machine learning tende a diminuir seu obstáculo inicial de aprendizado. Utilizando da técnica de associar conhecimentos novos a uma ferramenta com maior chance de familiaridade permite que haja maior sinergia e engajamento para aprender. Aplicar com maior consciência métodos de aprendizado de máquina abrem potenciais novas oportunidades para o profissional tomar decisões de negócio ainda mais valorosas.
 
---


Matrícula: 192.671.143

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
