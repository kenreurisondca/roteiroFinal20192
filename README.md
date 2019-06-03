---
title: "Roteiro do último laboratório"
author: Prof. Kennedy R. Lopes
date: \today
header-includes:
  - \usepackage[brazilian]{babel}
  - \usepackage[utf8]{inputenc}
  - \usepackage[T1]{fontenc}
  - \usepackage{longtable,booktabs}
incremental: false  
theme: "Frankfurt"  
colortheme: "beaver"
---

# Apresentação

#### Computador de Propósito Geral

Os computadores atuais são resultados de diversas tentativas em desenvolver uma máquina eficiente para cálculo. Se por um lado existem dispositivos rápidos que se dedicam a realizar uma única operação, os computadores de propósito geral são capazes de realizar uma sequência de instruções pré-programadas com velocidade compatível ao _clock_ do dispositivo.

# Computador NEANDER
Principais características:

- Largura de dados e de endereços de 8 bits
- Dados representados em complemento de dois
- Modo de endereçamento: direto
- 1 registrador acumulador de 8 bits
- 1 apontador de programa de 8 bits
- 1 registrador de estado com 2 códigos de condição: negativo e zero

# Conjunto de Instruções
|Código|Instrução|Operação|
|:---------|:------------|:-------------------------------------------------------------|
|0000|NOP    |Nenhuma Operação|
|0001|STA end|Armazena acumulador no endereço “end” da memória|
|0010|LDA end|Carrega o acumulador com o conteúdo do endereço “end” da memória|
|0011|ADD end|Soma o conteúdo do endereço “end” da memória ao acumulador|
|0100|OR  end|Efetua operação lógica “OU” do conteúdo do endereço “end” da memória ao acumulador|
  : legenda
  :ref: legenda1

# Conjunto de Instruções
|Código|Instrução|Operação|
|:---------|:------------|:-------------------------------------------------------------|
|0101|AND end|Efetua operação lógica “E” do conteúdo do endereço “end” da memória ao acumulador|
|0110|JMP end|Desvio incondicional para o endereço “end” da memória|
|1001|JN  end|Desvio condicional, se “N=1”, para o endereço “end” da memória|
|1010|JZ  end|Desvio condicional, se “Z=1”, para o endereço “end” da memória|
|1111|HLT	   |Para o ciclo de busca-decodificação-execução|

# Diagrama geral


# Referencias
1. https://www.overleaf.com/project/5cf493298a48086e11478c95
2. Markdown Command:
```
pandoc -t beamer principal.md -o principal.pdf
```
3. https://commonmark.org/help/
4. https://gist.github.com/mufid/4062574
5. https://bookdown.org/yihui/rmarkdown/prettydoc.html
