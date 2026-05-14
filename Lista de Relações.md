
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