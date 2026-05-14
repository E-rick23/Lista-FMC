## Questão 3

**A)** $f(A\cap B) \subseteq f(A) \cap F(B)$

Se um conjunto está contido em outro, qualquer elemento que pertence ao primeiro também pertence ao segundo.

Seja $y$ um elemento pertencente a imagem da interseção, ou seja $y \in F(A \cap B)$. Pela definição de imagem de um conjunto, existe pelo menos um elemento $x \in (A \cap B)$ tal que $f(x) = y.$

Ora como $x \in A \cap B$ isso significa que $x \in A$ e $x \in B$ Se $x \in B$, então a sua imagem $f(x)$ pertence à imagem de $B$, ou seja, $f(x) \in f(B).$ 

Como $y = f(x)$, temos que $y \in f(A)$ e $y \in f(B)$, o que significa que $y \in f(A)$ e $y \in f(B)$, o que significa que $y \in f(A) \cap f(B).$

**Então, já que o $y$ é genérico, concluímos que todo elemento de $f(A \cap B)$ também está em $f (A) \cap f(B)$ logo $f(A \cap B) \subseteq f(A) \cap f(B)$**

**B)** $f(A) \cap f(B) \subseteq f(A \cap B)$

Considere os conjuntos $X = {1,2}$ e $Y = {3}$.
E a função $f : X -> Y$ tal que $f(1) = 3$ e $f(2) = 3$
E escolha os subconjuntos $A = {1}$ e $B = {2}$.

Calculando os 2 lados da expressão:
 
A interseção $A \cap B =  Ø$. Logo, a imagem da interseção é vazia: $f(A \cap B) = f(Ø) = Ø$. 

Já a imagem de $A$ é $f(A) = {3}$ e a imagem de $B$ é $f(B) = {3}$. A interseção dessas imagens é $f(A) \cap f(B) = {3} \cap {3} = {3}.$

Comparando os resultados vemos que ${3}$ não é subconjunto do $Ø$, **portanto a afirmação é falsa.**

**C)** $f(A - B) = f(A) - f(B).$

Considere os conjuntos $X - {1,2}$ e $Y = {3}$.
E a função $f : X -> Y$ tal que $f(1) = 3$ e $f(2) = 3$.
E escolha os subconjuntos $A = {1,2}$ e $B = {2}.$

Calculando os dois lados da igualdade:

A diferença de conjuntos é $A - B = {1}$. E a imagem dessa diferença é $f(A - B) = f({1}) = {3}.$

Por outro lado, $f(A) = f({1}) = {3}$ e $f(B) = f({2}) = {3}$. A diferença das imagens é $f(A) - f(B) = {3} - {3} = Ø$

**Como ${3} \neq Ø$ a igualdade é falsa.**

**D)** $f^{-1} (C \cap D) = f^{-1} (C) \cap f^{-1} (D)$  

Definição de imagem inversa de um conjunto:

S é $f^{-1} (S) = {x \in X | f(x) \in S}.$

Seja $x \in f^{-1} (C \cap D).$

Por definição: $f(x) \in C \cap D$.

Logo, $f(x) \in C$ e $f(x) \in D$.

Se $f(x) \in C$, então por definição $x \in f^{-1} (C)$

Se $f(x) \in D$, então por definição $x \in f^{-1} (D)$

**Portanto $x \in f^{-1}(C)$ e $x \in f^{-1}(D)$ o que implica que $x \in f^{-1}(C) \cap x \in f^{-1}(D)$.**

Agora, seja $x \in f^{-1}(C) \cap x \in f^{-1}(D)$, isso significa que $x \in f^{-1}(C)$ e $x \in f^{-1}(D)$, então pela definição $f(x) \in C$ e $f(x) \in D$.

Logo, $f(x)$ pertence a interseção, ou seja $f(x) \in C \cap D$.

**Se a imagem de $x$ está em $C \cap D$ então, por definição o elemento original está na pré-imagem desse conjunto: $x \in f (C \cap D)$.**

**Como ambas as inclusões foram satisfeitas, a igualdade está provada.**

---
## Questão 4

**a)** Imagens dos conjuntos $[0, 1], [0, 1), (0, 1]$ e $(0, 1)$

A imagem de um conjunto sob uma função é o conjunto de todos os resultados possíveis que a função retorna ao aplicarmos todos os valores daquele intervalo.

​Para o conjunto $[0, 1]$: (inclui o 0 e o 1)
​Para todo $x$ tal que $0 < x < 1$, o valor de $floor(x)$ é 0.
​Para $x = 1$, o valor de $floor(x)$ é 1.
​Imagem: ${0, 1}$

