# TG-EDUCACAO
Trabalho em Grupo realizado para a disciplina de Tópicos Especiais em Marketing II 

Objetivo do trabalho: estimar o potencial de mercado para novos negócios no ambito da educação nos municípios brasileiros

Primeira etapa do trabalho: realizar a coleta, a limpeza, o pre-processamento e a análise exploratória da base de dados referente à dimensão EDUCAÇÃO. 

# Coleta e Limpeza de Dados

Para a primeira entrega do trabalho, reunimos os dados do censo de 2010 coletados no site do IBGE (https://www.ibge.gov.br/estatisticas/sociais/populacao/2098-np-censo-demografico/9662-censo-demografico-2010.html?=&t=downloads). Os dados escolhidos para primeira análise foram de "Educação e Deslocamento", "Indicadores Sociais Municipais" e "Trabalho e Rendimento", foi realizado o download das tabelas por estado, sendo cada tópico uma tabela diferente. Para realizar a limpeza dos dados, foram excluidos fatores não importantes para o trabalho e reafirmado que as 3 tabelas baixadas continham as mesmas cidade, na mesma ordem. Então, os dados foram agregados em 1 planilha por estado e, após reunir os dados dos 26 estados mais o DF, as 27 planilhas foram incorporadas a uma base de dados única, contendo dados de todo o país. 

Para a segunda entrega, foi entendido a necessidade de dados mais atuais para uma análise mais certeira. Os novos dados foram coletados da base do FNDE (https://www.fnde.gov.br/index.php/financiamento/fundeb/area-para-gestores/dados-estatisticos/item/13254-2020-com-base-na-portaria-interministerial-n%C2%BA-04,-de-27-12-2019). Desta vez, os dados foram baixados em pdf e convertidos em xls para serem limpos no excel - os dados foram conferidos para garantir que não houve alterações durante a conversão. Células que continham números e estavam em formato de texto foram modificados para 'número' e pontos (.) foram transformados em vírgulas (,) para uniformização dos dados. Por fim, os novos dados foram acrescentados a base antiga de dados para aperfeiçoar a análise.

É importante destacar que, por mais que os novos dados sejam semelhantes aos dados antigos, julgamos diferenças suficientes neles para manter as duas bases no código. Por exemplo, enquanto a primeira base separava os individuos por idade, a nova base os separa por nível educacional.

Para maior entendimento dos dados:
Jovens - Indivíduos de até 19 anos;
Adultos - Indivíduos com idade entre 20 até 59 anos;
Idosos - Indivíduos de 60 anos em diante.
