# -superheropowers
Kaggle em https://www.kaggle.com/claudiodavi/superhero-set/data (superheropowers)


Desafio de aprendizado de máquina

Alelo


Introdução

Esta é uma pequena série de exercícios para avaliar seu conhecimento em aprendizado de máquina. Responda às perguntas detalhando as etapas executadas para resolver cada tarefa. Todas as perguntas são simples, mas esta é sua chance de nos mostrar seus conhecimentos técnicos.
Também esperamos receber seu código com sua solução e análise, incluindo quaisquer etapas de pré-processamento. Sinta-se à vontade para usar a linguagem de programação com a qual você se sentir mais confortável, mas forneça-nos instruções para executar seu código. Nem é preciso dizer, mas você não precisa codificar os algoritmos do zero. Você pode usar qualquer biblioteca disponível, como o scikit-learn. Lembre-se de que a organização e a legibilidade do seu código também serão avaliadas.
Queremos que este desafio (e esperamos que seu trabalho conosco) seja divertido, então selecionamos um conjunto de dados de super-heróis para você jogar! Você pode baixar os dados do Kaggle em https://www.kaggle.com/claudiodavi/superhero-set/data. É composto por dois arquivos csv, super hero powers.csv e heroes information.csv, e você usará os dois.
Por fim, projetamos esse desafio para durar no máximo três dias. Obviamente, não estamos cronometrando você, mas você não deve demorar muito mais para terminar este exercício. Lembre-se de que não estamos procurando os modelos de melhor desempenho, pois não é uma competição e principalmente avaliaremos sua abordagem para resolver essas tarefas. Portanto, invista seu tempo detalhando e explicando suas soluções, em vez de tentar o melhor modelo. Além disso, observe que não estamos definindo nenhuma divisão de dados ou métricas de avaliação. Isso depende inteiramente de você e será avaliado.
Se tiver algum problema com o exercício, não hesite em nos contactar, mas não iremos comentar as suas soluções nem aprofundar os detalhes técnicos das questões.
Clustering

Questão 1
Primeiro, queremos agrupar nossos super-heróis de acordo com seus poderes e informações. Execute um método de cluster não supervisionado usando o número de clusters que você julgar mais apropriado.

1. Qual algoritmo você escolheu e por quê? --> “k-means”
2. Quais recursos você usou e por quê? Explique qualquer pré-processamento ou engenharia de recursos (seleção) que você executou. --> Limpeza do banco de dados removendo dados faltantes (NAN), retirando as colunas não necessárias para análise estatística como a do ID.

Questão 2

Um dos desafios do clustering é definir o número certo de clusters. Como você escolheu esse número? Como você avalia a qualidade dos clusters finais? --> Através do método de Elbow (gráfico) com a inflexão aproximadamente 3 agrupamentos.

Identificando os bandidos
Nesta seção, lidaremos com o problema de aprendizagem supervisionada. Mais concretamente, iremos formular uma tarefa de classificação, e nosso alvo é o alinhamento dos super-heróis (bom ou mau).

Questão 3
Primeiro, usaremos o algoritmo Naive Bayes. Execute o algoritmo nos dados dos super-heróis para prever a variável de alinhamento e avaliar os resultados. Novamente, detalhe qualquer pré-processamento e engenharia de recursos que você aplicou no processo.

1. Quais hipóteses assumimos ao usar o algoritmo Naive Bayes? --> Altura e Peso são preditoras da Target ("Alignment").
2. Como as características específicas deste conjunto de dados influenciam suas escolhas e resultados de modelagem? --> Dados numéricos e contínuos.
3. Como você avalia os resultados? --> Foi necessário normalizar e balancear as classes, assim, no pré balanceamento a acuária era maior que após o procedimento.

Questão 4

Agora sinta-se à vontade para executar o algoritmo de classificação que julgar mais adequado para essa tarefa. Foi realizado um loop de modelos com a melhor acurária para a Arvore de Decisão.


1. O que motivou sua escolha do algoritmo? --> O resultado das análises de acurácia.
2. Como esse algoritmo se compara ao Naive Bayes em relação às suposições e resultados da modelagem? --> K-NN e Naive Bayes superam as Arvores de Decisão em ocorrências raras dos desfechos, se comparada a K-NN o NB supera pelos Hiperparâmetros alfa e beta. Os três métodos são indicados para Classificação no Aprendizado Supervisionado.

Além do bem e do mal

Vamos transformar nosso problema em uma tarefa de regressão e tentar prever o peso dos super-heróis dados os outros recursos.

1. Qual algoritmo você escolheu e por quê? --> Regressão Linear Múltipla devido utilizar mais de uma variável preditora.
2. Como você avalia o desempenho do seu algoritmo neste caso? --> R 0.547, sendo que ambos P são estatisticamente significativos (0.013; 0.000).

Análise
Quais aspectos desse conjunto de dados apresentam problemas para agrupamento, classificação e regressão? Como você resolveu esses problemas? As variáveis booleanas, essas foram transformadas para numéricas, limpeza do banco, normalização e balanceamento.

Bônus
Se você gostou de brincar com o conjunto de dados de super-heróis, esta seção é para você mostrar quaisquer outros aspectos dos dados que não exploramos nas perguntas. Como uma seção de bônus, isso é totalmente opcional, mas adoraríamos ver os insights que você pode obter desses dados. --> Relatório da Análise da Estatística pelo Pandas Profilling.




