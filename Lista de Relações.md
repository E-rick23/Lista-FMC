
## Questão 1

#### Para quaisquer relações $R, S \subseteq A \times B$  mostre:

### a) $(R^{-1})^{-1} = R$

> $\# R^{-1} = \{(b, a) \in B \times A \mid (a, b) \in R\}$

Tome $(a, b) \in A \times B$ qualquer,

$$\begin{aligned} (a, b) \in (R^{-1})^{-1} &\iff (b, a) \in R^{-1} \quad (\text{def. de relação inversa}) \\ &\iff (a, b) \in R \quad (\text{def. de relação inversa}) \end{aligned}$$

Portanto, $(R^{-1})^{-1} = R$.

---

### b) $(R \cup S)^{-1} = R^{-1} \cup S^{-1}$

Tome $(b, a) \in B \times A$ qualquer

$$\begin{aligned} (b, a) \in (R \cup S)^{-1} &\iff (a, b) \in (R \cup S) \quad (\text{def. relação inversa}) \\ &\iff (a, b) \in R \text{ ou } (a, b) \in S \quad (\text{def. união}) \\ &\iff (b, a) \in R^{-1} \text{ ou } (b, a) \in S^{-1} \quad (\text{def. relação inversa}) \\ &\iff (b, a) \in R^{-1} \cup S^{-1} \quad (\text{def. união}) \end{aligned}$$

Portanto, $(R \cup S)^{-1} = R^{-1} \cup S^{-1}$.

---

### c) $(R \cap S)^{-1} = R^{-1} \cap S^{-1}$

Tome $(b, a) \in B \times A$ qualquer

$$\begin{aligned} (b, a) \in (R \cap S)^{-1} &\iff (a, b) \in (R \cap S) \quad (\text{def. relação inversa}) \\ &\iff (a, b) \in R \text{ e } (a, b) \in S \quad (\text{def. de intersecção}) \\ &\iff (b, a) \in R^{-1} \text{ e } (b, a) \in S^{-1} \quad (\text{def. de relação inversa}) \\ &\iff (b, a) \in R^{-1} \cap S^{-1} \end{aligned}$$

Portanto, $(R \cap S)^{-1} = R^{-1} \cap S^{-1}$.

---

### d) $(R')^{-1} = (R^{-1})'$, onde $R'$ é o complementar de $R$, def $R' = (A \times B) - R$.

Tome $(b, a) \in B \times A$ qualquer