​Para o conjunto $[0, 1)$: (inclui o 0, mas não o 1)
​Para todo $x$ tal que $0 < x < 1$, o valor de $floor(x)$ é 0.
​Imagem: ${0}$

​Para o conjunto $(0, 1]$: (não inclui o 0, mas inclui o 1)
​Para todo $x$ tal que $0 < x < 1$, o valor de $floor(x)$ é 0.
​Para $x = 1$, o valor de $floor(x)$ é 1.
​Imagem: ${0, 1}$

​Para o conjunto $(0, 1)$: (não inclui o 0 nem o 1)
​**Para todo $x$ tal que $0 < x < 1$, o valor de $floor(x)$ é 0.**
**​Imagem: ${0}$**

**b)** A função floor é injetiva? Prove ou dê contra-exemplo.

Definição de injetiva: ​Uma função é injetiva (ou um-para-um) se elementos diferentes do domínio sempre mapeiam para elementos diferentes no contradomínio.

Considere $x_1 = 0.5$ e $x_2 = 0.8.$
Ambos pertencem ao domínio dos reais. ($\mathbb{R}$)
$floor(0.5) = 0$    e     $floor(0.8) = 0$
Como $x_1 \neq x_2$     mas $floor(x )$ = $floor(x )$, **a função não é injetiva, pois dois números reais resultam no mesmo número inteiro.**

**c)** A função floor é sobrejetiva? Prove ou dê contra-exemplo.

Definição de sobrejetiva: Se a imagem de uma função é igual ao seu contradomínio, a função é sobrejetiva.

O problema define a função como floor: $\mathbb{R} \rightarrow \mathbb{Z}$ 

então o contradomínio é o conjunto dos inteiros, logo, para que a função seja sobrejetiva, é necessário provar que para qualquer inteiro $y$ no contradomínio, existe pelo menos um real $x$ no domínio tal que $floor(x) = y.$

Prova:
Seja $y \in \mathbb{Z}$, um inteiro qualquer.
Como o conjunto dos números inteiros está contido no conjunto dos números reais $\mathbb{Z} \subset \mathbb{R}$ , podemos escolher $x = y.$
Pela definição da função floor, se $x$ já é um número inteiro, o maior inteiro menor ou igual a $x$ é o próprio $x$.

Portanto:

$floor(x) = |y| = y$

Como foi demonstrado que para todo $y \in \mathbb{Z}$ existe um $x \in \mathbb{R}$ correspondente (basta que x seja o próprio y), **a função cobre todo o contradomínio e, logo, é sobrejetiva.**

---
## Questão 14

Sejam $A$ e $B$ conjuntos infinitos enumeráveis. Então existem bijeções

$$f:\mathbb{N}\to A \qquad \text{e} \qquad g:\mathbb{N}\to B.$$

Assim, podemos escrever

$$A=\{a_1,a_2,a_3,\ldots\}$$

e

$$B=\{b_1,b_2,b_3,\ldots\}.$$

Logo,

$$A\times B=\{(a_i,b_j)\; ;\; i,j\in\mathbb{N}\}.$$

Para mostrar que $A\times B$ é enumerável, basta mostrar que $\mathbb{N}\times\mathbb{N}$ é enumerável.

Considere os pares $(i,j)\in\mathbb{N}\times\mathbb{N}$. Organizamos esses pares em diagonais definidas por

$$D_n=\{(i,j)\in\mathbb{N}\times\mathbb{N} : i+j=n\}.$$

Cada diagonal possui quantidade finita de elementos. Por exemplo,

$$D_2=\{(1,1)\},$$

$$D_3=\{(1,2),(2,1)\},$$

$$D_4=\{(1,3),(2,2),(3,1)\},$$

e assim sucessivamente.

Enumerando os elementos diagonal por diagonal, obtemos a sequência

$$(1,1),(1,2),(2,1),(1,3),(2,2),(3,1),\ldots$$

Todo par $(i,j)$ pertence exatamente à diagonal $D_{i+j}$. Logo, todo elemento de $\mathbb{N}\times\mathbb{N}$ aparece em alguma posição dessa enumeração.

Portanto, existe uma bijeção entre $\mathbb{N}$ e $\mathbb{N}\times\mathbb{N}$, isto é, $\mathbb{N}\times\mathbb{N}$ é enumerável.

Como $A\times B$ está em bijeção com $\mathbb{N}\times\mathbb{N}$ pela aplicação

$$(i,j)\mapsto (a_i,b_j),$$

