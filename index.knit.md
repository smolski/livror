--- 
title: "Software R: Análise estatística de dados utilizando um programa livre"
author: 
- Felipe Micail da Silva Smolski
- Iara Denise Endruweit Battisti
date: "2018-12-10"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: authoryear
link-citations: yes
github-repo: rstub/bookdown-chapterbib
url: 'http\://rstub.github.io/bookdown-chapterbib/'
description: "Curso de análise estatística com R da UFFS Cerro Largo - RS"
fontsize: 12pt
lang: pt-Br
always_allow_html: yes
classoption: oneside
---





# Apresentação {-}

A necessidade de flexibilidade e robustez para a análise estatística fez com que fosse criado, na década de 1990, a linguagem de programação R. Capitaneado pelos desenvolvedores Ross Ihaka e Robert Gentleman, dois estatísticos da Universidade de Auckland na Nova Zelândia, o projeto foi uma grande evolução para a análise de dados. A partir de então, a ideia inicial de proporcionar autonomia ao pesquisador, viu na expansão do acesso à internet uma oportunidade para que a pesquisa científica se tornasse cada vez mais colaborativa. Ao mesmo tempo, os códigos e rotinas se tornaram facilmente disponibilizáveis na rede, aumentando a reprodução e replicação dos estudos, práticas estas que podem tornar as análises mais confiáveis.

A linguagem de programação R trouxe consigo inúmeras vantagens aos pesquisadores. Dentre elas, pode-se dizer primeiramente que, basicamente o R trabalha com uma extensa relação de modelos estatísticos, que vão desde a modelagem linear e não-linear, a análise de séries temporais, os testes estatísticos clássicos, análise de grupamento e classificação, etc. Não bastasse este fato, é possível a apresentação gráfica dos resultados contando com variadas técnicas, passando também pela criação e manipulação de mapas.

Outra questão importante é que o R possui uma comunidade ativa de desenvolvedores, que se expande regularmente. Isto faz com que as técnicas de análise de dados atinjam pesquisadores de variadas disciplinas ao longo do planeta. Inclusive, concebe que o desenvolvimento dos pacotes melhorem constantemente. No ano de 2018, já haviam mais de 12.700 pacotes disponibilizados. Não menos importante, talvez o essencial: o programa é livre, ao passo que entrega o estado da arte da estatística ao usuário.

Outro progresso significativo na utilização do R foi a criação do *software* RStudio, a partir de 2010. Este, por sua vez, se configura em um ambiente integrado com o R e com inúmeras linguagens de marcação de texto (exemplos LaTeX, Markdown, HTML). Possui igualmente versão livre que disponibiliza ao pesquisador a execução, guarda, retomada e manipulação dos códigos de programação diretamente em seu console, bem como a administração de diretórios de trabalhos e projetos.

O material aqui criado é destinado não somente a alunos de graduação, pós-graduação, professores e pesquisadores acadêmicos, mas também para qualquer indivíduo interessado no aprendizado inicial sobre a utilização de técnicas estatísticas com o R. Inclusive, com o objetivo de alcançar um público das mais variadas áreas do conhecimento, esta obra foi elaborada com exemplos gerais, a serem absorvidos em um momento inicial do estudante. Assim, possui a base para continuar estudos posteriores em estatística e no *software* RStudio. O sistema operacional aqui utilizado é o Windows 10. Importante mencionar que este livro origionu-se de projeto de extensão aprovado no Edital de Apoio a Programas de Extensão (Nº 522/GR/UFFS/2016) da Universidade Federal da Fronteira Sul (UFFS).

