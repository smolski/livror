--- 
title: "Software R: Análise estatística de dados utilizando um programa livre"
author: 
- Felipe Micail da Silva Smolski
- Iara Denise Endruweit Battisti
date: "2018"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: authoryear
biblatexoptions: [refsegment=chapter]
link-citations: yes
github-repo: rstub/bookdown-chapterbib
url: 'http\://rstub.github.io/bookdown-chapterbib/'
description: "Curso de análise estatística com R da UFFS Cerro Largo - RS"
fontsize: 12pt
lang: pt-Br
---



# Apresentação {-}

A necessidade de flexibilidade e robustez para a análise estatística fez com que fosse criado, na década de 1990, a linguagem de programação R. Capitaneado pelos desenvolvedores Ross Ihaka e Robert Gentleman, dois estatísticos da Universidade de Auckland na Nova Zelândia, o projeto foi uma grande evolução para a análise de dados. A partir de então, a ideia inicial de proporcionar autonomia ao pesquisador, viu na expansão do acesso à internet uma oportunidade para que a pesquisa científica se tornasse cada vez mais colaborativa. Ao mesmo tempo, os códigos e rotinas se tornaram facilmente disponibilizáveis na rede, aumentando a reprodução e replicação dos estudos, práticas estas que podem tornar as análises mais confiáveis.

A linguagem de programação R trouxe consigo inúmeras vantagens aos pesquisadores. Dentre elas, pode-se dizer primeiramente que, basicamente o R trabalha com uma extensa relação de modelos estatísticos, que vão desde a modelagem linear e não-linear, a análise de séries temporais, os testes estatísticos clássicos, análise de grupamento e classificação, etc. Não bastasse este fato, é possível a apresentação gráfica dos resultados contando com variadas técnicas, passando também pela criação e manipulação de mapas.

Outra questão importante é que o R possui uma comunidade ativa de desenvolvedores, que se expande regularmente. Isto faz com que as técnicas de análise de dados atinjam pesquisadores de variadas disciplinas ao longo do planeta. Inclusive, concebe que o desenvolvimento dos pacotes melhorem constantemente. No ano de 2017, já haviam mais de 6.000 pacotes disponibilizados. Não menos importante, talvez o essencial: o programa é livre, ao passo que entrega o estado da arte da estatística ao usuário.

Outro progresso significativo na utilização do R foi a criação do *software* RStudio, a partir de 2010. Este, por sua vez, se configura em um ambiente integrado com o R e com inúmeras linguagens de marcação de texto (exemplos LaTeX, Markdown, HTML). Possui igualmente versão livre que disponibiliza ao pesquisador a execução, guarda, retomada e manipulação dos códigos de programação diretamente em seu console, bem como a administração de diretórios de trabalhos e projetos.

O material aqui criado é destinado não somente a alunos de graduação, pós-graduação, professores e pesquisadores acadêmicos, mas também para qualquer indivíduo interessado no aprendizado inicial sobre a utilização de técnicas estatísticas com o R. Inclusive, com o objetivo de alcançar um público das mais variadas áreas do conhecimento, esta obra foi elaborada com exemplos gerais, a serem absorvidos em um momento inicial do estudante. Assim, possui a base para continuar estudos posteriores em estatística e no *software* RStudio. O sistema operacional aqui utilizado é o Windows 10.

