---
title: Números Naturais e Indução
description: >-
  Propriedades dos Números Naturais.
  Princípio da Boa Ordenação
  Princípio da Indução Finita.
path: /itn/naturais-e-inducao
type: content
---

# Números Naturais e Indução

```toc

```

## Propriedades dos Números Naturais

O conjunto dos **números naturais** são todos os números inteiros não negativos. Nesta cadeira o zero _pertence_ ao conjunto!

$$
\mathbb{N} = \lbrace 0,1,2,3, \ldots \rbrace
$$

Consideremos também as operações de [**soma**](color:green) e de [**produto**](color:red). A subtração é só a soma com o simétrico, e a divisão nem sempre devolve números inteiros, por isso não a consideraremos por enquanto.

:::info[Propriedades dos Números Naturais]

$\forall a,b,c \in \mathbb{N}$

[**Associatividade da Soma**](color:green): $\lparen a+b \rparen +c= a+ \lparen b+c \rparen$

[**Comutatividade da Soma**](color:green): $a+b=b+a$

[**Lei do Corte para a Soma**](color:green): $a+c=b+c \Rarr a=b$

[**Elemento Neutro da Soma**](color:green): $a+0=a$

[**Associatividade do Produto**](color:red): $\lparen ab \rparen c= a \lparen bc \rparen$

[**Comutatividade do Produto**](color:red): $ab=ba$

[**Lei do Corte para o Produto**](color:red): $ac=bc \and c \neq 0 \Rarr a=b$

[**Elemento Neutro do Produto**](color:red): $a1=a$

[**Distributividade**](color:orange): $a(b+c)=ab+ac$

:::

### Princípio da Boa Ordenação

Uma propriedade importante do conjunto dos números naturais é que **para qualquer subconjunto dele, existe um primeiro elemento**. Ou seja, $X\subset \mathbb{N},\exists x_{0} \in X:x< x_{0} \Longrightarrow x\notin X$. Este $x_0$ é menor ou igual do que qualquer elemento de $X$, logo se houver um número natural menor do que $x_0$, não pertence a $X$.


:::tip[Exemplos]

$X= \left\{1,3,4 \right\}\Rightarrow x_0=1\in\mathbb{N}$

$X= \left\{0,10,11,12 \right\}\Rightarrow x_0=0\in\mathbb{N}$

$X= \left\{5,6,7,\dots \right\}\Rightarrow x_0=5\in\mathbb{N}$

:::



## Indução Finita

A **indução** é um método utilizado para provar proposições.

Este método é particularmente útil para **somatórios**, pois dependem de um valor máximo variável, onde podemos aplicar a indução.

Temos uma proposição que é válida para qualquer $n$ natural (ou para algum subconjunto de $\mathbb{N}$).

- Primeiro temos de provar que é verdade para o $n$ mais pequeno.
- De seguida, temos de provar que, supondo que é verdade para um $n$, também é verdade para $n+1$.
Se conseguirmos fazer estes dois passos, provamos com sucesso a proposição.


:::tip[Exemplo]

Consideremos a seguinte proposição:

$$\sum_{i=1}^{n} i=\frac{n\left(n+1\right)}{2} \forall n\geq 1$$

Para começar, podemos notar que a variável ($n$) pode ser no mínimo $1$. Então $n$ vai pertencer sempre a um subconjunto dos números naturais, $\mathbb{N}$, logo pelo [**Princípio da Boa Ordenação**](color:orange) o elemento $1$ será menor ou igual do que qualquer elemento do subconjunto.

Então, aplicaremos o primeiro passo a $1$. Temos de verificar que a proposição de facto é verdade para $n=1$:

$$\sum_{i=1}^{1} i=1=\frac{1\left(1+1\right)}{2}$$

*É verdade!* Ambos os lados da proposição dão 1. Agora podemos proceder ao **passo de indução**: temos de provar que _assumindo que é verdade para um $n$, também é para $n+1$._

$$\sum_{i=1}^{n+1} i$$

E agora? Sabemos que um somatório é uma soma de $n$ elementos. Então, somar $n+1$ elementos é a mesma coisa do que somar $n$ elementos e depois o elemento $n+1$.

$$\sum_{i=1}^{n+1} i=n+1 + \sum_{i=1}^{n} i$$

Mas lembra-te que estamos a assumir a proposição para $n$! Logo, supomos que $\sum_{i=1}^{n} i=\frac{n\left(n+1\right)}{2}$.

Substituindo isso na expressão anterior,

$$n+1 + \sum_{i=1}^{n} i=n+1 + \left(\frac{n\left(n+1\right)}{2}\right)$$

Agora temos de simplificar a expressão para mostrar que dá $\frac{\left(n+1\right)\left(n+2\right)}{2}$.

$$n+1 + \left(\frac{n\left(n+1\right)}{2}\right) = \\
= \frac{2n+2}{2} + \frac{n\left(n+1\right)}{2} = \\
= \frac{2n+2+n\left(n+1\right)}{2} = \\
= \frac{2\left(n+1\right)+n\left(n+1\right)}{2}= \\
= \frac{\left(n+1\right) \left(n+2\right)}{2}$$

E assim conseguimos provar o passo de indução! Com estes dois passos, **provámos a proposição com sucesso!**

:::

Como vimos no exemplo, a técnica principal é **criar o caso pressuposto a partir do que se quer provar,** substituí-lo pela assunção e simplificar. Mas cuidado, pois pode ser mais complexo do que isso.