segue que $A\times B$ é infinito enumerável.

---

## Questão 15

Seja $A$ finito e $B$ infinito enumerável, com $A\cap B=\varnothing$.

Como $A$ é finito, existe $k\in\mathbb{N}$ tal que

$$A=\{a_1,a_2,\ldots,a_k\}.$$

Como $B$ é infinito enumerável,

$$B=\{b_1,b_2,b_3,\ldots\}.$$

Definimos a função

$$h:\mathbb{N}\to A\cup B$$

por

$$h(n)= \begin{cases} a_n, & \text{se } 1\leq n\leq k,\\ b_{n-k}, & \text{se } n>k. \end{cases}$$

Como $A\cap B=\varnothing$, nenhum elemento de $A$ coincide com um elemento de $B$.

Além disso,

- os elementos $a_1,\ldots,a_k$ são distintos entre si;
    
- os elementos $b_1,b_2,\ldots$ são distintos entre si.
    

Logo, números naturais diferentes possuem imagens diferentes por $h$. Portanto, $h$ é injetiva.

Agora, seja $x\in A\cup B$.

- Se $x\in A$, então existe $i\in\{1,\ldots,k\}$ tal que $x=a_i=h(i)$.
    
- Se $x\in B$, então existe $j\in\mathbb{N}$ tal que $x=b_j=h(k+j)$.
    

Assim, todo elemento de $A\cup B$ pertence à imagem de $h$. Logo, $h$ é sobrejetiva.

Concluímos que $h$ é bijetiva. Portanto, $A\cup B$ é infinito enumerável.

---

## Questão 16

Sejam $A$ e $B$ conjuntos infinitos enumeráveis. Então podemos escrever

$$A=\{a_1,a_2,a_3,\ldots\}$$

e

$$B=\{b_1,b_2,b_3,\ldots\}.$$

Considere a sequência obtida intercalando os elementos de $A$ e $B$:

$$a_1,b_1,a_2,b_2,a_3,b_3,\ldots$$

Essa sequência contém todos os elementos de $A\cup B$, embora alguns possam aparecer mais de uma vez quando $A\cap B\neq\varnothing$.

Construímos então uma nova sequência eliminando cada repetição após sua primeira aparição. Denotemos essa sequência por

$$c_1,c_2,c_3,\ldots$$

Nessa nova sequência,

- todo elemento de $A\cup B$ aparece pelo menos uma vez;
    
- nenhum elemento aparece mais de uma vez.
    

Definimos então a função

$$f:\mathbb{N}\to A\cup B$$

por

$$f(n)=c_n.$$

A função $f$ é injetiva, pois os termos da sequência $c_1,c_2,c_3,\ldots$ são todos distintos.

Além disso, $f$ é sobrejetiva, pois todo elemento de $A\cup B$ aparece em algum termo da sequência.

Logo, $f$ é bijetiva.

Portanto, $A\cup B$ é infinito enumerável.

---
## Questão 20
### Dicionário:

$<>$ - Representa a lista vazia
$<x>$ representa uma lista contendo um único elemento $x$.
A operação $x ⚬ L$ representa a concatenação de um elemento x no início de uma lista $L$. Por exemplo, $a  ⚬ <b,c>$ = $<a,b,c>$.

a) A função last retorna o último elemento de uma lista não-vazia
Caso base: Se a lista possui apenas um elemento, esse elemento é o último.
$last(<x>) = x$
Passo recursivo: Se a lista possui mais de um elemento (uma cabeça x e uma cauda L que não é vazia) o último elemento da lista inteira é igual  ao último elemento da cauda.
$last(x ⚬ L) = last(L),$ para $L \neq <>$ 

b) A a função front retorna a lista original sem o seu último elemento.

Caso base: Se a lista possui apenas um elemento, remover o último elemento resulta em uma lista vazia.

$front(<x>) = <>$

Passo recursivo: Se a lista possui mais de um elemento (cabeça x e cauda não-vazia L), a função deve manter o primeiro elemento x e reconstruir o resto da lista aplicando a função front na cauda L.

$front(x ⚬ L) = x ⚬ front(L),$ para $L \neq <>$

- Exemplo de execução para $front(<a,b,c>)$:

$front(a ⚬ <b,c>) = a ⚬ front(<b,c>)$
Resolvendo o interior:
$front(b ⚬ <c>) = b ⚬ front(<c>)$
O interior atingiu o caso base:
$front(<c>) = <>$
Substituindo de volta:
$b ⚬ <> = <b>$
Substituindo de volta novamente:
$a ⚬ <b> = <a,b>$