Este livro está organizado da seguinte maneira: no capítulo [1](#intro) [**Primeiros Passos com o R**], busca-se instruir o pesquisador para a instalação dos programas necessários para acessar o ambiente de programação, bem como orientar sobre a usabilidade do programa em suas funções básicas de carregamento de bases de dados, criação de objetos e princípios de manipulação. 

Já no capítulo [2](#desc) [**Estatística Descritiva**], leva o leitor ao encontro das técnicas básicas para descrever as variáveis em bancos de dados, como exemplos a média, mínima, máxima, desvio padrão, os quartis e também, apresentar os princípios dos elementos gráficos de apresentação dos dados. 

O capítulo [3](#inf) [**Estatística Inferencial**] tratará dos métodos de determinação de intervalos de confiança (média e proporção), testes de hipóteses (verificar a normalidade dos dados) e das comparações entre médias de amostras dependentes e independentes. 

No capítulo [4](#qui) [**Teste de Qui-Quadrado**], serão abordadas as referidas técnicas para verificação de asssociação entre duas variáveis qualitativas e de aderência a uma distribuição.

No capítulo [5](#reg) [**Modelos de Regressão**] serão introduzidos os conhecimentos sobre as técnicas de análise de correlação e regressão linear simples, bem como sobre o diagrama de dispersão, método dos mínimos quadrados, análise de variância, coeficiente e intervalo de predição, da análise dos resíduos e dos princípios de regressão múltipla.

A criação de documentos dinâmicos utilizando o RStudio será tratada no capítulo [6](#rmark) [**RMarkdown**]. O pesquisador poderá conhecer as formas de integrar a programação no R e a manipulação de bases de dados, criando, compilando e configurando relatórios finais em diversos formatos (HTML, PDF e Word/Libre/Open Office).

Boa leitura!

# Introdução {#intro}

O R é um ambiente voltado para análise de dados com o uso de uma linguagem de programação, frente a isso um conhecimento prévio dos príncipios de programação facilita a compreensão da condução das análises aplicadas no software. Entretanto, não é pré-requisito. Neste capítulo abordaremos os primeiros passos para o emprego da linguagem de programação R utilizando uma interface "amigável" - o software RStudio. Além disso, serão apresentados os comandos básicos para a manipulação de dados dentro do RStudio.


## Download e instalação do R e Rstudio


**R**: <http://www.r-project.org>. Clique em Download (CRAN) - escolha o link de um repositório - clique no link do sistema operacional (Linux, Mac ou Windows) - clique em *install R for de first time - Download*. 

**RStudio**: <http://www.rstudio.com/products/rstudio/download>. Em RStudio Desktop, escolha a versão *free*, seguidas da opção do sistema operacional do usuário.

Lembrando que:

- R é o software;
- RStudio é uma ferramenta amigável para o R.


## Painéis

O RStudio é a interface que faz com que seja mais fácil a utilização da programação em R. 

\begin{figure}

{\centering \includegraphics[width=\textwidth]{paineis} 

}

\caption{Painéis do Rstudio}(\#fig:paineis)
\end{figure}

- **Fonte/Editor de Scripts**: se constitui do ambiente onde serão abertos os scripts previamente salvos nos mais diversos formatos ou mesmo sendo o local de visualização das bases de dados.
- **Console**: local onde será efetuada a digitação das linhas de código que serão interpretadas pelo R.
- **Ambiente e Histórico**: o ambiente será visualizado os objetos criados ou carregados durante a seção e; a aba History retoma os scripts digitados no console.
- **Plots/arquivos/Pacotes**: local onde podem ser acessados os arquivos salvos no computador pela aba *files*; a aba *Plots* carrega os gráficos e plotagens; a aba *Packages* contém os pacotes instalados em seu computador, onde são ativados ou instalados novos; em *Help* constam as ajudas e explicações dos pacotes e; *Viewer* vizualiza documentos do tipo html.

## Help

Acessamos a ajuda do RStudio por meio do comando `help()`, através da aba "Help" ou ao clicar no nome do pacote. Pode-se digitar a ajuda que usuário necessita (exemplo `help("summary")`), ou diretamente no colsole digitamos ? e a função desejada, exemplo: `?mean`.

## Instalação de pacotes

Em alguns situações, o uso de pacotes pode dar ao trabalho mais praticidade, e para isso se faz necessário efetuar a sua instalação. Precisamos ir até o painel dos pacotes em *packages}, selecionar a opção instalar e inserir o nome do pacote desejado na janela indicada. Ao selecionar a opção instalar, no console receberemos informações do procedimento e do sucesso do mesmo. 


\begin{figure}

{\centering \includegraphics[width=\textwidth]{pacotes,1} 

}

\caption{Instalação de pacotes}(\#fig:pacotes1)
\end{figure}

\begin{figure}

{\centering \includegraphics[width=\textwidth]{pacotes,2} 

}

\caption{Caixa de informação de pacote a ser instalado}(\#fig:pacotes2)
\end{figure}

A mesma função, para instalação de um pacote, pode ser efetuada diretamente via console: `install.packages("pacote")`. É importante ressaltar a função `library(nomedopacote)` que é utilizada no console para informar ao R e "carregar" o pacote que o usuário irá utilizar. Podem ser instalados mais de um pacote ao mesmo tempo, como no exemplo:


`install.packages(c("readr", "readxl"))`


## Abrir arquivo de dados

Dispondo de um banco de dados em uma planilha eletrônica (LibreOffice Calc ou EXCEL), neste caso será utilizado o arquivo  ["árvores"](https://github.com/Smolski/softwarelivrer/raw/master/basico/arvores.xlsx) como exemplo o banco de dados. Os dados derivam de uma pesquisa com espécies de árvores registrando as variáveis diâmetro altura do peito (DAP) e altura. Dados cedidos pela professora Tatiane Chassot.

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

A opção `load()` (exemplo: `load("base.RData")`) pode ser utilizada para carregar as bases de dados salvas com a função `save()`, que será descrita no subcapítulo a seguir.

Outra opção é o carregamento das bases de dados manualmente pelo caminho *Envoirment $>$ Import Dataset*, escolhendo o tipo de arquivo:

\begin{figure}

{\centering \includegraphics[width=\textwidth]{r3} 

}

\caption{Aba *Import Dataset*}(\#fig:r3)
\end{figure}

Na caixa correspondente a File/Url se insere o endereço virtual ou o local onde se encontra o arquivo. Ao importar os dados, carrega-se um objeto criado com as informações contidas no arquivo. No nosso exeplo, carregamos a planilha arvores (arquivo .xls) como mostra a Figura \@ref(fig:r4), derivado do caminho "Import Dataset $>$ From Excel" do Environment.

\begin{figure}

{\centering \includegraphics[width=\textwidth]{r4} 

}

\caption{Caixa de informações do Import Data}(\#fig:r4)
\end{figure}

O campo *Code Preview* mostra o comando que está sendo criado para a importação destes dados. Em *Import Options*, delimita-se opções do objeto como o nome (*name*), o número máximo de linhas (*Max Rows*), quantas linhas serão puladas na importação do arquivo (*Skip*), o tratamento das células em branco (*NA*) e se a primeira linha contém os nomes (*Firts Row as Names*).

Com relação à importação de arquivos de texto separado por caracteres (.csv), ela se dá via "Import Dataset $>$ From Text (readr)" do Environment. Constam algumas solicitações diferentes a serem determinadas pelo usuário no campo *Import Options*, conforme mostra a Figura \@ref(fig:r4csv). Uma questão importante é a opção *Delimiter*, a qual o pesquisador tem que prestar atenção quando o arquivo está separado por vírgulas (*Comma*), ponto e vírgula (*Semicolon*) ou outro tipo de caractere. A opção *Locale $>$ Configure...* oportuniza determinar os tipos de marca decimal e codificação de textos, por exemplo.

\begin{figure}

{\centering \includegraphics[width=\textwidth]{r4csv} 

}

\caption{Opções da importação de arquivos .csv}(\#fig:r4csv)
\end{figure}

Importante mencionar que em ambos os casos de importação, no campo *Dada Preview* onde constam os dados do arquivo a ser importado, é possível determinar o tipo de dado que cada "coluna" contém. Isto é extremamente importante, pois campos que possuem números, que serão posteriormente utilizados em operações aritméticas, por exemplo, devem ser configurados como tal. No entanto, como será visto adiante, a alteração do tipo do dado também pode ser feita posteriormente sem problema algum.

Alguns tipos de dados:

- **Numeric**: números, valores decimais em geral (`5.4`).
- **Integer**: números (`4`).
- **Character**: variável de texto, ou *string} (`casa`).
- **Double**: cria um vetor de precisão dupla, que abarca os números.
- **Logical**: operadores booleanos (`TRUE, FALSE`).
- **Date**: opção para datas.
- **Time**: vetor para séries de tempo.
- **Factor**: variável nominal, inclusive como fator ordenado, representam categorias.

## Salvar arquivo de dados

O banco de dados que o R armazena na memória pode ser salvo, junto com todo o ambiente, usando o ícone de disquete na aba "Environment" (salva como arquivo .RData), e depois carregado pelo ícone de pasta (Abrir dados...) na mesma aba. Desta forma, salvará todos os objetos criados no ambiente de trabalho.

\begin{figure}

{\centering \includegraphics[width=\textwidth]{r6} 

}

\caption{Atalho para abrir e salvar arquivo de dados}(\#fig:r6)
\end{figure}

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

## Criação de variáveis

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

### Conversão de uma variável

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

## Alguns comandos essenciais

A função `head()` mostra as 6 primeiras colunas do arquivo para se ter uma noção do conteúdo. No caso do mesmo ser um data.frame, podemos solicitar o número de valores ou linhas a serem mostrados no console através do parâmetro n ou na ausência deste, todas as linhas serão impressas, como exemplo `head(x ,n=2)` para ver as duas primeiras linhas. 

O comando `summary()` efetua o resumo dos dados, se for qualitativa mostra a frequência absoluta das categorias e se for quantitativa apresenta as categorias. No exemplo abaixo trabalharemos com uma base de dados de treinamento denominada "iris" que está acessível no *software} RStudio através do comando que carrega dados específicos `data()`:


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


### Comando *tapply*

O comando `taply()` agrega os dados pelos níveis das variáveis qualitativas. Note que a coluna "Especie" possui dados em forma de fatores. Assim, para filtrarmos a informação (coluna "Sepal.Length") média por Especie, podemos utilizar:


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

### Comando *subset*

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

## Estrutura de dados

### Vetores

Os fatores são uma classe especial de vetores, que definem variáveis categóricas de classificação, como os tratamentos em um experimento fatorial, ou categorias em uma tabela de contingência.


```r
# Criação de um vetor
x= c(2, 4, 6)
x
```

```
[1] 2 4 6
```

Os vetores podem ser criados a partir de uma sequência numérica ou mesmo de um intervalo entre valores:


```r
x= c(2:6)
x
```

```
[1] 2 3 4 5 6
```

```r
# Criação de um vetor a partir do intervalo entre cada elemento e valores
#mínimo e máximo
x= seq(2, 3, by=0.5)
x
```

```
[1] 2.0 2.5 3.0
```

Criação de um vetor atráves de uma repetição também é útil em várias situações. No primeiro exemplo repete o intervalo de 1 a 3 4 vezes e no segundo exemplo, a cada 3 vezes:


```r
x= rep(1:3, times=4)
x
```

```
 [1] 1 2 3 1 2 3 1 2 3 1 2 3
```

```r
y= rep(1:3, each=3)
y
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

#### Função *table*

Para contar elementos em cada nível de um fator, usa-se a função table:


```r
table(participantes)
```

```
participantes
mulheres   homens 
      10        0 
```

A função pode fazer tabulações cruzadas, gerando uma tabela de contingência, esse tipo de tabela é usado para registrar observações independentes de duas ou mais variáveis aleatórias: 



```r
table(sexo,dieta)
```

```
    dieta
sexo normal light diet
   F      3     3    3
   M      3     3    3
```

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

#### Comandos para manipulação de listas

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

## Função *edit*

Esta função abre uma interface simples de edição de dados em formato planilha, e é útil para pequenas modificações. Mas para salvar as modificações atribua o resultado da função `edit` a um objeto.

Utiliza-se o comando da seguinte forma: 

\noindent
`novonomedabase = edit(nomeatualdabase)`


```r
informacoes.2=edit(informacoes)
```

\begin{figure}

{\centering \includegraphics[width=\textwidth]{95} 

}

\caption{Editor de dados}(\#fig:95)
\end{figure}

Basta clicar no retângulo correspondente a variável que deseja ser modificada, excluir ou adicionar novas colunas.

\begin{figure}

{\centering \includegraphics[width=\textwidth]{10} 

}

\caption{Acréscimo de uma nova coluna através do editor de dados}(\#fig:10)
\end{figure}

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

## Funções

As funções a seguir são aplicáveis a vetores, data.frames e listas, e em muitos casos trazem praticidade a uma análise estatística. Foram criados objetos com informações do nome dos estudantes e altura. Segue o processo de criação do *data frame} com estas informações, lembrando que esta forma de "união" das informações pressupõe que a ordem dos dados esteja correta:


```r
# União de um banco de dados (existencia de uma váriavel em comum)

estudantes=c("Guilherme", "Marcelo", "Pedro", "Camila")
altura= c(1.50, 1.9, 1.74, 1.80)
informacoes.3=data.frame(estudantes, altura)
```

Já o comando `merge()` serve para juntar dois *data frames} que possuam uma coluna em comum. Neste caso, unimos o objeto `informações.2` com o objeto `informações.3` utilizando o nome dos estudantes (informação em comum):


```r
informacoes=merge(informacoes.2,informacoes.3, by="estudantes")
```

Adicionar um cálculo entre as colunas é muito simples com o RStudio, neste caso com os dados do peso e altura, pode-se calcular o IMC (Índice de Massa Corporal) em uma nova coluna:


```r
informacoes$Imc=c(peso/(altura^2))
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 28.89
2  Guilherme    18  100 Porto Alegre   1.50 21.88
3    Marcelo    17   80     Soledade   1.90 26.42
4      Pedro    17   79      Gramado   1.74 30.86
```

Ainda, se houver linhas que tenham pelo menos uma informação faltante (NA), estas podem ser excluídas com o comando `na.omit()`, ou mesmo os NAs serem substituídos por outro caractere (neste caso foi substituído por zero) com o comando `is.na`:


```r
# Retirar as linhas que tenham pelo menos um NA:

informacoes<- na.omit(informacoes)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 28.89
2  Guilherme    18  100 Porto Alegre   1.50 21.88
3    Marcelo    17   80     Soledade   1.90 26.42
4      Pedro    17   79      Gramado   1.74 30.86
```

```r
# Substituir NA's por zero no data.frame

informacoes[is.na(informacoes)] = 0
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 28.89
2  Guilherme    18  100 Porto Alegre   1.50 21.88
3    Marcelo    17   80     Soledade   1.90 26.42
4      Pedro    17   79      Gramado   1.74 30.86
```

Outro recurso interessante é a substituição de dados em uma columa, que pode ser feito de forma automática para uma condição padrão escolhida. No exemplo abaixo, substituimos aquelas informações de idade igual a 17 pelo número 19:


```r
# Substituir números na coluna
informacoes$idade[informacoes$idade == 17] <- 19
informacoes
```

```
  estudantes idade peso      cidades altura   Imc
1     Camila    21   65   Nova Hartz   1.80 28.89
2  Guilherme    18  100 Porto Alegre   1.50 21.88
3    Marcelo    19   80     Soledade   1.90 26.42
4      Pedro    19   79      Gramado   1.74 30.86
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
1     Camila    21   65   Nova Hartz   1.80 28.89 excesso de peso
2  Guilherme    18  100 Porto Alegre   1.50 21.88     peso normal
3    Marcelo    19   80     Soledade   1.90 26.42 excesso de peso
4      Pedro    19   79      Gramado   1.74 30.86 excesso de peso
```


```
Carregando pacotes exigidos: knitr
```

```
Carregando pacotes exigidos: kableExtra
```

\begin{table}

\caption{(\#tab:IMC)Valores padrão para o IMC}
\centering
\begin{tabular}[t]{l|l}
\hline
Resultado & Situação\\
\hline
Abaixo de 17 & Muito abaixo do peso\\
\hline
Entre 17 e 18,49 & Abaixo do peso\\
\hline
Entre 18,5 e 24,99 & Peso normal\\
\hline
Entre 25 e 29,99 & Acima do peso\\
\hline
Entre 30 e 34,99 & Obesidade I\\
\hline
Entre 35 e 39,99 & Obesidade II (severa)\\
\hline
Acima de 40 & Obesidade III (mórbida)\\
\hline
\multicolumn{2}{l}{\textit{Note: }}\\
\multicolumn{2}{l}{Fonte: @brasil2014.}\\
\end{tabular}
\end{table}


No entanto, o IMC possui várias classificações de acordo com o seu resultado (Tabela \@ref(tab:IMC)), sendo que, por exemplo, resultados abaixo de 17 informam que o indivíduo se encontra como Muito abaixo do peso, e acima de 40, se encontra em Obesidade III. Para efetuar a classificação desta maneira utilizando o comando `ifelse`, ou seja, com mais de uma condição, pode ser efetuada a estruturação com a aglutinação do comando:


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
1     Camila    21   65   Nova Hartz   1.80 28.89 excesso de peso Acima do Peso
2  Guilherme    18  100 Porto Alegre   1.50 21.88     peso normal   Peso Normal
3    Marcelo    19   80     Soledade   1.90 26.42 excesso de peso Acima do Peso
4      Pedro    19   79      Gramado   1.74 30.86 excesso de peso   Obesidade I
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
1     Camila    21   65   Nova Hartz   1.80 28.89 excesso de peso Acima do Peso
2  Guilherme    18  100 Porto Alegre   1.50 21.88     peso normal   Peso Normal
3    Marcelo    19   80     Soledade   1.90 26.42 excesso de peso Acima do Peso
4      Pedro    19   79      Gramado   1.74 30.86 excesso de peso   Obesidade I
  binario
1       0
2       1
3       0
4       0
```

O comando `rbind()` é utilizado para incluir linhas novas abaixo de um objeto já criado pelo pesquisador, sendo que é importante o cuidado de que estas novas informações tenham os mesmos campos (colunas). A exemplo, pede-se para incluir uma nova pessoa no *data frame} informacoes: Francisco, 30 anos de idade, peso 59, natural de Ijuí, IMC 21.3387, classificado como peso normal. Lembrando de incluir os campos "tipoimc" e "binario".


```r
novo1=data.frame(estudantes="Francisco", idade=30, peso=59, 
                 cidades="Ijuí", 
                 altura="1,59", 
                 Imc= 23.30, 
                 classificacao= "peso normal",
                 tipoimc="Peso Normal", 
                 binario=1)
informacoes=rbind(informacoes, novo1)
informacoes
```

```
  estudantes idade peso      cidades altura   Imc   classificacao       tipoimc
1     Camila    21   65   Nova Hartz    1.8 28.89 excesso de peso Acima do Peso
2  Guilherme    18  100 Porto Alegre    1.5 21.88     peso normal   Peso Normal
3    Marcelo    19   80     Soledade    1.9 26.42 excesso de peso Acima do Peso
4      Pedro    19   79      Gramado   1.74 30.86 excesso de peso   Obesidade I
5  Francisco    30   59         Ijuí   1,59 23.30     peso normal   Peso Normal
  binario
1       0
2       1
3       0
4       0
5       1
```

Outra forma de incluir informações adicionais nos *data frames} através de atributos é utilizando o pacote `dplyr`. Decide-se criar um campo "faixa etária", sendo que aqueles indivíduos com idade acima de 21 chamaremos de "adulto" e do contrário "não adulto".


```r
library(dplyr)
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
1     Camila    21   65   Nova Hartz    1.8 28.89 excesso de peso Acima do Peso
2  Guilherme    18  100 Porto Alegre    1.5 21.88     peso normal   Peso Normal
3    Marcelo    19   80     Soledade    1.9 26.42 excesso de peso Acima do Peso
4      Pedro    19   79      Gramado   1.74 30.86 excesso de peso   Obesidade I
5  Francisco    30   59         Ijuí   1,59 23.30     peso normal   Peso Normal
  binario faixa etaria
1       0       adulto
2       1   não adulto
3       0   não adulto
4       0   não adulto
5       1       adulto
```

A (re)ordenação das colunas de um *data frame* pode ser muito útil em alguns casos, sendo extremamente fácil efetuá-la, cada número representa o número da respectiva coluna:


```r
# Reordenar colunas
informacoes=informacoes[c(8,2,3,4,1,6,5,7,9)]
```

Caso se queira a inversão total da ordem das colunas do objeto estudado, o comando `rev()` pode ser útil:


```r
# Inversão do posicionamento dos elementos
rev(informacoes)
```

```
  binario   classificacao altura   Imc estudantes      cidades peso idade
1       0 excesso de peso    1.8 28.89     Camila   Nova Hartz   65    21
2       1     peso normal    1.5 21.88  Guilherme Porto Alegre  100    18
3       0 excesso de peso    1.9 26.42    Marcelo     Soledade   80    19
4       0 excesso de peso   1.74 30.86      Pedro      Gramado   79    19
5       1     peso normal   1,59 23.30  Francisco         Ijuí   59    30
        tipoimc
1 Acima do Peso
2   Peso Normal
3 Acima do Peso
4   Obesidade I
5   Peso Normal
```

A  função `table()` faz a contagem os dados; já o comando `sort()` ordena os objetos em ordem crescente (caso queira no formato decrescente, informar `decreasing=TRUE`).


```r
# contagem de objetos
table(informacoes$classificacao)
```

```

excesso de peso     peso normal 
              3               2 
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
5   Peso Normal    30   59         Ijuí  Francisco 23.30   1,59     peso normal
1 Acima do Peso    21   65   Nova Hartz     Camila 28.89    1.8 excesso de peso
3 Acima do Peso    19   80     Soledade    Marcelo 26.42    1.9 excesso de peso
4   Obesidade I    19   79      Gramado      Pedro 30.86   1.74 excesso de peso
2   Peso Normal    18  100 Porto Alegre  Guilherme 21.88    1.5     peso normal
  binario
5       1
1       0
3       0
4       0
2       1
```

```r
#ordem crescente
informacoes[order(informacoes$idade, decreasing = FALSE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
2   Peso Normal    18  100 Porto Alegre  Guilherme 21.88    1.5     peso normal
3 Acima do Peso    19   80     Soledade    Marcelo 26.42    1.9 excesso de peso
4   Obesidade I    19   79      Gramado      Pedro 30.86   1.74 excesso de peso
1 Acima do Peso    21   65   Nova Hartz     Camila 28.89    1.8 excesso de peso
5   Peso Normal    30   59         Ijuí  Francisco 23.30   1,59     peso normal
  binario
2       1
3       0
4       0
1       0
5       1
```

```r
#ordem crescente
informacoes[order(informacoes$cidades, decreasing = FALSE),]
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
4   Obesidade I    19   79      Gramado      Pedro 30.86   1.74 excesso de peso
5   Peso Normal    30   59         Ijuí  Francisco 23.30   1,59     peso normal
1 Acima do Peso    21   65   Nova Hartz     Camila 28.89    1.8 excesso de peso
2   Peso Normal    18  100 Porto Alegre  Guilherme 21.88    1.5     peso normal
3 Acima do Peso    19   80     Soledade    Marcelo 26.42    1.9 excesso de peso
  binario
4       0
5       1
1       0
2       1
3       0
```

O comando `rank()` cria uma ranqueamento crescente das informações. Se pretende-se, por exemplo, criar uma coluna com o ranking dos valores do IMC, pode ser utilizado:


```r
informacoes$rankingImc=rank(informacoes$Imc)
informacoes
```

```
        tipoimc idade peso      cidades estudantes   Imc altura   classificacao
1 Acima do Peso    21   65   Nova Hartz     Camila 28.89    1.8 excesso de peso
2   Peso Normal    18  100 Porto Alegre  Guilherme 21.88    1.5     peso normal
3 Acima do Peso    19   80     Soledade    Marcelo 26.42    1.9 excesso de peso
4   Obesidade I    19   79      Gramado      Pedro 30.86   1.74 excesso de peso
5   Peso Normal    30   59         Ijuí  Francisco 23.30   1,59     peso normal
  binario rankingImc
1       0          4
2       1          1
3       0          3
4       0          5
5       1          2
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
[1] Pedro
Levels: Camila Guilherme Marcelo Pedro Francisco
```

O arredondamento de valores numéricos pode ser feito utilizando o comando `round()`, o qual o pesquisador informa o número de casas decimais:


```r
# Arredondar para n casas decimais
round(informacoes$Imc, 2)
```

```
[1] 28.89 21.88 26.42 30.86 23.30
```

Já o comando `signif()` determina onúmero de algarismos significativos da série escolhida, ou seja, ele arredonda para os valores em seu primeiro argumento com os número de dígitos detemrinados: 


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

# Estatística Descritiva {#desc}

# Estatística Inferencial{#inf}

# Teste de Qui-Quadrado {#qui}

# Modelos de Regressão {#reg}

# RMarkdown {#rmark}

# Referências {-}




<!--chapter:end:index.Rmd-->