Este livro está organizado da seguinte maneira: no capítulo [1](#intro) [**Primeiros Passos com o R**], busca-se instruir o pesquisador para a instalação dos programas necessários para acessar o ambiente de programação, bem como orientar sobre a usabilidade do programa em suas funções básicas de carregamento de bases de dados, criação de objetos e princípios de manipulação. 

Já no capítulo [2](#desc) [**Estatística Descritiva**], leva o leitor ao encontro das técnicas básicas para descrever as variáveis em bancos de dados, como exemplos a média, mínima, máxima, desvio padrão, os quartis e também, apresentar os princípios dos elementos gráficos de apresentação dos dados. 

O capítulo [3](#inf) [**Estatística Inferencial**] tratará dos métodos de determinação de intervalos de confiança (média e proporção), testes de hipóteses (verificar a normalidade dos dados) e das comparações entre médias de amostras dependentes e independentes. 

No capítulo [4](#qui) [**Teste de Qui-Quadrado**], serão abordadas as referidas técnicas para verificação de asssociação entre duas variáveis qualitativas e de aderência a uma distribuição.

No capítulo [5](#reg) [**Modelos de Regressão**] serão introduzidos os conhecimentos sobre as técnicas de análise de correlação e regressão linear simples, bem como sobre o diagrama de dispersão, método dos mínimos quadrados, análise de variância, coeficiente e intervalo de predição, da análise dos resíduos e dos princípios de regressão múltipla.

A criação de documentos dinâmicos utilizando o RStudio será tratada no capítulo [6](#rmark) [**RMarkdown**]. O pesquisador poderá conhecer as formas de integrar a programação no R e a manipulação de bases de dados, criando, compilando e configurando relatórios finais em diversos formatos (HTML, PDF e Word/Libre/Open Office).

Boa leitura!

# Introdução{#intro}

*Felipe Micail da Silva Smolski*

*Djaina Sibiani Rieger*

\begin{flushright}
\emph{}

\emph{}
\end{flushright}

O R é um ambiente voltado para análise de dados com o uso de uma linguagem de programação, frente a isso um conhecimento prévio dos príncipios de programação facilita a compreensão da condução das análises aplicadas no software. Entretanto, não é pré-requisito. Neste capítulo abordaremos os primeiros passos para o emprego da linguagem de programação R utilizando uma interface "amigável" - o software RStudio. Além disso, serão apresentados os comandos básicos para a manipulação de dados dentro do RStudio.


## Download e instalação do R e Rstudio


**R**: <http://www.r-project.org>. Clique em Download (CRAN) - escolha o link de um repositório - clique no link do sistema operacional (Linux, Mac ou Windows) - clique em *install R for de first time - Download*. 

**RStudio**: <http://www.rstudio.com/products/rstudio/download>. Em RStudio Desktop, escolha a versão *free*, seguidas da opção do sistema operacional do usuário.

Lembrando que:

- R é o software;
- RStudio é uma ferramenta amigável para o R.


## Painéis

O RStudio é a interface que faz com que seja mais fácil a utilização da programação em R. 

<div class="figure" style="text-align: center">
<img src="paineis.png" alt="Painéis do Rstudio" width="80%" />
<p class="caption">(\#fig:paineis1)Painéis do Rstudio</p>
</div>
Fonte: Elaborado pelo(s) autor(es).

- **Fonte/Editor de Scripts**: se constitui do ambiente onde serão abertos os scripts previamente salvos nos mais diversos formatos ou mesmo sendo o local de visualização das bases de dados.
- **Console**: local onde será efetuada a digitação das linhas de código que serão interpretadas pelo R.
- **Ambiente e Histórico**: o ambiente será visualizado os objetos criados ou carregados durante a seção e; a aba History retoma os scripts digitados no console.
- **Plots/arquivos/Pacotes**: local onde podem ser acessados os arquivos salvos no computador pela aba *files*; a aba *Plots* carrega os gráficos e plotagens; a aba *Packages* contém os pacotes instalados em seu computador, onde são ativados ou instalados novos; em *Help* constam as ajudas e explicações dos pacotes e; *Viewer* vizualiza documentos do tipo html.

## Help

Acessamos a ajuda do RStudio por meio do comando `help()`, através da aba "Help" ou ao clicar no nome do pacote. Pode-se digitar a ajuda que usuário necessita (exemplo `help("summary")`), ou diretamente no colsole digitamos ? e a função desejada, exemplo: `?mean`.

## Instalação de pacotes

Em alguns situações, o uso de pacotes pode dar ao trabalho mais praticidade, e para isso se faz necessário efetuar a sua instalação. Precisamos ir até o painel dos pacotes em *packages*, selecionar a opção instalar e inserir o nome do pacote desejado na janela indicada. Ao selecionar a opção instalar, no console receberemos informações do procedimento e do sucesso do mesmo. 


<div class="figure" style="text-align: center">
<img src="pacotes1.png" alt="Instalação de pacotes" width="80%" />
<p class="caption">(\#fig:pacotes1)Instalação de pacotes</p>
</div>

Fonte: Elaborado pelo(s) autor(es).

<div class="figure" style="text-align: center">
<img src="pacotes2.png" alt="Caixa de informação de pacote a ser instalado" width="80%" />
<p class="caption">(\#fig:pacotes2)Caixa de informação de pacote a ser instalado</p>
</div>

Fonte: Elaborado pelo(s) autor(es)

A mesma função, para instalação de um pacote, pode ser efetuada diretamente via console: `install.packages("pacote")`. É importante ressaltar a função `library(nomedopacote)` que é utilizada no console para informar ao R e "carregar" o pacote que o usuário irá utilizar. Podem ser instalados mais de um pacote ao mesmo tempo, como no exemplo:


`install.packages(c("readr", "readxl"))`

## Abrir arquivo de dados

Dispondo de um banco de dados em uma planilha eletrônica (LibreOffice Calc ou EXCEL), neste caso será utilizado o arquivo  [árvores](https://github.com/Smolski/softwarelivrer/raw/master/basico/arvores.xlsx) como exemplo o banco de dados. Os dados derivam de uma pesquisa com espécies de árvores registrando as variáveis diâmetro altura do peito (DAP) e altura. Dados cedidos pela professora Tatiane Chassot.

Pode-se utilizar a linha de comando para carregar os arquivos de dados, da seguinte forma:

`library(readxl)`

`nome.objeto.xls = read_excel("d:/arvores.xls")`

Outras opções de arquivos podem ser carregados no RStudio, como por exemplo arquivos de texto (.txt ou .csv), arquivos derivados do excel (.xls ou .xlsx), arquivos de dados do SPSS (.sav), do *software* SAS (.sas7bdat) e do STATA (.dta). A instalação de alguns pacotes é requerida, dependendo da origem da base de dados, como por exemplo o `readxl`, `readr` e `haven`, como os exemplos abaixo:

`library(readr)`

`nomeobjeto = read.csv("d:/arvores.csv")`

`library(haven)` 

`nomeobjeto = read_sav("d:/arvores.sav")`

`nomeobjeto = read_dta("d:/arvores.dta")`

`nomeobjeto = read_sas("d:/arvores.sas7bdat")`

Outras opções podem ser comandadas dentro destes comando para abertura de arquivos, como por exemplo, um arquivo csv em que esteja separado por vírgulas pode ser lido como:

`read.csv("d:/arvores.csv", sep=",")`

O comando `header=TRUE` diz que a primeira linha do arquivo contém o cabeçalho; `skip=4` faz com que sejam ignoradas as 4 primeiras linhas.

A função `load()` (exemplo: `load("base.RData")`) pode ser utilizada para carregar as bases de dados salvas com a função `save()`, que será descrita no subcapítulo a seguir.

Outra opção é o carregamento das bases de dados manualmente pelo caminho *Envoirment $>$ Import Dataset*, escolhendo o tipo de arquivo:

<div class="figure" style="text-align: center">
<img src="r3.png" alt="Aba Import Dataset" width="80%" />
<p class="caption">(\#fig:r3)Aba Import Dataset</p>
</div>

Fonte: Elaborado pelo(s) autor(es).

Na caixa correspondente a File/Url se insere o endereço virtual ou o local onde se encontra o arquivo. Ao importar os dados, carrega-se um objeto criado com as informações contidas no arquivo. No nosso exeplo, carregamos a planilha arvores (arquivo .xls) como mostra a Figura \@ref(fig:r4), derivado do caminho "Import Dataset $>$ From Excel" do Environment.

<div class="figure" style="text-align: center">
<img src="r4.png" alt="Caixa de informações do Import Data" width="80%" />
<p class="caption">(\#fig:r4)Caixa de informações do Import Data</p>
</div>
Fonte: Elaborado pelo(s) autor(es).

O campo *Code Preview* mostra o comando que está sendo criado para a importação destes dados. Em *Import Options*, delimita-se opções do objeto como o nome (*name*), o número máximo de linhas (*Max Rows*), quantas linhas serão puladas na importação do arquivo (*Skip*), o tratamento das células em branco (*NA*) e se a primeira linha contém os nomes (*Firts Row as Names*).

Com relação à importação de arquivos de texto separado por caracteres (.csv), ela se dá via "Import Dataset $>$ From Text (readr)" do Environment. Constam algumas solicitações diferentes a serem determinadas pelo usuário no campo *Import Options*, conforme mostra a Figura \@ref(fig:r4csv). Uma questão importante é a opção *Delimiter*, a qual o pesquisador tem que prestar atenção quando o arquivo está separado por vírgulas (*Comma*), ponto e vírgula (*Semicolon*) ou outro tipo de caractere. A opção *Locale $>$ Configure...* oportuniza determinar os tipos de marca decimal e codificação de textos, por exemplo.

<div class="figure" style="text-align: center">
<img src="r4csv.png" alt="Opções da importação de arquivos .csv" width="80%" />
<p class="caption">(\#fig:r4csv)Opções da importação de arquivos .csv</p>
</div>

Fonte: Elaborado pelo(s) autor(es)

Importante mencionar que em ambos os casos de importação, no campo *Dada Preview* onde constam os dados do arquivo a ser importado, é possível determinar o tipo de dado que cada "coluna" contém. Isto é extremamente importante, pois campos que possuem números, que serão posteriormente utilizados em operações aritméticas, por exemplo, devem ser configurados como tal. No entanto, como será visto adiante, a alteração do tipo do dado também pode ser feita posteriormente sem problema algum.

Alguns tipos de dados:

- **Numeric**: números, valores decimais em geral (`5.4`).
- **Integer**: números (`4`).
- **Character**: variável de texto, ou *string* (`casa`).
- **Double**: cria um vetor de precisão dupla, que abarca os números.
- **Logical**: operadores booleanos (`TRUE, FALSE`).
- **Date**: opção para datas.
- **Time**: vetor para séries de tempo.
- **Factor**: variável nominal, inclusive como fator ordenado, representam categorias.

Ainda, é possível importar objetos utilizando arquivos hospedados em links da internet, por exemplo o comando  `source("http://www.openintro.org/stat/data/cdc.R")` utiliza a função `source()` para carregar um objeto do R denominado cdc ("cdc.R").

## Salvar arquivo de dados

O banco de dados que o R armazena na memória pode ser salvo, junto com todo o ambiente, usando o ícone de disquete na aba "Environment" (salva como arquivo .RData), e depois carregado pelo ícone de pasta (Abrir dados...) na mesma aba. Desta forma, salvará todos os objetos criados no ambiente de trabalho.

<div class="figure" style="text-align: center">
<img src="r6.png" alt="Atalho para abrir e salvar arquivo de dados" width="80%" />
<p class="caption">(\#fig:r6)Atalho para abrir e salvar arquivo de dados</p>
</div>

Fonte: Elaborado pelo(s) autor(es)

Outra opção com mesmo efeito é utilizar o comando a seguir diretamente no console do RStudio: 

`save("nomeDoObjeto",file="nomeDoArquivo.RData")`

O nome do objeto pode ser uma lista de objetos para salvar mais de um objeto do ambiente, `list=("objeto1", "objeto2")`. Para carregar um arquivo RData no ambiente, o comando a ser utilizado pelo usuário é 

`load("arquivo.RData")`,

desde que o arquivo esteja no diretório de trabalho do R.

É possível exportar as bases trabalhadas para vários formatos de arquivos de dados e de texto, como seguem alguns exemplos:

- `write.csv(nomeobjeto,"file.csv", sep=";")`: salvando em arquivo csv.
- `write.foreign(nomeobjeto,"d:/nome.sps")`: arquivos sps.
- `write.foreign(nomeobjeto,"d:/nome.dta")`: arquivos dta.
- `write.foreign(nomeobjeto,"d:/nome.sas7bdat")`: arquivos sas7bdat.

## Diretórios de trabalho

Os trabalhos efetudados via Rstudio, incluindo as bases de dados, os objetos, os resultados das fórmulas, os cálculos aplicados sobre os vetores e demais arquivos resultantes da utilização do programa podem ser salvos em seu diretório de arquivos. Após instalado o Rstudio  destina um diretório padrão salvar estes arquivos, o qual pode ser verificado com o comando `getwd()`. 

Este caminho padrão, por sua vez, pode ser alterado via comando

`setwd("C://file/path")`

onde o usuário escolhe a pasta desejada que ficará como padrão. O comando `dir()` mostra ao usuário os documentos que constam no diretório padrão ou o escolhido para a consulta.

## Operações

### Operações Aritméticas

A realização de uma operação aritmética no R acontece da seguinte forma: onde a resolução das operações segue o padrão, ou seja, primeiro exponenciações, seguido de multiplicações e divisões, deixando por ultimo adições e subtrações, de acordo com a ordem que estão dispostas. Para alterar a prioridade da resolução de operações fazemos o uso do parenteses para destacar a operação que deve ser prioritária na resolução. Seguem alguns exemplos efetuados diretamente no console do RStudio:


```r
# soma
19+26
```

```
[1] 45
```

```r
# subtração
19-26
```

```
[1] -7
```

```r
# divisão
4/2
```

```
[1] 2
```

```r
# multiplicação 
4*2
```

```
[1] 8
```

```r
# exponenciação
4^2
```

```
[1] 16
```

```r
# prioridade de resolução
19 + 26 /4 -2 *10
```

```
[1] 5.5
```

```r
((19 + 26) /(4 -2))*10
```

```
[1] 225
```

```r
# raiz quadrada
sqrt(16)
```

```
[1] 4
```

```r
# Logaritmo 
log(1)
```

```
[1] 0
```

### Operações Lógicas

O ambiente de programação Rstudio trabalha com algumas operações lógicas, que serão importantes na manipulação de bases de dados:

- $a == b$ ("a" é igual a "b")
- $a != b$ ("a" é diferente a "b")
- $a > b$ ("a" é maior que "b")
- $a < b$ ("a" é menor  que "b")
- $a >= b$ ("a" é maior ou igual a "b")
- $a <= b$ ("a" é menor ou igual a "b")
- is.na ("a" é missing - faltante)
- is.null ("a" é nulo)

Seguem alguns exemplos da aplicação das operações lógicas:


```r
# maior que 
2 > 1
```

```
[1] TRUE
```

```r
1 > 2
```

```
[1] FALSE
```

```r
# menor que 
1 < 2
```

```
[1] TRUE
```

```r
# maior ou igual a 
0 >= (2+(-2))
```

```
[1] TRUE
```

```r
# menor ou igual a 
1 <= 3
```

```
[1] TRUE
```

```r
# conjunção
9 > 11 & 0 < 1
```

```
[1] FALSE
```

```r
# ou
6 < 5 | 0 > -1
```

```
[1] TRUE
```

```r
# igual a
1 == 2/2
```

```
[1] TRUE
```

```r
# diferente de
1 != 2
```

```
[1] TRUE
```

## Criação de objetos

A linguagem de programação R se configura em uma linguagem orientada a objetos, ou seja, a todo tempo estamos criando diversos tipos de objetos e efetuando operações com os mesmos. Por exemplo, a criação de listas, bases de dados, união de bases de dados, data.frames e até mesmo mapas!


```r
#Criando um objeto simples
objeto = "meu primeiro objeto" #enter
#Agora para retomar o objeto criado:
objeto #enter
```

```
[1] "meu primeiro objeto"
```

```r
#Pode ser efetuada uma operação:
a= 2+1
a
```

```
[1] 3
```

O comando `ls()` lista todos os objetos que estão criados no ambiente e `rm(x)` remove o objeto indicado (x). Para remover todos os objetos de uma só vez utiliza-se `rm(list=ls())`.


```r
#Lista objetos do ambiente
ls()
```

```
[1] "a"      "objeto"
```

```r
#Remover um banco de dados
rm(a)
```

**Conversão de uma variável**

Para a aplicação de algumas funções é importante que cada variável esteja corretamente classificada, o que em alguns casos não ocorre durante o reconhecimento automático do R. Precisamos então reconhecê-la como variável texto, numérica ou fator. Além disso, a classe ordered se aplica a variáveis categóricas que podem ser consideradas ordenáveis.


```r
idade=c('11', '12', '31')
nomes=c("Elisa", "Priscila", "Carol")
cep=c(98700000,98701000,98702000)
idade= as.numeric(idade)
idade
```

```
[1] 11 12 31
```

```r
cep = as.character(cep)
cep
```

```
[1] "98700000" "98701000" "98702000"
```

## Algumas funções e comandos essenciais

A função `head()` mostra as 6 primeiras colunas do arquivo para se ter uma noção do conteúdo. No caso do mesmo ser um data.frame, podemos solicitar o número de valores ou linhas a serem mostrados no console através do parâmetro n ou na ausência deste, todas as linhas serão impressas, como exemplo `head(x ,n=2)` para ver as duas primeiras linhas. 

O comando `summary()` efetua o resumo dos dados, se for qualitativa mostra a frequência absoluta das categorias e se for quantitativa apresenta as categorias. No exemplo abaixo trabalharemos com uma base de dados de treinamento denominada "iris" que está acessível no *software* RStudio através do comando que carrega dados específicos `data()`:


```r
#Carregando dados da base do RSdudio iris.
data(iris)

#Visualizando as primeiras 6 colunas
head(iris)
```

```
  Sepal.Length Sepal.Width Petal.Length Petal.Width Species
1          5.1         3.5          1.4         0.2  setosa
2          4.9         3.0          1.4         0.2  setosa
3          4.7         3.2          1.3         0.2  setosa
4          4.6         3.1          1.5         0.2  setosa
5          5.0         3.6          1.4         0.2  setosa
6          5.4         3.9          1.7         0.4  setosa
```

```r
#Resumo do objeto
summary(iris)
```

```
  Sepal.Length   Sepal.Width    Petal.Length   Petal.Width        Species  
 Min.   :4.30   Min.   :2.00   Min.   :1.00   Min.   :0.1   setosa    :50  
 1st Qu.:5.10   1st Qu.:2.80   1st Qu.:1.60   1st Qu.:0.3   versicolor:50  
 Median :5.80   Median :3.00   Median :4.35   Median :1.3   virginica :50  
 Mean   :5.84   Mean   :3.06   Mean   :3.76   Mean   :1.2                  
 3rd Qu.:6.40   3rd Qu.:3.30   3rd Qu.:5.10   3rd Qu.:1.8                  
 Max.   :7.90   Max.   :4.40   Max.   :6.90   Max.   :2.5                  
```

O comando `names()` lista os nomes das colunas dos bancos de dados escolhidos, enquanto `tail()` mostra as últimas seis linhas.


```r
#Para visualizar os nomes das colunas dos dados:
names(iris)
```

```
[1] "Sepal.Length" "Sepal.Width"  "Petal.Length" "Petal.Width"  "Species"     
```

```r
#vizualizar as ultimas seis linhas do objetos
tail(iris)
```

```
    Sepal.Length Sepal.Width Petal.Length Petal.Width   Species
145          6.7         3.3          5.7         2.5 virginica
146          6.7         3.0          5.2         2.3 virginica
147          6.3         2.5          5.0         1.9 virginica
148          6.5         3.0          5.2         2.0 virginica
149          6.2         3.4          5.4         2.3 virginica
150          5.9         3.0          5.1         1.8 virginica
```

Para que o pesquisador conheça melhor as bases de dados em que está atuando, o comando `class()` serve para identificar o tipo de base ou dados da base. Com o exemplo abaixo constata-se que o objeto "iris" é um *data frame*, a variável "Sepal.Length" é uma variável numérica e que a variável numérica.


```r
class(iris)
```

```
[1] "data.frame"
```

```r
class(iris$Sepal.Length)
```

```
[1] "numeric"
```

```r
class(iris$Especie)
```

```
[1] "NULL"
```

Efeito semelhante possui o comando `ls.str()`:


```r
ls.str(iris)
```

```
Petal.Length :  num [1:150] 1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
Petal.Width :  num [1:150] 0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
Sepal.Length :  num [1:150] 5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
Sepal.Width :  num [1:150] 3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
Species :  Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...
```

Os comandos `ncol()` e `nrow()` mostram o número de colunas e o número de linhas do objeto, respectivamente.

### Funções *View* e *dim*

A função `View()` permite vizualizar os elementos no script do dataframe requesitado, enquando a função `dim()` (abreviatura de dimensões) fornece o número de linhas e de colunas, respectivamente.


```r
View(iris)
dim(iris)
```

```
[1] 150   5
```

Para alterar um nome de uma variável pode ser utilizado o comando colnames. No exemplo acima, vamos alterar o nome da coluna "Species" para "Especie". 


```r
#Alterar o nome da coluna, sendo que o '[5]' indica que está na quinta coluna.
colnames(iris)[5]='Especie'
```

Para selecionarmos uma coluna do objeto "iris", por exemplo a coluna "Sepal.Length", poderíamos digitar no console o comando **iris\$Sepal.Length**. O padrão de carregamento da base de dados nos obriga a dizer ao R qual é a base que quer selecionar (iris), inserindo o símbolo `$` e após o nome da coluna a qual deseja as informações. Para criar um novo objeto com esta informação, basta dizer ao R, como já visto acima, por exemplo: **novoobjeto=iris\$novacoluna**.

No entanto, para acessar os dados sem o uso do símbolo `$`, podemos usar o seguinte comando: **attach(iris)**. Assim, podemos efetuar o sumário da coluna "Petal.Width":


```r
#Definindo a função attach para o objeto 'dados'.
attach(iris)
#Efetuando o sumário de 'pop.total'.
summary(Petal.Width)
```

```
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    0.1     0.3     1.3     1.2     1.8     2.5 
```

```r
#Como a coluna 'distrito' é um fator, o sumário será 
#a contagem da quantidade de cada fator na coluna.
summary(Especie)
```

```
    setosa versicolor  virginica 
        50         50         50 
```


### Função *tapply*

O comando `tapply()` agrega os dados pelos níveis das variáveis qualitativas. Note que a coluna "Especie" possui dados em forma de fatores. Assim, para filtrarmos a informação (coluna "Sepal.Length") média por Especie, podemos utilizar:


```r
#Função 'tapply', número médio da população total por distrito.
tapply(Sepal.Length, Especie, mean)
```

```
    setosa versicolor  virginica 
     5.006      5.936      6.588 
```

No caso da coluna "Sepal.Length", se ela possuir um registro NA (faltante), para que se efetue a média por este coluna neste quesito, há que se adicionar o parâmetro `na.rm=T`, que ignora as células faltantes para calcular-se a média:


```r
#Função 'tapply' considerando NAs:
tapply(Sepal.Length, Especie, mean)
```

```
    setosa versicolor  virginica 
     5.006      5.936      6.588 
```

```r
#Função 'tapply' sem considerar NAs:
tapply(Sepal.Length, Especie, mean, na.rm=T)
```

```
    setosa versicolor  virginica 
     5.006      5.936      6.588 
```

### Função *subset*

Utiliza-se o comando `subset()` para formar um subconjunto de dados o qual desejamos selecionar de um objeto. Por exemplo, se quisermos criar um novo objeto com somente os dados da "Especie" setosa:


```r
dadossetosa=subset(iris, Especie=='setosa')
head(dadossetosa)
```

```
  Sepal.Length Sepal.Width Petal.Length Petal.Width Especie
1          5.1         3.5          1.4         0.2  setosa
2          4.9         3.0          1.4         0.2  setosa
3          4.7         3.2          1.3         0.2  setosa
4          4.6         3.1          1.5         0.2  setosa
5          5.0         3.6          1.4         0.2  setosa
6          5.4         3.9          1.7         0.4  setosa
```

Pode ser configurado mais de uma condição para a filtragem dos dados, por exemplo, além de serem filtrados os dados referentes a Especie setosa, aquelas na qual o Sepal.Length é superior a 5. Como no exemplo, criamos um novo objeto com estas condições:


```r
dadossetosa2=subset(iris, Especie=='setosa'& Sepal.Length>5)
head(dadossetosa2)
```

```
   Sepal.Length Sepal.Width Petal.Length Petal.Width Especie
1           5.1         3.5          1.4         0.2  setosa
6           5.4         3.9          1.7         0.4  setosa
11          5.4         3.7          1.5         0.2  setosa
15          5.8         4.0          1.2         0.2  setosa
16          5.7         4.4          1.5         0.4  setosa
17          5.4         3.9          1.3         0.4  setosa
```

### Função *table*

Para contar elementos em cada nível de um fator, usa-se a função `table()`. A função pode fazer tabulações cruzadas, gerando uma tabela de contingência, esse tipo de tabela é usado para registrar observações independentes de duas ou mais variáveis aleatórias.

Para exemplo da utilização da função `table` agora com dados qualitativos (gênero e saúde), vamos utilizar a base de dados `cdc`:


```r
# Carregando a base
source("http://www.openintro.org/stat/data/cdc.R")
#Vizualizamos as primeiras linhas
head(cdc)
```

```
    genhlth exerany hlthplan smoke100 height weight wtdesire age gender
1      good       0        1        0     70    175      175  77      m
2      good       0        1        1     64    125      115  33      f
3      good       1        1        1     60    105      105  49      f
4      good       1        1        0     66    132      124  42      f
5 very good       0        1        0     61    150      130  55      f
6 very good       1        1        0     64    114      114  55      f
```

```r
# Efetuamos a contagem dos dados qualitativos com a função table
table(cdc$genhlth,cdc$gender)
```

```
           
               m    f
  excellent 2298 2359
  very good 3382 3590
  good      2722 2953
  fair       884 1135
  poor       283  394
```


## Estrutura de dados

### Vetores

Os fatores são uma classe especial de vetores, que definem variáveis categóricas de classificação, como os tratamentos em um experimento fatorial, ou categorias em uma tabela de contingência.


```r
# Criação de um vetor
c(2, 4, 6)
```

```
[1] 2 4 6
```

Os vetores podem ser criados a partir de uma sequência numérica ou mesmo de um intervalo entre valores:


```r
c(2:6)
```

```
[1] 2 3 4 5 6
```

```r
# Criação de um vetor a partir do intervalo entre cada elemento e valores
#mínimo e máximo
seq(2, 3, by=0.5)
```

```
[1] 2.0 2.5 3.0
```

Criação de um vetor atráves de uma repetição também é útil em várias situações. No primeiro exemplo repete o intervalo de 1 a 3 4 vezes e no segundo exemplo, a cada 3 vezes:


```r
rep(1:3, times=4)
```

```
 [1] 1 2 3 1 2 3 1 2 3 1 2 3
```

```r
rep(1:3, each=3)
```

```
[1] 1 1 1 2 2 2 3 3 3
```

A função factor cria um fator, a partir de um vetor:


```r
sexo<-factor(rep(c("F", "M"),each=8))
sexo
```

```
 [1] F F F F F F F F M M M M M M M M
Levels: F M
```

```r
numeros=rep(1:3,each=3)
numeros
```

```
[1] 1 1 1 2 2 2 3 3 3
```

```r
numeros.f<-factor(numeros)
numeros.f
```

```
[1] 1 1 1 2 2 2 3 3 3
Levels: 1 2 3
```


Fatores têm um atributo que especifica seus níveis ou categorias (levels), que seguem ordem alfanumérica crescente, por *default*. Em muitas análises essa ordem é de fundamental importância e dessa forma pode ser alterada através do argumento levels, por exemplo, para que possa ser colocado o controle antes dos tratamentos: 


```r
tratamentos=factor(rep(c("controle","adubo A","adubo B"), each=4))
tratamentos
```

```
 [1] controle controle controle controle adubo A  adubo A  adubo A  adubo A 
 [9] adubo B  adubo B  adubo B  adubo B 
Levels: adubo A adubo B controle
```

```r
tratamentos=factor(rep(c("controle","adubo A","adubo B"), each=4), 
levels=c("controle", "adubo A", "adubo B"))
tratamentos
```

```
 [1] controle controle controle controle adubo A  adubo A  adubo A  adubo A 
 [9] adubo B  adubo B  adubo B  adubo B 
Levels: controle adubo A adubo B
```

Fatores podem conter níveis não usados (vazios):


```r
participantes=factor(rep("mulheres",10), levels=c("mulheres","homens"))
participantes
```

```
 [1] mulheres mulheres mulheres mulheres mulheres mulheres mulheres mulheres
 [9] mulheres mulheres
Levels: mulheres homens
```
<!--
Também é possível aplicar uma função aos subconjuntos de um vetor definidos por um fator utilizando a função `tapply()`. Criamos um objeto com o sexo das pessoas, seguido pela dieta e peso (que caracterizamos como numérico). Depois, determinamos a média de peso frente ao sexo e a dieta


```r
sexo=factor(rep(c("F","M"),each=9))
dieta=factor(rep(rep(c("normal","light","diet"), each=3),2), 
levels=c("normal", "light","diet"))
peso=c(90, 89, 78, 69, 85, 69, 77, 89, 80, 60, 75, 79, 65, 94,
       69, 85, 69, 77)
sexo
```

```
 [1] F F F F F F F F F M M M M M M M M M
Levels: F M
```

```r
dieta
```

```
 [1] normal normal normal light  light  light  diet   diet   diet   normal
[11] normal normal light  light  light  diet   diet   diet  
Levels: normal light diet
```

```r
peso=as.numeric(peso)

# média de peso frente ao sexo e dieta
tapply(peso,list(sexo,dieta), mean)
```

```
  normal light diet
F  85.67 74.33   82
M  71.33 76.00   77
```
-->


### Matrizes

A função matrix tem a finalidade de criar uma matriz com os valores do argumento data, argumento este que insere as variáveis desejadas na matriz. O número de linhas é definido pelo argumento nrow e o número de colunas é definido pelo argumento ncol: 


```r
nome.da.matriz= matrix(data=1:12,nrow = 3,ncol = 4)
nome.da.matriz
```

```
     [,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12
```


Por *default* (ação tomada pelo *software*), os valores são preenchidos por coluna. Para preencher por linha basta instruir o programa de outra forma, alterando o argumento `byrow` para TRUE:


```r
nome.da.matriz= matrix(data=1:12,nrow = 3,ncol = 4, byrow=T)
nome.da.matriz
```

```
     [,1] [,2] [,3] [,4]
[1,]    1    2    3    4
[2,]    5    6    7    8
[3,]    9   10   11   12
```

Se a matriz inserida tem menos elementos do que a ordem informada para a matriz, os são repetidos até preenchê-la:


```r
lista= list(matriz=matrix(c(1,2,1), nrow=3, ncol=2))
lista
```

```
$matriz
     [,1] [,2]
[1,]    1    1
[2,]    2    2
[3,]    1    1
```

### Listas

As listas podem ser criadas a partir do comando `list()`. 

- **nrow**: corresponde ao número de linhas;
- **ncol**: corresponde ao número de colunas.

Para ver quais elementos estão em suas listas é só chamar pelo nome que foi dado para ela, como no exemplo abaixo. Representa uma coleção de objetos.


```r
lista= list(matriz=matrix(c(1,2,1,5,7,9), nrow=3, ncol=2),vetor=1:6)
lista
```

```
$matriz
     [,1] [,2]
[1,]    1    5
[2,]    2    7
[3,]    1    9

$vetor
[1] 1 2 3 4 5 6
```

**Comandos para manipulação de listas**

Para descobrirmos de maneira rápida o números de objetos que há na lista, utilizamos o comando `length(nomedalista)`.


```r
lista
```

```
$matriz
     [,1] [,2]
[1,]    1    5
[2,]    2    7
[3,]    1    9

$vetor
[1] 1 2 3 4 5 6
```

```r
length(lista)
```

```
[1] 2
```

O uso do comando `names(nomedalista)` retorna os nomes dos objetos que estão presentes na lista.


```r
names(lista)
```

```
[1] "matriz" "vetor" 
```

Para chamar várias listas através usamos o comando da seguinte forma:

`c(nome1, nome2)`


```r
lista.1= list(matriz=matrix(c(1,2,1,5,7,9), nrow=3, ncol=2),
              vetor=1:6)
lista.2= list(nomes=c("Marcelo", "Fábio", "Felipe"), 
              idade=c(25, 34, 26))
c(lista.1,lista.2)
```

```
$matriz
     [,1] [,2]
[1,]    1    5
[2,]    2    7
[3,]    1    9

$vetor
[1] 1 2 3 4 5 6

$nomes
[1] "Marcelo" "Fábio"   "Felipe" 

$idade
[1] 25 34 26
```

### Data frames

Com a função `data.frame()` reunimos vetores de mesmo comprimento em um só objeto. Neste caso são criadas tabelas de dados. Cada observação é descrita por um conjunto de propriedades. Abaixo podemos ver como inserir os dados para criar a "tabela". Similar como matrizes, porem diferentes colunas podem possuir elementos de natureza diferentes .


```r
estudantes= c("Camila", "Pedro", "Marcelo","Guilherme")
idade=c(21,17,17,18)
peso=c(65,79,80,100)
informacoes=data.frame(estudantes,idade,peso)
informacoes
```

```
  estudantes idade peso
1     Camila    21   65
2      Pedro    17   79
3    Marcelo    17   80
4  Guilherme    18  100
```

Adiciona-se colunas no *data frame* através do comando a seguir, pressupondo que a ordem dos dados esteja correta:

`nomedodata.frame$variávelaseradicionada`


```r
informacoes$cidades=c("Nova Hartz","Gramado","Soledade",
                      "Porto Alegre")
informacoes
```

```
  estudantes idade peso      cidades
1     Camila    21   65   Nova Hartz
2      Pedro    17   79      Gramado
3    Marcelo    17   80     Soledade
4  Guilherme    18  100 Porto Alegre
```

É possível fazer uma contagem concatenando com a filtragem do pacote `subset`, como no exemplo a contagem dos indivíduos cuja origem é Soledade.


```r
length(subset(informacoes$cidades, informacoes$cidades=="Soledade"))
```

```
[1] 1
```

## Manipulação de banco de dados

<!--
## Funções
-->

A função `edit()` abre uma interface simples de edição de dados em formato planilha, e é útil para pequenas modificações. Mas para salvar as modificações atribua o resultado da função `edit` a um objeto.

Utiliza-se o comando da seguinte forma: 


`novonomedabase = edit(nomeatualdabase)`


```r
informacoes.2=edit(informacoes)
```

<div class="figure" style="text-align: center">
<img src="95.png" alt="Editor de dados" width="80%" />
<p class="caption">(\#fig:95)Editor de dados</p>
</div>

Basta clicar no retângulo correspondente a variável que deseja ser modificada, excluir ou adicionar novas colunas.

<div class="figure" style="text-align: center">
<img src="10.png" alt="Acréscimo de uma nova coluna através do editor de dados" width="80%" />
<p class="caption">(\#fig:10)Acréscimo de uma nova coluna através do editor de dados</p>
</div>

Logo, chamando o novo banco de dados, teremos:


```r
informacoes.2 
```

```
  estudantes idade peso      cidades
1     Camila    21   65   Nova Hartz
2      Pedro    17   79      Gramado
3    Marcelo    17   80     Soledade
4  Guilherme    18  100 Porto Alegre
```


As funções a seguir são aplicáveis a vetores, data.frames e listas, e em muitos casos trazem praticidade a uma análise estatística. Foram criados objetos com informações do nome dos estudantes e altura. Segue o processo de criação do *data frame* com estas informações, lembrando que esta forma de "união" das informações pressupõe que a ordem dos dados esteja correta:


```r
# Crição do data frame
estudantes=c("Guilherme", "Marcelo", "Pedro", "Camila")
altura= c(1.50, 1.9, 1.74, 1.80)
informacoes.3=data.frame(estudantes, altura)
```

Já o comando `merge()` serve para juntar dois *data frames* que possuam uma coluna em comum. Neste caso, unimos o objeto `informações.2` com o objeto `informações.3` utilizando o nome dos estudantes (informação em comum):


```r
# União de um banco de dados (existencia de uma váriavel em comum)

informacoes=merge(informacoes.2,informacoes.3, by="estudantes")
```

Adicionar um cálculo entre as colunas é muito simples com o RStudio, neste caso com os dados do peso e altura, pode-se calcular o IMC (Índice de Massa Corporal) em uma nova coluna:


```r
informacoes$Imc=c(informacoes$peso/(informacoes$altura^2))
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    17   80     Soledade   1.90 22.16
4      Pedro    17   79      Gramado   1.74 26.09
```

Ainda, se houver linhas que tenham pelo menos uma informação faltante (NA), estas podem ser excluídas com o comando `na.omit()`, ou mesmo os NAs serem substituídos por outro caractere (neste caso foi substituído por zero) com o comando `is.na`:


```r
# Retirar as linhas que tenham pelo menos um NA:

informacoes<- na.omit(informacoes)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    17   80     Soledade   1.90 22.16
4      Pedro    17   79      Gramado   1.74 26.09
```

```r
# Substituir NA's por zero no data.frame

informacoes[is.na(informacoes)] = 0
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    17   80     Soledade   1.90 22.16
4      Pedro    17   79      Gramado   1.74 26.09
```

Outro recurso interessante é a substituição de dados em uma coluna, que pode ser feito de forma automática para uma condição padrão escolhida. No exemplo abaixo, substituimos aquelas informações de idade igual a 17 pelo número 19:


```r
# Substituir números na coluna
informacoes$idade[informacoes$idade == 17] <- 19
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 20.06
2  Guilherme    18  100 Porto Alegre   1.50 44.44
3    Marcelo    19   80     Soledade   1.90 22.16
4      Pedro    19   79      Gramado   1.74 26.09
```

A classificação qualitativa das informações, com base em condições definidas pelo usuário podem ser facilmente efetuadas pelo comando `ifelse`. Para quem não tem intimidade com atributos de programação, este comando seleciona "se" (*if*) uma informação desejada é atendida, e cria uma rotina (*else*) que será aplicada "então". 

No nosso exemplo, cria-se um objeto "classificacao" e se a coluna IMC conter dados acima de 25, será marcado como "peso normal", sendo que do contrário, constará como "excesso de peso". Após utilizamos o comando `cbind()` para unir os dois objetos pelas colunas. caso não queira utilizar o comando `cbind()`, poderia ser criado uma nova coluna com o nome do obetjo sendo "informacoes\$classificacao".


```r
# Classificar qualitativamente informações em um determinado intervalo 
classificacao=ifelse(informacoes$Imc<25, "peso normal", 
                     "excesso de peso")
informacoes=cbind(informacoes, classificacao)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao
1     Camila    21   65   Nova Hartz   1.80 20.06     peso normal
2  Guilherme    18  100 Porto Alegre   1.50 44.44 excesso de peso
3    Marcelo    19   80     Soledade   1.90 22.16     peso normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso
```


Table: (\#tab:imct)Valores padrão para o IMC

Resultado            Significado             
-------------------  ------------------------
Abaixo de 17         Muito abaixo do peso    
Entre 17 e 18,49     Abaixo do peso          
Entre 18,5 e 24,99   Peso normal             
Entre 25 e 29,99     Acima do peso           
Entre 30 e 34,99     Obesidade I             
Entre 35 e 39,99     Obesidade II (severa)   
Acima de 40          Obesidade III (mórbida) 

No entanto, o IMC possui várias classificações de acordo com o seu resultado (Tabela \@ref(tab:imct)), sendo que, por exemplo, resultados abaixo de 17 informam que o indivíduo se encontra como Muito abaixo do peso, e acima de 40, se encontra em Obesidade III. Para efetuar a classificação desta maneira utilizando o comando `ifelse`, ou seja, com mais de uma condição, pode ser efetuada a estruturação com a aglutinação do comando:


```r
informacoes$tipoimc=ifelse(informacoes$Imc<17, "Muito abaixo do peso",
ifelse(informacoes$Imc>=17&informacoes$Imc<=18.49,"Abaixo do peso",
ifelse(informacoes$Imc>=18.5&informacoes$Imc<=24.99,"Peso Normal",
ifelse(informacoes$Imc>=25&informacoes$Imc<=29.99,"Acima do Peso",
ifelse(informacoes$Imc>=30&informacoes$Imc<=34.99,"Obesidade I",
ifelse(informacoes$Imc>=35&informacoes$Imc<=39.99,"Obesidade II",
       "Obesidade III"))))))
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz   1.80 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre   1.50 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade   1.90 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
```

A classificação binária dos dados (0,1) também é relevante para o estudo da manipulação dos dados trabalhados pelo pesquisador. Neste exemplo, classificou-se aqueles valores da coluna "classificacao" com o "peso normal" iguais a 1, do contrário classificou-se 0 (zero).


```r
# Classificar informações usando o código binário
informacoes$binario= ifelse(informacoes$classificacao 
                            == 'peso normal', 1, 0) 
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz   1.80 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre   1.50 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade   1.90 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
  binario
1       1
2       0
3       1
4       0
```

O comando `rbind()` é utilizado para incluir linhas novas abaixo de um objeto já criado pelo pesquisador, sendo que é importante o cuidado de que estas novas informações tenham os mesmos campos (colunas). A exemplo, pede-se para incluir uma nova pessoa no *data frame* informacoes: Francisco, 30 anos de idade, peso 59, natural de Ijuí, IMC 23,33768, classificado como peso normal. Lembrando de incluir os campos "tipoimc" e "binario".


```r
novo1=data.frame(estudantes="Francisco", idade=30, peso=59, 
                 cidades="Ijuí", 
                 altura="1,59", 
                 Imc= 23.33768, 
                 classificacao= "peso normal",
                 tipoimc="Peso Normal", 
                 binario=1)
informacoes=rbind(informacoes, novo1)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz    1.8 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre    1.5 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade    1.9 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
5  Francisco    30   59         Ijuí   1,59 23.34     peso normal   Peso Normal
  binario
1       1
2       0
3       1
4       0
5       1
```

Outra forma de incluir informações adicionais nos *data frames* através de atributos é utilizando o pacote `dplyr`. Decide-se criar um campo "faixa etária", sendo que aqueles indivíduos com idade acima de 21 chamaremos de "adulto" e do contrário "não adulto".


```r
require(dplyr)
```

```
Carregando pacotes exigidos: dplyr
```

```

Attaching package: 'dplyr'
```

```
The following objects are masked from 'package:stats':

    filter, lag
```

```
The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union
```

```r
informacoes= mutate(informacoes, 
                    "faixa etaria"= ifelse(informacoes$idade<21,
                                           "não adulto", "adulto"))
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz    1.8 20.06     peso normal   Peso Normal
2  Guilherme    18  100 Porto Alegre    1.5 44.44 excesso de peso Obesidade III
3    Marcelo    19   80     Soledade    1.9 22.16     peso normal   Peso Normal
4      Pedro    19   79      Gramado   1.74 26.09 excesso de peso Acima do Peso
5  Francisco    30   59         Ijuí   1,59 23.34     peso normal   Peso Normal
  binario faixa etaria
1       1       adulto
2       0   não adulto
3       1   não adulto
4       0   não adulto
5       1       adulto
```

A (re)ordenação das colunas de um *data frame* pode ser muito útil em alguns casos, sendo extremamente fácil efetuá-la, cada número representa o número da respectiva coluna:


```r
# Reordenar colunas
informacoes=informacoes[c(8,2,3,4,1,6,5,7,9,10)]
```

Caso se queira a inversão total da ordem das colunas do objeto estudado, o comando `rev()` pode ser útil:


```r
# Inversão do posicionamento dos elementos
rev(informacoes)
```

```
  faixa etaria binario   classificacao altura   Imc estudantes      cidades
1       adulto       1     peso normal    1.8 20.06     Camila   Nova Hartz
2   não adulto       0 excesso de peso    1.5 44.44  Guilherme Porto Alegre
3   não adulto       1     peso normal    1.9 22.16    Marcelo     Soledade
4   não adulto       0 excesso de peso   1.74 26.09      Pedro      Gramado
5       adulto       1     peso normal   1,59 23.34  Francisco         Ijuí
  peso idade       tipoimc
1   65    21   Peso Normal
2  100    18 Obesidade III
3   80    19   Peso Normal
4   79    19 Acima do Peso
5   59    30   Peso Normal
```

A  função `table()` faz a contagem os dados; já o comando `sort()` ordena os objetos em ordem crescente (caso queira no formato decrescente, informar `decreasing=TRUE`).


```r
# contagem de objetos
table(informacoes$classificacao)
```

```

excesso de peso     peso normal 
              2               3 
```

```r
# Ordenar os objetos em ordem crescente
sort(informacoes$idade)
```

```
[1] 18 19 19 21 30
```

A ordenação de todo o *data frame* a partir de uma variável, pode ser realizada utilizando o comando `order`, sendo que pode ser realizada inclusive com variáveis categóricas (no exemplo abaixo o nome das cidades).


```r
# Ordem decrescente 
informacoes[order(informacoes$idade, decreasing = TRUE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
5   Peso Normal    30   59         Ijuí  Francisco 23.34   1,59     peso normal
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
  binario faixa etaria
5       1       adulto
1       1       adulto
3       1   não adulto
4       0   não adulto
2       0   não adulto
```

```r
#ordem crescente
informacoes[order(informacoes$idade, decreasing = FALSE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
5   Peso Normal    30   59         Ijuí  Francisco 23.34   1,59     peso normal
  binario faixa etaria
2       0   não adulto
3       1   não adulto
4       0   não adulto
1       1       adulto
5       1       adulto
```

```r
#ordem crescente
informacoes[order(informacoes$cidades, decreasing = FALSE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
5   Peso Normal    30   59         Ijuí  Francisco 23.34   1,59     peso normal
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
  binario faixa etaria
4       0   não adulto
5       1       adulto
1       1       adulto
2       0   não adulto
3       1   não adulto
```

O comando `rank()` cria uma ranqueamento crescente das informações. Se pretende-se, por exemplo, criar uma coluna com o ranking dos valores do IMC, pode ser utilizado:


```r
informacoes$rankingImc=rank(informacoes$Imc)
informacoes
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
1   Peso Normal    21   65   Nova Hartz     Camila 20.06    1.8     peso normal
2 Obesidade III    18  100 Porto Alegre  Guilherme 44.44    1.5 excesso de peso
3   Peso Normal    19   80     Soledade    Marcelo 22.16    1.9     peso normal
4 Acima do Peso    19   79      Gramado      Pedro 26.09   1.74 excesso de peso
5   Peso Normal    30   59         Ijuí  Francisco 23.34   1,59     peso normal
  binario faixa etaria rankingImc
1       1       adulto          1
2       0   não adulto          5
3       1   não adulto          2
4       0   não adulto          4
5       1       adulto          3
```

Para utilizar a função `rank` com os maiores valores em primeiro lugar:


```r
rank(-informacoes$Imc)
```

```
[1] 5 1 4 2 3
```


## Funções Matemáticas

A utilização de funções matemáticasno RStudio contribui para que o pesquisador possa realizar vários experimentos com seus dados. Os cálculos podem ser efetuados diretamente no console do programa ou aplicados aos objetos criados:


```r
log(1.5)
```

```
[1] 0.4055
```

```r
exp(1)
```

```
[1] 2.718
```

No caso do *data frame* o qual foi criado acima ("informacoes"), pode-se buscar as informações dos valores mínimos (função `min()`), máximos (`max()`) da base:


```r
max(informacoes$idade)
```

```
[1] 30
```

```r
min(informacoes$idade)
```

```
[1] 18
```

Ainda, se o interesse está em descobrir a posição, no *data frame}, do peso mínimo e máximo da amostra utiliza-se o comando `which.min` e `which.max`.


```r
# Para descobrir em qual posição se encontra o peso mínimo:
which.min(informacoes$peso)
```

```
[1] 5
```

```r
which.max(informacoes$peso)
```

```
[1] 2
```

Para descobrir qual é o estutande que possui o peso mínimo, por exemplo, ou o Imc máximo, utiliza-se o seguinte comando (notem que os resultados trazem a lista de todos os estudantes comparados):


```r
informacoes$estudantes[which.min(informacoes$peso)]
```

```
[1] Francisco
Levels: Camila Guilherme Marcelo Pedro Francisco
```

```r
informacoes$estudantes[which.max(informacoes$Imc)]
```

```
[1] Guilherme
Levels: Camila Guilherme Marcelo Pedro Francisco
```

O arredondamento de valores numéricos pode ser feito utilizando o comando `round()`, o qual o pesquisador informa o número de casas decimais:


```r
# Arredondar para n casas decimais
round(informacoes$Imc, 2)
```

```
[1] 20.06 44.44 22.16 26.09 23.34
```

Já o comando `signif()` determina o número de algarismos significativos da série escolhida, ou seja, ele arredonda para os valores em seu primeiro argumento com os número de dígitos detemrinados: 


```r
x2 <- pi * 100^(-1:3)
round(x2, 3)
```

```
[1] 3.100e-02 3.142e+00 3.142e+02 3.142e+04 3.142e+06
```

```r
signif(x2, 3) 
```

```
[1] 3.14e-02 3.14e+00 3.14e+02 3.14e+04 3.14e+06
```

A soma do total da coluna idade, o desvio padrão, a variância, a média aritmética e mediana podem ser encontrados, respectivamente, pelos comandos `sum()`, `sd()`, `var()`, `mean()`, `median()`:


```r
# Realiza a somatória dos valores
sum(informacoes$idade)
```

```
[1] 107
```

```r
# Desvio padrão
sd(informacoes$idade)
```

```
[1] 4.93
```

```r
# Variancia
var(informacoes$idade)
```

```
[1] 24.3
```

```r
# Calcula a média aritmética dos valores
mean(informacoes$idade)
```

```
[1] 21.4
```

```r
# Informa o valor mediano do conjunto
median(informacoes$idade)
```

```
[1] 19
```

O comando `quantile()` oferece a possibilidade de obter os quartis dos dados de acordo com as probabilidades estabelecidas pelo pesquisador. No exemplo, explora-se a variável idade:


```r
quantile(informacoes$idade,  probs = c(0.5, 1, 2, 5, 10, 50)/100)
```

```
 0.5%    1%    2%    5%   10%   50% 
18.02 18.04 18.08 18.20 18.40 19.00 
```

## Conversão de datas

A configuração e padronização dos formato de datas no RStudio podem ser efetuadas pelo pesquisador, primeiramente ao carregar a base de dados no programa e em um segundo momento durante a manipulação das informações. Assim, seguem alguns dos procedimentos para a correta alteração dos padrões de datas:


```r
abertura <- c("03/02/69", "17/08/67")
fechamento <- c("2000-20-01", "1999-14-08")
abertura <- as.Date(abertura, format = "%d/%m/%y")
fechamento <- as.Date(fechamento, format = "%Y-%d-%m")

# Diferença de dias dos intervalos informados
abertura-fechamento
```

```
Time differences in days
[1] -11308  24840
```

## Exercícios

**1.**	Baixe o arquivo "arvores" que se encontra no endereço <https://smolski.github.io/softwarelivrer/atividades>. Este é um banco de dados com informações cedido pela professora Tatiane Chassot. Abra o arquivo no Rstudio tomando os cuidados necessários (importar no formato correto, prestar atenção nas vírgulas e nomes...). Por meio dos comandos do R, responda as seguintes perguntas, informando o comando utilizado.

**1.1.**	Qual é a espécie de árvore que possui o maior e menor diâmetro?  E quais são estes valores de diâmetro?

<!--
Neste caso, irão utilizar o comando da seguinte forma >Nome_do_banco_de_dados$Nome_da_variável_buscada[which.max(diâmetro_cm)]
-->

**1.2.**	Qual é a altura média, mínima e média das árvores? 

**1.3.**	Encontre o diâmetro médio para cada espécie de árvores.

**1.4.**	Com os comandos do R, verifique a quantidade de dados referente as variáveis, bem como o nome referente a cada variável.

**1.5.**	Renomeie a primeira coluna para "espécie".

**1.6.**	Classifique as árvores quanto ao seu porte, em relação à altura, em que:

Pequeno porte = árvores com altura inferior a 10 metros.

Grande porte = árvores com altura superior a 10 metros. 


**2.**	Baixe o arquivo "bancodedados1" que se encontra no endereço <https://smolski.github.io/softwarelivrer/atividades>. Este é um banco de dados com informações fictícias que usaremos a fim de aprendizado. Abra o arquivo no Rstudio tomando os cuidados necessários. Por meio dos comandos do R, responda as seguintes perguntas, informando o comando utilizado.

**2.1.** Qual é o vendedor com mais sucesso de vendas?  E o vendedor com menor número de vendas?

**2.2.**	Qual foi o número total de vendas?

**2.3.**	Supondo que um vendedor tenha ficado de fora dos dados, insira suas informações no banco de dados que já possuímos.

- Vendedor = Silvia; Idade = 48; Setor = 2; N de vendas = 45.

**2.4.**	Crie uma nova coluna classificando os vendedores como:

- vendas $<$ 25 = "Regular"

- 25 $>$ vendas = "Ótimo"

**2.5** Renomeie a coluna "vendas mensais" para "vendas diárias".


# Estatística Descritiva{#desc}

*Denize Ivete Reis*

\begin{flushright}
\emph{}
\end{flushright}

A Estatística é uma ciência cujo campo de aplicação estende-se a diferentes áreas do conhecimento humano. Tem por objetivo fornecer métodos e técnicas que permitem lidar, racionalmente, com situações sujeitas a incertezas. Apresenta um conjunto de técnicas e métodos de pesquisa que envolvem o planejamento de estudos (experimentais e observacionais), a coleta e organização de dados, a inferência, a análise e a disseminação de informação.

Alguns termos extensamente utilizados em estatística, são definidos a seguir [@triola1999]:

**População**: é uma coleção completa de todos os elementos (valores, pessoas, medidas etc.) a serem estudados.

**Censo**:  é uma coleção de dados relativos a todos os elementos de uma população.

**Amostra**:  é uma sub-coleção de elementos extraídos de uma população.
	Parâmetro  é a medida numérica que descreve uma característica de uma população.
	
**Estatística**: é uma medida numérica que descreve uma característica de uma amostra.


## Natureza da medida das variáveis


Variáveis reporta-se a características ou atributos que podem tomar diferentes valores ou categorias, o que se opõe ao conceito de constante [@almeida2000]. Assim, variável pode ser definida como sendo a característica dos elementos da amostra ou da população que nos interessa estudar estatisticamente.

Variáveis podem ser classificadas da seguinte forma:

**Variáveis quantitativas**: consistem em números que representam contagens ou medidas. Dividem-se em:


a) Variáveis discretas: resultam em um conjunto finito de valores possíveis, ou de um conjunto enumerável desses valores. Ex. número de unidades produzidas.

b) Variáveis contínuas: resultam de um número infinito de valores possíveis que podem ser associados a pontos em uma escala contínua de tal maneira que não haja lacunas ou interrupções. Ex. Renda das famílias em reais.

**Variáveis qualitativas**: ou variáveis categóricas, ou atributos que podem ser separados em diferentes categorias que se distinguem por alguma característica não-numérica. Divididas em:

a) Variável nominal: caracterizada por dados que consistem apenas em nomes, rótulos ou categorias. Os dados não podem ser dispostos segundo um esquema ordenado (como de baixo para cima). Ex. nacionalidade

b) Variável ordinal: envolve variáveis representadas por nomes que podem ser dispostos em alguma ordem, mas as diferenças entre os valores dos dados não podem ser determinadas, ou não tem sentido. Esse nível dá informações sobre comparações relativas, mas os graus de diferença não servem para cálculos [@triola1999]. Ex. Grau de escolaridade.

**Dado**: é o valor assumido por uma variável aleatória em um experimento.


A Estatística subdivide-se em descritiva e inferencial. A estatística descritiva se preocupa em descrever os dados. A estatística inferencial, fundamentada na teoria das probabilidades, se preocupa com a análise destes dados e sua interpretação.

Informações estatísticas em jornais, relatórios e outras publicações que consistem de dados reunidos e apresentados de forma clara e resumida, na forma de tabelas, gráficos ou numéricos, são conhecidos como estatísticas descritivas (ANDERSON, 2002).


**Exemplo 1**

Estaremos utilizando como exemplo os dados de uma pesquisa (dados simulados), cujo banco de dados está intitulado "Dados\_pesquisa.ods". Os dados são referentes aos resultados obtidos por ocasião de uma pesquisa realizada entre os consumidores a fim de analisar características associadas ao mercado consumidor de sucos, sendo que a amostra é composta de 348 entrevistados aleatoriamente selecionados.


- O objetivo primário do estudo foi determinar variáveis que seriam úteis para caracterizar os consumidores que já conhecem o suco e a possibilidade potencial de futuros consumidores. Há também interesse nas relações entre variáveis das características pessoais desses consumidores ou futuros consumidores.

- A pesquisa foi realizada, depois que os participantes realizaram uma visita técnica às instalações da empresa e puderam conhecer seus produtos e processos.

Para cada entrevistado foram registrados dados para as seguintes variáveis:
 

**Sexo** – Gênero sexual;

**Divulgacao** – Forma de acesso ao suco ou publicidade do mesmo;

**Renda\_h** – Renda por hora do entrevistado;

**Praticidade** – Aspectos quanto a oferta do suco, como por ex. embalagem;

**Sabor** – Aspectos relacionados ao sabor;

**Pessoas\_familia** – Número de pessoas que compõe o grupo familiar;

**Preço** – como cada entrevistado classificava o preço do produto;

**consumo\_anterior** – Se já consumia o suco antes da visita técnica;

**consumo\_pos** – Se consumia o suco após a visita técnica;

**Idade** – Idade dos consumidores;

**Altura\_(m)** – Altura dos consumidores;

**Peso\_(Kg)** – Peso dos consumidores.

Pede-se:

1.	Salvar inicialmente os dados em formato CSV, xlsx ou outro.

2.	Ler os dados no "Environment" pelo "Import Dataset...From CSV" ou outro. No exemplo abaixo foram importados os dados diretamente do arquivo hospedado na internet.

3.	Carregar o banco de dados, com a finalidade de usar os objetos (variáveis) diretamente nas funções a serem utilizadas.

`attach(nome_da_planilha)`
  

```r
library(readxl)
url <- "https://github.com/Smolski/livror/raw/master/pesquisa_dados.xlsx"
destfile <- "pesquisa_dados.xlsx"
curl::curl_download(url, destfile)
pesquisa_dados <- read_excel(destfile)
attach(pesquisa_dados)
ls.str(pesquisa_dados)
```

```
Altura_(m) :  num [1:348] 1.82 1.9 1.69 1.89 1.9 1.76 1.83 1.81 1.67 1.55 ...
Caso :  num [1:348] 1 2 3 4 5 6 7 8 9 10 ...
consumo_anterior :  chr [1:348] "N" "N" "S" "N" "S" "S" "S" "N" "N" "N" "N" "N" "S" "S" "S" ...
consumo_pos :  chr [1:348] "N" "S" "N" "S" "N" "S" "N" "S" "N" "S" "S" "S" "S" "S" "S" ...
Divulgacao :  chr [1:348] "Degustacao" "Radio" "TV" "TV" "Degustacao" "TV" "TV" "Radio" ...
Idade :  num [1:348] 22 21 20 18 16 28 19 19 22 19 ...
Peso_(Kg) :  num [1:348] 78.5 80 54 78 36 82 75 69 58 49 ...
Pessoas_familia :  num [1:348] 4 3 3 7 4 4 3 4 1 4 ...
Praticidade :  chr [1:348] "Pessima" "Otima" "Boa" "Pessima" "Ruim" "Boa" "Regular" ...
Preço :  chr [1:348] "Acima_concorrencia" "Abaixo_concorrencia" ...
Renda_h :  chr [1:348] "1.41" "17.34" "6.86" "2.65" "2.01" "11.32" "6.86" "3.25" ...
Sabor :  chr [1:348] "Otimo" "Pessimo" "Bom" "Otimo" "Otimo" "Regular" "Ruim" "Bom" ...
Sexo :  chr [1:348] "Feminino" "Feminino" "Feminino" "Feminino" "Masculino" ...
```
  
## Tabelas

Segundo @barbetta1988, dados representados em tabelas e gráficos adequados, permitem observar determinados aspectos relevantes, bem como delinear hipóteses a respeito da estrutura dos dados em estudo, o que conhecemos como análise exploratória de dados. Isto pode ser feito inicialmente com a representação em forma de tabelas.


O comando `table()` é utilizado para elaborarmos tabelas de frequências absolutas. Dependendo da variável a ser representada, podemos usar esse comando de diferentes formas:

### Tabela simples para apresentação das frequências absolutas

Uma tabela simples considera quantas vezes ocorre cada categoria (ou nível).

`table(nome_variável)`


Ex. Variável **Praticidade**


```r
table(Praticidade)
```

```
Praticidade
    Boa   Otima Pessima Regular    Ruim 
     82      70      21      80      95 
```

### Tabela cruzada

A tabela cruzada, também conhecida como tabela de dupla entrada, para apresentação das frequências absolutas.


`table(nome_variável1,nome_variável2)`


Ex. Construir uma tabela cruzada apresentando as frequências absolutas das variáveis **Sexo** e **Divulgacao**.


```r
table(pesquisa_dados$Sexo,pesquisa_dados$Divulgacao)
```

```
           
            Degustacao Outro Radio  TV
  Feminino          78     6    61 147
  Masculino         19     1    15  21
```


### Tabela cruzada para apresentação das frequências relativas

Com a introdução do comando `prop.table` é possível gerar, facilmente, tabelas de frequências relativas para as variáveis de interesse. As medidas relativas são importantes para comparar distribuições de frequências [@barbetta1988].

`prop.table(table(nome_variável1,nome_variável2))`


Ex. Construir uma tabela cruzada apresentando as frequências relativas das variáveis **Sexo** e **Divulgacao**.


```r
prop.table(table(Divulgacao,Sexo))
```

```
            Sexo
Divulgacao   Feminino Masculino
  Degustacao 0.224138  0.054598
  Outro      0.017241  0.002874
  Radio      0.175287  0.043103
  TV         0.422414  0.060345
```


A função `tapply` serve para calcular um valor usando uma variável categórica como condição, ou seja, aplica uma função qualquer (como média, por exemplo) a uma variável quantitativa para cada classe de uma variável categórica. Assim, permite obter em um só comando, a medida para cada categoria. 

`tapply(var_quantitativa,var_categórica, função_desejada)`

`tapply(variavel_quantitativa,variavel_qualitativa, mean)`

Se um registro possui `NA`, isto é, dados perdidos: com o parâmetro na.rm=T, indicamos para o comando ignorar os NAs nos dados e calcular a média. 


`tapply(variavel_quanti, variavel_quali, mean, na.rm=T)`

## Gráficos

### Gráfico de colunas

As frequências podem ser visualizadas graficamente, usando gráficos de barras elementares, que se aplicam à descrição de qualquer variável qualitativa ou quantitativa discreta, vetor de dados ou tabelas.

No entanto, no caso de dados em banco de dados, quando não utilizamos outros mecanismos de atribuição, precisamos usar o comando table.

`barplot(table(nome_variável))`

Ex. Construir um gráfico de colunas para a variável **Sexo**.


```r
barplot(table(Sexo))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-67-1.png" alt="Gráfico de colunas com a variável Sexo" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-67)Gráfico de colunas com a variável Sexo</p>
</div>

**Obs**.: É possível personalizar o gráfico, incluindo o título do eixo x (xlab), o título do eixoy (ylab), o título do gráfico (main), a cor da coluna (col) e cor da borda da coluna (border), lembrando que as cores, assim como os comandos devem ser expressas em inglês.


`barplot(table(nome_variável), col=c("blue","red"), main="Título", xlab="Variável do eixo x", ylab = "Informação que consta no eixo y",border="red")`


**Ex.1)** Construir um gráfico de colunas para a variável **Pessoas\_familia**.



```r
barplot(table(`Pessoas_familia`), col=c("blue"), 
        main = "Frequência de pessoas por família", 
        xlab = "Frequência", 
        ylab = "Pessoas", 
        border = "red")
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-68-1.png" alt="Gráfico de colunas com a variável `Pessoas familia`" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-68)Gráfico de colunas com a variável `Pessoas familia`</p>
</div>

**Ex.2)** Construir uma tabela de dupla entrada para as variáveis **Sexo** e **Divulgação**.


```r
barplot(table(Sexo,Divulgacao), 
        col=c("blue"), 
        main = "Frequência de pessoas por Sexo e Divulgacao")
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-69-1.png" alt="Gráfico de colunas com as variáveis Sexo e Divulgacao" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-69)Gráfico de colunas com as variáveis Sexo e Divulgacao</p>
</div>


**Ex.3)** Na sequência utiliza o sinal de atribuição <- para atribuir o nome Resultado para esta tabela (tabela de dupla entrada obtida em Ex.2).


```r
Resultado<-table(Sexo,Divulgacao)
```

**Ex.4)** Execute o seguinte comando:


```r
barplot(Resultado,col=c("blue","red"),main="Título",
        xlab="Variável do eixo x",
        ylab="Informação que consta no eixo y", 
        border='red', 
        beside=T,legend=rownames(Resultado),
        args.legend = list(x = "topleft"))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-71-1.png" alt="Gráfico de colunas com as variáveis Sexo e Divulgacao (2)" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-71)Gráfico de colunas com as variáveis Sexo e Divulgacao (2)</p>
</div>


Observe que o uso do argumento `beside=T` evita que as barras fiquem empilhadas e o arguemnto `legend`' insere a legenda conforme as cores das colunas.


**Ex.5)** Repita o exercício a partir do Ex.3, invertendo a ordem entre as variáveis qualitativas.

### Setograma ou gráfico de pizza

Os gráficos em setores são utilizados para ilustrar dados qualitativos de modo mais compreensível. Quando a variável é ordinal, gráficos de colunas são mais indicados pelo fato de permitirem manter a ordem das categorias. Isto também vale para os casos em que se tem muitas categorias ou quanto se pretende dar mais destaque às categorias mais frequentes [@barbetta1988].

`pie(table(nome_variável),main="nome")`

Ex. Construa um gráfico na forma de Setograma para a variável **Sabor**.


```r
# Criar objeto com a tabela de Sabor
Sabor1=table(Sabor)

# Calcular o percentual
percent=signif(Sabor1/sum(Sabor1)*100,3)

#Criando os nomes da legenda
nomesleg=c("Bom","Ótimo","Péssimo","Regular","Ruim")

#Plota-se o gráfico de pizza
pie(Sabor1, 
    labels = paste(percent, "%", sep=""), 
    col = terrain.colors(5), # Determina cores 
    radius = 1) 
legend(x="topright", # Determina posição da legenda
       legend=nomesleg, # Insere nomes da legenda
       cex = 0.65, # Tamanho do texto
       fill = terrain.colors(5)) # Determina cores 

## Alguns exemplos de paletas de cores:
# - rainbow(n)
# - heat.colors(n)
# - terrain.colors(n) 
# - topo.colors(n)
# - cm.colors(n)
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-72-1.png" alt="Gráfico de pizza com a variável Sabor" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-72)Gráfico de pizza com a variável Sabor</p>
</div>

### Histograma

No histograma, utilizado em geral quando temos variáveis quantitativas contínuas, a altura dos retângulos representa a frequência de ocorrência de valores no intervalo (deve iniciar sempre em zero), devem ter sempre a mesma largura podendo ser justapostos. O eixo horizontal (dos valores da variável) pode iniciar próximo ao menor valor da variável [@barbetta1988]. Para confecção do histograma devemos usar:

`hist(nome_variável)`

Ex. Construa um histograma com a variável **Renda\_h**.


```r
hist(as.numeric(`Renda_h`))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-73-1.png" alt="Histograma com a variável `Renda h`" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-73)Histograma com a variável `Renda h`</p>
</div>

**Obs**. I: Neste caso também é possível personalizar o gráfico, incluindo o título do eixo x (xlab), o título do eixoy (ylab), o título do gráfico (main), a cor da coluna (col) e cor da borda da coluna (border), lembrando que as cores, assim como os comandos devem ser expressas em inglês.

**Obs**. II: Para definir o número de intervalos no Histograma, usamos:


`hist(nome_variável, breaks = 5)`


```r
hist(as.numeric(`Renda_h`), 
     breaks=5, 
     labels=TRUE, 
     ylim=c(0,200), 
     xlab = 'Renda',
     ylab = 'Frequência',
     main = 'Histograma da Renda',
     col = '#BBDEFB')
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-74-1.png" alt="Histograma com a variável Renda h com breaks=5" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-74)Histograma com a variável Renda h com breaks=5</p>
</div>
O comando `ylim` determina os limites do eixo y a serem mostrados; `xlab` e `ylab` determinam o nome das variáveis dos eixos x e y; `main` determina o nome do título e `col` determina a cor do gráfico. Use o argumento `main=NULL` para remover o título.

Inserindo as opções `$counts` e `$breaks` retomamos os valores da contagem dos dados e dos intervalos do histograma:


```r
hist(as.numeric(`Renda_h`), breaks=5)$counts
```

```
[1] 106 167  62  11   2
```

```r
hist(as.numeric(`Renda_h`), breaks=5)$breaks
```

<img src="index_files/figure-html/unnamed-chunk-75-1.png" width="80%" style="display: block; margin: auto;" />

```
[1]  0  5 10 15 20 25
```


### Boxplot ou diagrama em caixas

Os diagramas em caixa são convenientes para revelar tendências centrais, dispersão, distribuição dos dados e a presença de outliers (valores extremos). Como as medianas revelam uma tendência central, ao passo que os quartis indicam a dispersão dos dados, os diagramas em caixa têm a vantagem de não serem tão sensíveis a valores extremos como outras medidas baseadas na média e no desvio-padrão. Por outro lado, os diagramas em caixa (boxplots) não dão informação tão detalhada quanto os histogramas ou os gráficos ramo-e-folhas, podendo não ser, assim, a melhor escolha quando lidamos com um único conjunto de dados. Os diagramas em caixa são, entretanto, mais convenientes na comparação de dois ou mais conjuntos de dados [@triola1999]. 

No diagrama de caixas, torna-se fácil identificar **outliers** (ou valores extremos), que são valores extremamente  raros, no sentido de que estão muito afastados da maioria dos dados. Ao explorarmos um conjunto de dados, não podem deixar de considerar os outliers, porque eles podem revelar informações importantes [@triola1999].

Para obter o boxplot para um conjunto de dados:

`boxplot(variávelA, variávelB, names=c("A","B"))`


**Ex.1)** Construir um boxplot da variável **Idade**.


```r
boxplot(Idade,horizontal = T)
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-76-1.png" alt="Boxplot com a variável Idade" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-76)Boxplot com a variável Idade</p>
</div>


**Ex.2)** Construir um boxplot das variáveis **Peso\_(Kg)** e **Altura\_(m)**.    



### Gráfico ramo-e-folhas

Em um gráfico ramo-e-folhas, classificamos os dados segundo um padrão que revela a distribuição subjacente. O padrão consiste em separar um número em duas partes em geral: o ramo consiste nos algarismos mais à esquerda e as folhas consistem nos algarismos mais à direita.

No gráfico Ramo-e-folhas, podemos ver a distribuição desses dados, que é uma vantagem do gráfico ramo-e-folhas e ainda conservar toda a informação da lista original; se necessário, podemos recompor a relação original de valores. Note que as linhas de algarismos em um gráfico ramo-e-folhas são análogas, em natureza, às barras de um histograma [@triola1999].


`stem(nome_variável)` - comando que permite obter um gráfico Ramo e Folhas. 

Ou 

`stem(nome_variável,scale=1)`


O "scale=1", que é o padrão, separa os ramos das folhas a partir das casas decimais.

Caso padrão:

- A ideia do ramo e folhas é separar um número (como 16,0) em duas partes. Assim, a primeira parte inteira (16) chamada de ramo e a segunda, a parte decimal (0) chamada de folha. O padrão do R é separar os números em duas partes (inteira e decimal) e agrupar os números em classes de tamanho 2. Por exemplo, o ramo 16 leva em conta os números 16 e 17. 


**Obs.**: Esse padrão vai se alterando, à medida que o conjunto de dados apresente diferentes casas decimais.

Assim, outras opções podem ser avaliadas:

a) `stem(nome_variável,scale=0.5)`

b) `stem(nome_variável,scale=2)`

**Obs.**: Quando uma folha relacionada com certo ramo tem uma quantidade tão grande de valores que ele sintetiza essa quantidade usando a denominação +n, e invade a linha seguinte. Isso pode ser melhorado usando **width**.

c) `stem(nome_variável,scale=0.5,width=120)`

Ex. Construa um gráfico Ramo e Follhas com a variável **Idade**.


```r
stem(Idade,scale=2)
```

```

  The decimal point is at the |

  16 | 000
  17 | 000000000
  18 | 0000000000000000000000000000000000000000
  19 | 000000000000000000000000000000000000000000000000
  20 | 0000000000000000000000000000000000000000000000000000000000000000
  21 | 000000000000000000000000000000000000000000000000000000000000
  22 | 0000000000000000000000000000000000000000000
  23 | 000000000000
  24 | 000000000
  25 | 0000
  26 | 00000000000
  27 | 00000000000
  28 | 0000000000000
  29 | 00
  30 | 00000
  31 | 
  32 | 00
  33 | 
  34 | 00
  35 | 00
  36 | 
  37 | 
  38 | 000
  39 | 
  40 | 
  41 | 
  42 | 
  43 | 
  44 | 
  45 | 
  46 | 
  47 | 
  48 | 00000
```

### Gráficos de dispersão

Às vezes temos dados emparelhados de forma que associa cada valor de um conjunto a um determinado valor de um segundo conjunto. Um diagrama de dispersão é um gráfico dos dados emparelhados (x, y), com um eixo x horizontal e um eixo y vertical. O diagrama de dispersão, apresenta no eixo horizontal os valores da primeira variável e um eixo vertical para os valores da segunda variável. O padrão dos pontos assim marcados costuma ajudar a determinar se existe algum relacionamento entre as duas variáveis A e B.

`plot(variável_independente,Variável_dependente)`

Ou

`plot(variável_dependente~variável_independente)`

### Gráfico de linhas

Apresenta a evolução de um dado, geralmente ao longo do tempo. Eixos na vertical e na horizontal indicam as informações a que se refere e a linha traçada entre eles, ascendente, descendente constante ou com vários altos e baixos mostra o percurso de um fenômeno específico.

Ex. Considere os dados que descrevem os valores do número de empresas fiscalizadas na fiscalização do trabalho na área rural Brasil 1998-2010.

<!--

Table: (\#tab:unnamed-chunk-78)Evolução dos resultados da fiscalização do trabalho na área rural Brasil 1998-2010

  Ano  Empresas.Fiscalizadas 
-----  ----------------------
 1998  7.042                 
 1999  6.561                 
 2000  8.585                 
 2001  9.641                 
 2002  8.873                 
 2003  9.367                 
 2004  13.856                
 2005  12.192                
 2006  13.326                
 2007  13.390                
 2008  10.839                
 2009  13.379                
 2010  11.978                
-->

Table: (\#tab:evolres)Evolução dos resultados da fiscalização do trabalho na área rural Brasil 1998-2010

|**Ano**|**Empresas Fiscalizadas**|
|:----:|:---------------------:|
| 1998|7.042                  |
| 1999|6.561                  |
| 2000|8.585                  | 
| 2001|9.641                  |
| 2002|8.873                  |
| 2003|9.367                  |
| 2004|13.856                 |
| 2005|12.192                 |
| 2006|13.326                 |
| 2007|13.390                 |
| 2008|10.839                 |
| 2009|13.379                 |
| 2010|11.978                 |

Fonte: MTE. SFIT. Elaboração: DIEESE.

Para construir um gráfico de linhas, utilizamos o seguinte comando:

`plot(x,y,type= "Tipo de símbolo")`

Neste gráfico, podemos utilizar comandos já utilizados anteriormente, para inserir título, nomes dos eixos, etc. Para escolher o formato das linhas, com o uso do argumento `type`, seguem algumas opções:

- `"p"` para pontos,
- `"l"` para linhas,
- `"b"` para pontos e linhas,
- `"c"` para linhas descontínuas nos pontos,
- `"o"` para pontos sobre as linhas,
- `"n"` para nenhum gráfico, apenas a janela.

Para o caso de representação no mesmo gráfico, de duas ou mais variáveis, o processo deverá ser realizado por etapas:

`plot(x,y1,type="b",main="Título", xlab="Nome_eixo_x",ylab="Nome_eixo_y", col="cor das linhas",ylim=c(yi,ys))`


```r
empfisc=data.frame(ano=c(1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,
    2008,2009,2010), qtd=c(7042,6561,8585,9641,8873,9367,
13856,12192,13326,13390,10839,13379,11978))

plot(empfisc$ano,empfisc$qtd,type="b",main="Título",
     xlab="Nome_eixo_x",ylab="Nome_eixo_y", 
     col="blue",xlim=c(1998,2010))
```

<div class="figure" style="text-align: center">
<img src="index_files/figure-html/unnamed-chunk-79-1.png" alt="Gráfico de linha sobre a fiscalização do trabalho na área rural Brasil 1998-2010" width="80%" />
<p class="caption">(\#fig:unnamed-chunk-79)Gráfico de linha sobre a fiscalização do trabalho na área rural Brasil 1998-2010</p>
</div>

onde, no argumento `ylim`, devemos indicar o intervalo de variação dos valores de y, ou seja todo o intervalo que será necessário para representar todas as variáveis.

Na sequência adicionamos as instruções para as demais variáveis:

`lines(x, y2,col="cor_desejada", type="b")`

Com o argumento `"legend"` instruímos a formatação da legenda:

`legend(xp,yp,c("representação_variável_1 na legenda", "representação_variável_2 na legenda"),
`col =c("Cor1","cor2"),pch=Valor entre 0 e 25)`

Obs.: `pch`= número (entre 0 e 25). No Help do R (buscando com pch), você encontra a lista completa de símbolos que podem ser utilizados na representação da legenda.
Neste caso, pode ser importante também alterar o tamanho da fonte da legenda, com o uso do argumento `"cex"`.

Exemplo: Segue exemplo de um gráfico de linhas para as temperaturas registradas durante o dia 11/04/2018, pela Estação Meteorológica de São Luiz Gonzaga, RS, conforme dados obtidos no site do Inmet.































































































































































































































