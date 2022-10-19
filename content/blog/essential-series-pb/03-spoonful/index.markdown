---
title: "Como definir (e achar) o diretório de trabalho (#01)"
weight: 3
subtitle: "Como dizer ao RStudio para encontrar nossos arquivos de dados"
excerpt: "Como dizer ao RStudio para encontrar nossos arquivos de dados"
date: 2022-10-19
draft: false
---

É possível gerar arquivos no próprio *script* do RStudio, mas, geralmente, nós queremos importar nossos dados e trabalhar com eles. Por exemplo, podemos importar dados de um estudo psicolinguístico e fazer transformações e testes estatísticos com eles. Para isso, em qualquer *script*, nós precisamos dizer ao RStudio (*com carinho, sempre*) **onde** estão nossos arquivos. Vamos aprender sobre as funções `setwd()` e `getwd()` ?

## O que é o diretório de trabalho? 

O **working directory** é, essencialmente, a pasta em seu computador em que seus arquivos brutos estão. Portanto, se queremos que o RStudio ache esses arquivos, precisamos informá-lo qual é o **path** dessa pasta.

## setwd()

Em nossos computadores, nós usualmente temos muitos arquivos, cada um em uma pasta, certo? Cada um desses arquivos pode ser encontrado por um ***path*** (um ***caminho***). Isto é, cada arquivo tem um caminho único para ser encontrado.

> Supondo que você tenha uma pasta em "documentos" chamada "Masters" e, dentro dela, uma subpasta chamada "Research_Data":

![](images/paste-47F99758.png)

> Podemos ver que a pasta "Research_Data" está dentro da subpasta "Masters", que, por sua vez, está dentro de "Documentos" que, por sua vez, está dentro "Deste Computador". É **exatamente isso** que você precisa dizer ao RStudio, que, infelizmente, (ainda) não tem como advinhar sozinho onde seus arquivos estão. <br>
Há [diversas](https://pt.wikihow.com/Encontrar-o-Caminho-de-um-Arquivo-no-Windows#:~:text=Para%20copiar%20o%20caminho%20do,V%20para%20finalizar%20o%20processo.) formas de encontrar os caminhos para pastas e arquivos dentro do próprio Windows (nunca usei um Macbook, então infelizmente não sei dizer como seria no Mac).

Bom, ótimo, então, você só precisa dizer ao RStudio com a função `setwd()` (ler: *set working directory* ou *defina o diretório de trabalho*) qual é a path da pasta em que seus dados estão, assim:

> setwd("C:/Users/laris/Documents/Masters/Research_Data")

Outra forma de fazer isso é pelo **menu de opções** do RStudio que, por default, fica à direita do console. Assim:

![](images/paste-24016D46.png)

Como disse acima, há diversas formas de saber qual é a path do seu diretório de trabalho diretamente no Windows, mas, e se você quiser saber dentro do próprio RStudio?

## getwd()

É aqui que a função `getwd()` entra em jogo. Podemos usar `getwd()` (ler: *get working directory* ou *pegue o diretório de trabalho*) para que o próprio RStudio nos diga qual é o nosso atual diretório de trabalho.

> getwd()
>
> \[1\] "C:/Users/laris/Documents/Masters/Research_Data"

Sempre confira se seus dados estão na pasta certa. Confira sempre se você está trabalhando em seu diretório de trabalho. Às vezes o RStudio nos retorna erros como "não foi possível encontrar o arquivo tal" justamente por estarmos na pasta errada! 

Algo **bem** útil é usar ```getwd()``` e copiar no ```setwd()``` para economizarmos tempo de digitação! &#128521;

Dito isso, hoje há modos mais otimizados para se fazer isso, por meio de *projetos*, mas vamos falar sobre eles depois. Até lá! 

&#128021; Au-au! Hoje aprendemos que todo arquivo em nossos computadores têm um *path* e que precisamos dizer ao RStudio qual é esse *path* para que ele encontre nossos arquivos de dados. Fazemos isso por meio da função ```setwd()```. Se quisermos que o próprio RStudio nos indique qual é o atual diretório de trabalho, podemos usar ```getwd()``` para descobrirmos! Para economizarmos tempo, podemos colar o output de ```getwd()``` em ```setwd()```. Até a próxima! 
