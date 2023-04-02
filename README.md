# TG-EDUCACAO
Trabalho em Grupo realizado para a disciplina de Tópicos Especiais em Marketing II 

Objetivo do trabalho: estimar o potencial de mercado para novos negócios no ambito da educação nos municípios brasileiros.

Para atingir o objetivo do trabalho a estratégia de análise de dados utilizada foi utilizar o conceito de oferta X demanda. Assim, analisou-se a quantidade de estudantes que frequentam e não frequentam creches e pré-escolas (população total de crianças de 0 a 6 anos) em relação a quantidade de matrículas em creches e pré escolas (em tempo integral e parcial). Com isso, foi possível estabelecer um "ranking" dos municípios que apresentam oportunidades para a inserção de novas creches ou pré-escolas.

Optou-se por realizar esse estudo com as escolas de educação infantil pois é mais tangível e assertivo fazer a estimatia de mercado, já que o público desses estabelecimentos de estudos é definido, diferente, por exemplo, de universidades, que podem ter pessoas de diferentes idades realizando um curso superior. Para a segmentação do público de creches e pré-escolas usou-se a seguinte definição da constutuição federal: De acordo com o que a Constituição Federal e a LDB da Educação Nacional definiram as creches são para crianças de 0 a 3 anos de idade e as pré-escolas são para crianças de 4 a 6 anos de idade.



# Coleta e Limpeza de Dados

Para a primeira entrega do trabalho, reunimos os dados do censo de 2010 coletados no site do IBGE (https://www.ibge.gov.br/estatisticas/sociais/populacao/2098-np-censo-demografico/9662-censo-demografico-2010.html?=&t=downloads). Os dados escolhidos para primeira análise foram de "Educação e Deslocamento", "Indicadores Sociais Municipais" e "Trabalho e Rendimento", foi realizado o download das tabelas por estado, sendo cada tópico uma tabela diferente. Para realizar a limpeza dos dados, foram excluidos fatores não importantes para o trabalho e reafirmado que as 3 tabelas baixadas continham as mesmas cidade, na mesma ordem. Então, os dados foram agregados em 1 planilha por estado e, após reunir os dados dos 26 estados mais o DF, as 27 planilhas foram incorporadas a uma base de dados única, contendo dados de todo o país. 

Para a segunda entrega, foi entendido a necessidade de dados mais atuais para uma análise mais certeira. Os novos dados foram coletados da base do FNDE (https://www.fnde.gov.br/index.php/financiamento/fundeb/area-para-gestores/dados-estatisticos/item/13254-2020-com-base-na-portaria-interministerial-n%C2%BA-04,-de-27-12-2019). Desta vez, os dados foram baixados em pdf e convertidos em xls para serem limpos no excel - os dados foram conferidos para garantir que não houve alterações durante a conversão. Células que continham números e estavam em formato de texto foram modificados para 'número' e pontos (.) foram transformados em vírgulas (,) para uniformização dos dados. Por fim, os novos dados foram acrescentados a base antiga de dados para aperfeiçoar a análise.

Realizou-se também alguns agrupamentos de dados, a fim de tornar a análise mais simples, reduzindo o trade-off entre a interpretabilidade e acurácia, para deixar o modelo mais simples. Um exemplo de agrupamento pode ser visualizado a seguir:

Para maior entendimento dos dados:
Jovens - Indivíduos de até 19 anos;
Adultos - Indivíduos com idade entre 20 até 59 anos;
Idosos - Indivíduos de 60 anos em diante.


Por fim, depois de definida a estratégia de análise que leva em consideração o potencial de mercado para novas creches e pré-escolas em municípios brasileiros agregou-se mais dados que dizem respeito a características socioêconomicas de cada munícios brasileiro, como os índices de Desenvolvimento Humano Municipal (em uma perspetiva de renda, educação e geral) e também sobre o Produto Interno Bruto de cada cidade brasileira (geral e per capita), que é um importante indicador sobre a geração de riquezas de cada município.

É importante destacar que, por mais que os novos dados sejam semelhantes aos dados antigos, e que tenhamos adicionado mais variáveis ao longo da contrução do modelo, julgamos que existam diferenças suficientes neles para manter essas bases no código. Por exemplo, enquanto a primeira base separava os individuos por idade, a nova base os separa por nível educacional. O que gera uma complementariedade de informações e torna o modelo mais completo.

Vale ressaltar que todas as bases utilizadas levam em consideração todos os municípios brasileiros participantes do censo. Em algumas variáveis nã foi possível conseguir informações de 100% dos municípios presentes na base, nesses casos foi colocado o valor "0" em vez de deixar essa informação em branco ou com algum outro caracter, para que a coluna que contenha essa variável possa ser importada com sucesso e no formato correto (float).

# Análise Exploratória

Após levantar a base de dados utilizada na contrução do modelo, realizou-se outra importante etapa do processo que é a de Análises descritivas e exploratórias. Essa etapa tem como objetivo explorar e entender os dados disponíveis, antes de aplicar técnicas de modelagem ou análise mais complexas.

As análises descritivas são importantes para se ter uma visão geral dos dados, identificar possíveis problemas, erros ou inconsistências nos dados, além de auxiliar na escolha das técnicas apropriadas para análises futuras. Já as análises exploratórias permitem descobrir relações e padrões nos dados, o que ajuda a formular hipóteses iniciais que serão testadas posteriormente. 

Entre as técnicas utilizadas na EDA no trabalho estão: estatística descritiva, visualização de dados, identificação outliers, correlação entre variáveis, entre outras.

# Seleção de Modelos

Por fim, a última etapa do trabalho consiste em aplicar os conceitos vistos na prática ao longo do semestre, como: seleção de modelos, regularização e reamostragem. Essa é uma importante etapa do projeto que serve para melhorar a precisão e o desempenho do modelos desenvolvido.

A seleção de modelos consiste em escolher o modelo mais adequado para um determinado problema de negócio, considerando os dados disponíveis, essa etapa geralmente envolve o treinamento de modelos diferentes e a comparação de suas métricas de desempenho, sempre levando em consideração a relação entre acuracia e interpretabilidade para chegar em um modelo balanceado, já que não há um modelo ideal e padrão. Assim, para o nosso trabalho o modelo escolhido foi o de regressão, visto que as varáiveis que estamos analisando são quantitativas e este é o modelo mais utilizado.

Já a reamostragem é uma técnica utilizada para extrair o máximo possível da amostra que temos disponível, sendo possível avaliar o desempenho de um modelo em dados que não foram usados para treiná-lo. Assim, é possóvel ter múltiplas performances da amostra para definir um modelo mais assertivo. Existem diferentes técnicas de reamostragem que permitem estimar a precisão do modelo em dados não observados, tais como: Cross-validation (Validation set, Leave-One-Out (LOOCV) e k-Fold) e Bootstrap. Vale ressaltar que a reamostragem também é utilizada  para ajustar hiperparâmetros do modelo.

Por fim, a regularização é uma técnica utilizada para evitar o overfitting, que ocorre quando um modelo acaba sendo muito complexo e memoriza os dados de treinamento em vez de aprender padrões que possam ser generalizados para novos dados. Assim, a regularização serve para deixar o modelo mais simples e atingir o objetivo de ter um modelo equilibrado entre underfitting e overfitting. Para realizar esse processo, existem diferentes modelos de regularização, tais como: Subset Selection; Forward e Backward Stepwise Selection; Shrinkage: Ridge Regression; Shrinkage: Lasso Regression.


