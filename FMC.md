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

## Questão 20

20.
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

