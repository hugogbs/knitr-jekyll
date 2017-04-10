---
title: "relatorio_interativo"
author: "Gileade"
date: "22 de março de 2017"
output: html_document
---

<div style='text-align:justify'>
















# Introdução
A licitação é um processo utilizado pela administração pública como meio de contratar obras e serviços, adquirir produtos e realizar locações selecionando a proposta mais vantajosa e de maior qualidade entre diversas propostas oferecidas. Definido pela lei 8666/1993, o processo licitatório deve seguir os princípios de isonomia, transparência e impessoalidade.  
Uma das utilizações dos processos licitatórios diz respeito à compra de alimentação escolar, ou merenda. No passado recente, diversas irregularidades foram encontradas nessa área, que vem se mostrando como uma das favoritas para a realização de desvios e superfaturamentos. {[1](http://paraibaonline.com.br/balanco-da-cgu-revela-desvios-de-r-2-bilhoes-da-merenda-escolar/)}{[2](http://www.paraiba.com.br/2017/02/25/12605-ministerio-da-transparencia-fiscaliza-prefeituras-da-pb-e-constata-superfaturamento-de-merenda-escolar)}  
O objetivo dessa análise é descrever como se dá a realização de licitações para compra de merenda no estado da Paraíba, observando tendências e discrepâncias que possam surgir. Ao final, espera-se ainda obter um panorama que auxilie os cidadãos a perceber a forma como o dinheiro público está sendo investido, aumentando seus poderes fiscalizadores.

<br>

# Análise  
## 1 - Qual o número total de licitações feitas por ano entre 2010 e 2016?
Para responder a essa pergunta utilizou-se todos os dados referentes a licitações entre os anos de 2010 até 2016. Esse intervalo foi escolhido pois é o que apresenta a grande maioria do número de licitações. O objetivo seria identificar se existe uma tendência anual para o número de licitações em toda a Paraíba ou se existe algum ano que o número de licitações é muito diferente dos demais.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/total de licitacoes na paraiba-1.png" title="Figura 01" alt="Figura 01" style="display: block; margin: auto;" />

Segundo o gráfico acima percebe-se que no ano de 2010 cerca de 65084 licitações foram realizadas, esse valor é bem superior se comparado com os anos seguintes. No ano de 2016 é observado uma queda do número de licitações, isso se deve ao fato de que os dados observados possuem licitações até maio de 2016, ao contrário dos outros anos em que os dados possuem todos os meses.

<br>

## 2 - Qual o número de licitações feitas por ano em João Pessoa em relação ao número de licitações feitas na Paraíba?
Em seguida, buscamos verificar como a capital e maior cidade da Paraíba aparece nos dados de licitação. Buscou-se verificar se a mesma possui uma parcela significativa no número de licitações com relação a todo o Estado.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-1-1.png" title="Figura 02" alt="Figura 02" style="display: block; margin: auto;" />

Pelo gráfico fica claro que entre 2011 e 2014 o número de licitações feitas em João Pessoa possui um valor semelhante, mas em 2015 esse valor em relação ao total de licitações no estado aumenta muito. Inicialmente, somente por este gráfico não é possível saber a causa dessa diferença entre 2015 e os outros anos.

<br>

## 3 - Qual o número de licitações que envolvem as palavras merenda e alimentação escolar?
Agora que já entendemos um pouco sobre como o número de licitações se comportam ao longo do ano, e algumas tendências e anomalias, buscamos responder essa pergunta filtrando apenas as licitações que possuem em sua descrição as seguintes sentenças: "Merenda" e "Alimentação escolar". O filtro foi feito ignorando acentos e caixa alta.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-2-1.png" title="Figura 03" alt="Figura 03" style="display: block; margin: auto;" />

Pelo gráfico nota-se que novamente em 2010 cerca de 1405 licitações envolvendo merenda foram feitas, número esse bem grande se comparado a outros anos entre 2011 e 2015 (947 licitações). O ano de 2016 possui um baixo número de licitações envolvendo merenda já que os dados estão atualizados até maio de 2016.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-3-1.png" title="Figura 04" alt="Figura 04" style="display: block; margin: auto;" />

Se compararmos os dois gráficos (o número total de licitações por ano e o número total de licitações envolvendo merenda por ano) nota-se que licitações envolvendo merenda representam uma pequena parcela do universo de licitações. A partir daqui, vamos buscar analisar de forma mais específica essa pequena parcela e responder mais algumas perguntas.

<br>

## 4 - Qual a distribuição do número de licitações que envolvem merenda nos municípios da Paraíba?






Para responder a essa pergunta iremos utilizar o mapa de municípios da paraíba par obter a distribuição geográfica dos municípios da Paraíba e o número total de licitações relacionadas a merenda realizadas em todos os anos investigados(2010-2016). O mapa com os municípios foi retirado do site da AESA{[3](http://www.aesa.pb.gov.br/geoprocessamento/geoportal/shapes.html)}.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-7-1.png" title="Figura 05" alt="Figura 05" style="display: block; margin: auto;" />


Observou-se que alguns municípios, como Santa Rita e Monteiro realizaram um maior número de licitações no período do que os demais municípios. A capital João Pessoa apresentou um número baixo de licitações relacionadas a merenda se comparada a esses dois municípios citados a pouco, apenas 3 licitações. Ao olhar o mapa vemos que alguns municípios possuem um total de licitações próximo, e inclusive são municípios vizinhos. Só por esse mapa não é possível concluir se o tamanho, população e outras características podem influenciar na forma com que os municípios lidam com as licitações de merenda, nem se municípios com características parecidas lidam também de forma parecida com a merenda escolar. Mais tarde nessa análise trataremos mais sobre como as características dos municípios, como a população, influenciam nas variáveis de merenda no conjunto de dados.

<br>

## 5 - Em que período do ano ocorrem mais licitações de merenda? {#perg-5}
Seguindo com a análise feita nas perguntas anteriores, buscou-se verificar se há algum período do ano que concentra mais licitações de merenda.  
Aqui, foram analisados apenas os dados no período compreendido entre os anos 2011 e 2015 e observou-se que o intervalo entre os meses de fevereiro e abril concentra a maioria das licitações de merenda e que o número de licitações desse tipo decai conforme nos aproximamos dos meses finais do ano.  
Segundo o gráfico abaixo, podemos ainda observar que tal concentração se dá exatamente nos primeiros meses da volta às aulas da escolas, onde possivelmente são firmados contratos anuais de distribuição de alimentação escolar. 

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-8-1.png" title="Figura 06" alt="Figura 06" style="display: block; margin: auto;" />

<br>

## 6 - Qual a média do valor da licitação por merenda?
Até aqui trabalhamos com o número total de licitações, a seguir vamos buscar entender como o valor da licitação se comporta.  
Inicialmente, determinamos a média e a mediana do valor (em reais) de licitações envolvendo merenda, como mostrado a seguir.

| Media | 1.9394484 &times; 10<sup>5</sup> |
|:-----:|:------:|

<br>

## 7 - Qual a mediana do valor da licitação por merenda?
| Mediana | 7.683052 &times; 10<sup>4</sup> |
|:-------:|:------:|


Nota-se que a diferença entre a média e a mediana é de 117114.3 reais, isso pode indicar que a média não é uma boa medida para representar os dados de licitações quando estamos trabalhando com merenda. A causa disso é que alguns valores de licitação muito altos estão influenciando a média causando essa diferença.

<br>

## 8 - Qual o comportamento da média e da mediana do valor das licitações de merenda ao longo dos anos (2010-2016)?
No gráfico a seguir mostramos como o valor da média (preto) e da mediana (azul) se comporta entre os anos de 2010 e 2016.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-9-1.png" title="Figura 07" alt="Figura 07" style="display: block; margin: auto;" />

Observamos que a média sempre está acima da mediana. No ano de 2010 elas estavam bem próximas, mas nos anos seguintes a tendência foi a diferença aumentar, principalmente em 2014. Nesse ano algumas licitações de alto valor foram realizadas, o que afetou a média. Outra coisa que é possível perceber a partir desse gráfico é que, em geral, o valor das licitações que envolvem merenda aumentaram com o tempo.

<br>

## 9 - Qual a distribuição do valor médio de licitações de merenda escolar entre todos os municípios da Paraíba? 
Para responder a essa pergunta consideramos todas as licitações que envolvem merenda na Paraíba e os respectivos valores das licitações e determinamos a média desse valor por município. Em seguida, utilizamos o mapa abaixo para observar os resultados.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-10-1.png" title="Figura 08" alt="Figura 08" style="display: block; margin: auto;" />

É notado que João Pessoa foi a cidade que obteve o maior valor médio de licitação de merenda em todo o estado. Em geral, poucas cidades gastam mais de 1 milhão por licitação de merenda. E a maior parte deles tem valor médio de licitação entre 50 e 500 mil reais.

<br>

## 10 - Geralmente, quantas propostas são recebidas para licitações de merenda? {#perg-10}
Aqui, busca-se compreender como está distribuído o total de propostas para as licitações de merenda. A partir dessa análise é possível perceber se há muitos interessados nesse tipo de licitação e se algum valor mais comum ou discrepante.
Conforme descrito na figura 09, é possível observar que grande parte das licitações de merenda (92.66%) recebeu menos de 5 propostas.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-11-1.png" title="Figura 09" alt="Figura 09" style="display: block; margin: auto;" />

É possível ainda, restringir a abrangência do gráfico à área de maior concentração e perceber que a maioria das licitações de merenda (53.54%) recebeu apenas 3 propostas.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-12-1.png" title="Figura 10" alt="Figura 10" style="display: block; margin: auto;" />

Por outro lado, há 2 licitações cujo número de participantes passa dos 25, desviando-se mais de 10 vezes do número médio de participantes das demais. Uma dessas licitações foi realizada em João Pessoa em 2015, enquanto a outra, foi realizada em Monteiro no ano de 2014. 
Os detalhes desses dois processos podem ser observados na tabela abaixo.

| Cidade | Ano | Propostas | Valor(R$) |
|:------:|:---:|:---------:|:---------:|
|João Pessoa|2015|31|25.078.839,00|
|Monteiro|2014|50|250.911,00|

<br>

## 11 - Que tipo de licitação é mais comum na compra de merenda? {#perg-11}
A seguir, buscamos entender se há algum tipo de licitação mais comum ou padrão a ser utilizado na compra de alimentação escolar. Aqui, foi possível observar a maior parte das licitações de merenda fazem parte das modalidades convite e pregão presencial. Outros tipos como concorrência, tomada de preços e chamada pública também são amplamente utilizados. Um número expressivo de licitações, ainda, é considerado dispensável.  

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-13-1.png" title="Figura 11" alt="Figura 11" style="display: block; margin: auto;" />


<br>

## 12 - O valor médio da licitação alterou ao longo dos anos com relação aos tipos de licitação?
Outra variável interessante de se analisar nos dados é o tipo de licitação. Será que o valor médio(em reais) de licitação varia com o seu tipo ou ainda se esse valor também sofre influência do ano em que a licitação foi realizada. Essas são algumas questões que o gráfico a seguir pode responder.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-14-1.png" title="Figura 12" alt="Figura 12" style="display: block; margin: auto;" />

Observou-se que algumas modalidades de licitações não possuem valores médios em alguns anos, isso ocorre porque não houve licitações daquele tipo naquele ano. Alguns tipos de licitações se destacam por seu valor médio parecido e acima dos demais, são elas: Pregão (Eletrônico e Presencial), Adesão a Registro de Preço e Tomada de preços. Algumas modalidades possuem valores limites, por exemplo, Licitações por Convite não podem ter valor superior a 80 mil reais, isso fica claro no gráfico já que a média de licitações dessa modalidade fica em torno desse valor. Além disso, em geral, o valor médio das licitações aumentaram com os anos em praticamente todos os tipos de licitação.

A partir dessa resposta faz-se necessário saber se existem licitações de merenda da modalidade de Convite que ultrapassam o valor limite de 80.000 mil reais previsto pela Lei 8666. Descobrimos que 8 licitações possuem valor acima do limite. Essa inconsistência pode ser melhor investigada em análises futuras.

<br>

## 13 - A popularidade de alguma modalidade de licitação mudou ao longo dos anos? {#perg-13}
Dando prosseguimento à análise, foi verificado quais modalidades de licitação foram mais utilizadas para a obtenção de merenda entre os anos 2010 e 2015. Os resultados podem ser observados na figura 13.  

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-15-1.png" title="Figura 13" alt="Figura 13" style="display: block; margin: auto;" />

É interessante observar o grande número de licitações da modalidade convite no ano 2010, apresentando um claro outlier em relação aos anos posteriores. A que se deveria tamanha discrepância?  
Analisando apenas os dados referentes ao período entre os anos 2011 e 2015, podemos observar um padrão diferente na distribuição das modalidades de licitação. O resultado pode ser visto no gráfico abaixo. 

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-16-1.png" title="Figura 14" alt="Figura 14" style="display: block; margin: auto;" />

A modalidade de licitação mais utilizada para a obtenção de merenda no período observado foi o pregão, seja ele eletrônico ou presencial, e sua utilização ainda está em ascenção.  
Se por um lado a utilização do pregão apresentou popularidade ascendente no período, por outro, a popularidade das licitações da modalidade convite apresentaram uma queda considerável, chegando quase a 0 nos anos 2014 e 2015.  
Ainda há outros pontos importantes a serem ressaltados nesse tópico. É possível observar, por exemplo, que há uma grande diferença entre o total de licitações dispensadas em 2013 e o de seus anos vizinhos e que a modalidade chamada pública começou a ser utilizada apenas no ano referido anteriormente.    

<br>

## 14 - Em geral, as licitaçoes mais caras estao concentradas em alguma época do ano? {#perg-14}
Analisando novamente vez os dados do período entre 2011 e 2015, foi percebido que as licitações mais caras estão concentradas nos primeiros seis meses do ano, possuindo distribuição semelhante à do total de licitações realizadas. Interligando o resultado dessa pergunta com o obtido em \#[5](#perg-5), é possível dizer que nos primeiros seis meses do ano são realizados mais processos licitatórios, que geralmente vem a ser os mais caros também.  

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-17-1.png" title="Figura 15" alt="Figura 15" style="display: block; margin: auto;" />


<br>

## 15 - O valor da licitação está relacionado com o total de propostas recebidas? {#perg-15}
Para tentar responder essa pergunta, foi criado um gráfico de dispersão do valor das licitações pelo total de propostas. Além disso, o coeficiente de correlação linear entre as variáveis foi calculado.  

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-18-1.png" title="Figura 16" alt="Figura 16" style="display: block; margin: auto;" />

Observando a figura acima observamos que aparentemente não há relação linear entre as duas variáveis. Isso pode ser comprovado pelo valor do coeficiente de correlação linear entre elas, que é de 0.23.  

É possível, ainda, aproximar o gráfico da área que contém a maior concentração de pontos e recalcular a correlação entre as variáveis.  

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-19-1.png" title="Figura 17" alt="Figura 17" style="display: block; margin: auto;" />

Agora observamos que há ainda menos indícios de uma correlação linear entre as duas variáveis. Isso pode ser comprovado, mais uma vez, pelo valor do coeficiente de correlação linear entre elas, que diminuiu e passou a ser de -0.03.  

<br>

## 16 - Qual a relação entre o total de licitações de merenda e o número de propostas por modalidade?
Para responder a essa pergunta iremos considerar, inicialmente, os anos de 2010 até 2016. A figura abaixo mostra a frequência de licitações de acordo com o número de propostas. Limitamos o número de propostas para no máximo 6 já que esse intervalo(1:6) contém 96% dos dados de merenda. O 96º percentil é 6.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-20-1.png" title="Figura 18" alt="Figura 18" style="display: block; margin: auto;" />

Observou-se que a modalidade que mais possui licitações é Convite, e a maioria das licitações dessa modalidade possuem 3 propostas, isso ocorre devido ao número mínimo de participantes de uma licitação dessa modalidade que é 3, estabelecido pela Lei Nº 8666.

A interpretação do gráfico nos levou a outra pergunta: existem licitações de merenda da modalidade convite com número de propostas inferior ao número mínimo(3) exigido por Lei?
Encontramos 44 licitações de merenda que são da modalidade Convite e possuem menos de 3 propostas, o que não é permitido por Lei.

No ano de 2010, 76.6 % das licitações de merenda são da modalidade convite, totalizando 1076 licitações. Se retirarmos esse ano da nossa análise podemos melhor identificar que outras modalidades, com relação ao número de propostas, são mais frequentes.

<img src="/knitr-jekyllfigure/source/merenda/comprador-interativo/unnamed-chunk-21-1.png" title="Figura 19" alt="Figura 19" style="display: block; margin: auto;" />


Ao considerarmos as licitações de merenda feitas a partir de 2011 percebemos que a frequência de licitações da modalidade Convite diminui bastante, mas permanece sendo mais frequente quando o número de propostas é igual a 3. A modalidade de Pregão(Eletrônico e presencial) em grande parte das licitações possui apenas 1 proposta. Pelos dados não é possível concluir a razão pela qual o número de licitações de convite é tão superior em 2010 em relação a outros anos.  

<br>

# Conclusao
TODO

</div>

<br><br>