$$\begin{aligned} (b, a) \in (R')^{-1} &\iff (a, b) \in R' \quad (\text{def. relação inversa}) \\ &\iff (a, b) \in (A \times B) - R \quad (\text{def. complementar}) \\ &\iff (a, b) \in A \times B \text{ e } (a, b) \notin R \quad (\text{def. de diferença}) \\ &\iff (b, a) \in B \times A \text{ e } (a, b) \notin R \quad (\text{def. produto cartesiano}) \\ &\iff (b, a) \in B \times A \text{ e } (b, a) \notin R^{-1} \quad (\text{def. relação inversa}) \\ &\iff (b, a) \in (B \times A) - R^{-1} \quad (\text{def. de diferença}) \\ &\iff (b, a) \in (R^{-1})' \quad (\text{def. de complementar}) \end{aligned}$$

Portanto, $(R')^{-1} = (R^{-1})'$.

---

## Questão 2:
#### Dadas quaisquer relações binárias $R$ e $S$, mostre que $(R \circ S)^{-1} = S^{-1} \circ R^{-1}$.

> $\# (a, c) \in R \circ S \iff \exists b \text{ tq } \underbrace{(a, b) \in S}_{aRb} \text{ e } \underbrace{(b, c) \in R}_{bRc}$

Tome então $(c, a)$ qualquer:

$$\begin{aligned} (c, a) \in (R \circ S)^{-1} &\iff (a, c) \in R \circ S \quad (\text{def. relação inversa}) \\ &\iff \exists b \text{ tq } (a, b) \in S \text{ e } (b, c) \in R \quad (\text{def. de relação composta}) \\ &\iff \exists b \text{ tq } (b, a) \in S^{-1} \text{ e } (c, b) \in R^{-1} \quad (\text{def. relação inversa}) \\ &\iff (c, a) \in S^{-1} \circ R^{-1} \quad (\text{def. de relação composta}) \end{aligned}$$

Portanto, $(R \circ S)^{-1} = S^{-1} \circ R^{-1}$.

---
# Questão 5

Considere $len(w)$ como a quantidade de dígitos de uma string $w \in 2^* $.
Para todo $n \in \mathbb{Z}^+$, considere a definição simplificada da relação $\sim_n \subseteq 2^* \times 2^* $, tal que para quaisquer $a, b \in 2^*$:

* **Caso 1:** se $len(a) < n$ e $len(b) < n \text{ então, } (a,b) \in \sim_n$
* **Caso 2:** se $len(a) \ge n$ e $len(b) \ge n$ e os $n$ primeiros dígitos de $a$ e $b$ forem iguais $\text{ então, } (a,b) \in \sim_n$

## 5.A)

Por definição, para provar que $\sim_n$ é uma relação de equivalência, devemos mostrar que ela é reflexiva, simétrica e transitiva. Tome um $n \in \mathbb{Z}^+$ arbitrário.

### $\sim_n$ é Simétrica:
Tome $x, y \in 2^*$ arbitrários, suponha que $(x,y) \in \sim_n$. Pela definição de $\sim_n$ temos 2 casos possíveis:

* **Caso 1:** Como $len(y) < n$ e $len(x) < n$, então $(y,x) \in \sim_n$ por def. $\sim_n$ caso 1.
* **Caso 2:** Como $len(y) \ge n$ e $len(x) \ge n$ e, pela simetria da igualdade, os $n$ primeiros dígitos de $y$ são iguais aos $n$ primeiros dígitos de $x$, portanto, $(y,x) \in \sim_n$ por def. $\sim_n$ caso 2.

Como em todos os casos da definição $(y,x) \in \sim_n$, logo, a relação é simétrica.

### $\sim_n$ é Transitiva:
Tome $x, y, z \in 2^*$ arbitrários. Suponha $(x,y) \in \sim_n$ e $(y,z) \in \sim_n$. Pela definição de $\sim_n$, há 2 casos para cada par:

1.  **$(x,y)$ no caso 1 e $(y,z)$ no caso 1:** Como $len(x) < n$ e $len(z) < n$, então $(x,z) \in \sim_n$. Por def. $\sim_n$ caso 1.
2.  **$(x,y)$ no caso 1 e $(y,z)$ no caso 2:** É impossível pois exigiria que $len(y) < n$ e $len(y) \ge n$ ao mesmo tempo.
3.  **$(x,y)$ no caso 2 e $(y,z)$ no caso 1:** É impossível pois exigiria que $len(y) < n$ e $len(y) \ge n$ ao mesmo tempo.
4.  **$(x,y)$ no caso 2 e $(y,z)$ no caso 2:** Como os primeiros $n$ dígitos de $x$ são iguais aos de $y$ e os primeiros $n$ dígitos de $y$ são iguais aos de $z$, por transitividade da igualdade, os primeiros $n$ dígitos de $x$ são iguais aos de $z$. Como também $len(x) \ge n$ e $len(z) \ge n$, então $(x,z) \in \sim_n$. Por def. $\sim_n$ caso 2.

### $\sim_n$ é Reflexiva:
Tome $x \in 2^*$ arbitrário. 

* Para o **Caso 1**, suponha que $len(x) < n$. Nesse caso, $(x,x) \in \sim_n$, pela definição de $\sim_n$ caso 1, pois ambos os elementos têm comprimento menor que $n$.
* Para o **Caso 2**, suponha que $len(x) \ge n$. Nesse caso, $(x,x) \in \sim_n$, pela definição de $\sim_n$ caso 2, pois ambos os elementos têm comprimento maior ou igual a $n$ e seus primeiros $n$ dígitos são iguais.

Como $\sim_n$ provou-se reflexiva, simétrica e transitiva, ela é uma relação de equivalência. $\blacksquare$

## 5.B)

Por def. classe de equivalência, temos que $[1]_{\sim_n} = \{y \in 2^* \mid y \sim_n 1\}$. A descrição depende do valor de $n$:

* **Se $n > 1$:** Como $len(1) = 1$, temos que $len(1) < n$. Portanto, a string $1$ cai no **Caso 1**. A classe $[1]_{\sim_n}$ conterá todas as strings $y$ tais que $len(y) < n$.
* **Se $n = 1$:** Como $len(1) = 1$, temos que $len(1) \ge 1$. Portanto, a string $1$ cai no **Caso 2**. A classe $[1]_{\sim_1}$ conterá todas as strings $y$ que possuem tamanho maior ou igual a 1 e cujo primeiro dígito é igual a 1.

Portanto, para $n=1$:
$$[1]_{\sim_1} = \{y \in 2^* \mid len(y) \ge 1 \text{ e primeiro dígito de } y \text{ é "1"}\}$$

## 5.C)

Aqui $n=3$ e $len(1)=1$. Portanto, o elemento 1 se relaciona apenas com strings do **Caso 1** da definição de $\sim_n$, pois $len(1) < 3$.

Ou seja, $[1]_{\sim_3} = \{x \in 2^* \mid len(x) < 3\}$. Listando os elementos por comprimento:
* Comprimento 0: $\lambda$ (string vazia)
* Comprimento 1: $0, 1$
* Comprimento 2: $00, 01, 11, 10$

O conjunto final é $\{\lambda, 0, 1, 00, 01, 11, 10\}$. Ela possui **7 elementos**.

## 5.D)

Como $n \in \mathbb{Z}^+$ é arbitrário, a quantidade de elementos depende da categoria de $n$:

### Caso $n > 1$:
Neste cenário, $len(1) < n$. Assim, a string 1 relaciona-se apenas com strings do **Caso 1** da definição.
Ou seja, $[1]_{\sim_n} = \{x \in 2^* \mid len(x) < n\}$.

Para calcular o total de elementos, contamos as strings binárias para cada tamanho $k$ menor que $n$. Como o alfabeto binário possui 2 opções (0 ou 1), pelo Princípio Fundamental da Contagem, para uma string de tamanho $k$ existem $2^k$ combinações possíveis.
A quantidade total de elementos é a soma de todas essas possibilidades, de $0$ (string vazia $\lambda$) até $n-1$:
$$2^0 + 2^1 + 2^2 + \dots + 2^{n-1}$$

Esta expressão é uma Progressão Geométrica (P.G.) finita, onde $a_1 = 2^0 = 1$, a razão $q = 2$ e o número de termos é $n$. Aplicando a fórmula da soma da P.G. ($S = a_1 \frac{q^n - 1}{q - 1}$):
$$1 \cdot \frac{2^n - 1}{2 - 1} = 2^n - 1$$
Nesse caso, a classe possui **$2^n - 1$ elementos**.

### Caso $n = 1$:
Neste cenário, $len(1) = 1$. Logo, a string 1 relaciona-se através do **Caso 2** da definição, pois $len(1) \ge 1$.
Pela definição de $\sim_n$ caso 2, uma string $y$ pertence a essa classe se tiver tamanho $len(y) \ge 1$ e seu primeiro dígito for igual a '1'.

Como o conjunto $2^*$ contém strings de comprimento finito sem um limite máximo estabelecido para o tamanho da string, existem infinitas combinações possíveis para os dígitos que sucedem o primeiro (ex: $1, 10, 11, 100, 101, \dots$).
Nesse caso, a classe possui **infinitos elementos**.

# Questão 07: 

#### Considere $R, S, T$ relações quaisquer. Prove que $R \circ (S \cup T) = R \circ S \cup R \circ T$.

> $(x, z) \in R \circ Q \iff \exists y \text{ tq. } (x, y) \in Q \text{ e } (y, z) \in R$.

---

### $(\subset) \quad R \circ (S \cup T) \subset R \circ S \cup R \circ T$

Tome $(x, z) \in R \circ (S \cup T)$:

$$\begin{aligned} &\exists y \text{ tq. } (x, y) \in S \cup T \text{ e } (y, z) \in R \quad (\text{def. composição}) \\ &\exists y \text{ tq. } [(x, y) \in S \text{ ou } (x, y) \in T] \text{ e } (y, z) \in R \quad (\text{def. de união}) \end{aligned}$$

- **Caso $(x, y) \in S$ e $(y, z) \in R$**: $(x, z) \in R \circ S \subseteq R \circ S \cup R \circ T$.
- **Caso $(x, y) \in T$ e $(y, z) \in R$**: $(x, z) \in R \circ T \subseteq R \circ S \cup R \circ T$.

Ou seja, em ambos os casos: $(x, z) \in R \circ S \cup R \circ T$.

---

### $(\supset) \quad R \circ S \cup R \circ T \subset R \circ (S \cup T)$

Tome $(x, z) \in R \circ S \cup R \circ T$ qualquer:

- **Caso $(x, z) \in R \circ S$**: (def. composição)
    
    $\exists y \text{ tq. } (x, y) \in S \text{ e } (y, z) \in R$.
    
    Como $S \subseteq S \cup T$, temos que $(x, y) \in S \cup T$,
    
    e assim $(x, z) \in R \circ (S \cup T)$.
    
- **Caso $(x, z) \in R \circ T$**: (def. composição)
    
    $\exists y \text{ tq. } (x, y) \in T \text{ e } (y, z) \in R$.
    
    Como $T \subseteq S \cup T$, temos que $(x, y) \in S \cup T$,
    
    logo, $(x, z) \in R \circ (S \cup T)$.
    

---

**Portanto, $R \circ (S \cup T) = R \circ S \cup R \circ T$.** //
