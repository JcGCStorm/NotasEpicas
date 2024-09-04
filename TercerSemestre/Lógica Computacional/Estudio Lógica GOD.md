# Introducción 
### ¿Qué hace la lógica? ¿Para que sirve?
1. Construye argumentos.
2. Para ver que las cosas tengan sentido.
3. Para ver como funcionan las cosas.
4. Para ver si algo es verdadero o falso.
5. Para abstraer cosas del mundo real.
> [! Abstract] Consistencia
> Un sistema lógico es consistente si nunca es posible probar su formula y también su negación

> [! Abstract] Independiente.
> Los axiomas de un sistema lógico son independientes si no podemos "probar" un axiomas usando el resto de axiomas. 

> [! Abstract] Correctitud
> Las reglas del sistema no pueden obtener una inferencia falsa a partir de verdaderas.

> [! Abstract] Completitud.
> Toda sentencia verdadera es demostrable. Es decir, siempre que algo sea verdadero lo vamos a poder demostrar.


### Principio de Inducción Natural.
Sea $A$ un conjunto
1. $0 \in A$
2. $n \in A$, $\forall n \in A$, entonces $n+1 \in A$ 
Si $B = (x \in N| \text{x cumple una propiedad } P)$ entonces B = N
### Principio de Inducción Estructural.
Todo conjunto definido recursiva mente tiene un principio de inducción llamado _Inducción estructural._ 

> [! Abstract] ¿Cómo hacer un conjunto recursivo
> 1. Conjunto de elementos base
> 2. Conjunto de reglas donde se definen (al menos un) elemento nuevo en terminos anteriores.
> 3. Cláusula que afirma que los dos puntos anteriores son la única forma de generar elementos del conjunto.

> [! Note] Ejemplo
> Listas de elementos de A
> 1. [] es una lista de elementos de A
> 2. Si $a \in A$ y xs una lista de elementos de A, entonces [a:xs] es una lista de A.
> 3. Son todas.
¡

> [! Abstract] ¿Cómo mostramos/ hacemos inducción estructural?  
> Si P es una propiedad, debemos mostrar para todos los elementos de un conjunto A definido recursivamente, lo siguiente:
> 1. P se cumple para todos los elementos base.
> 2. Si x es un elemento de A construido a partir de $x_1, x_2, ... , x_n$, suponer que P se cumple para x.
> 3. Son todas.

# Proposiciones.
## #Definiciones 
Una _proposición_ es un enunciado al cual podemos calificarlo como verdadero o falso.
> [! Danger]- #Definición  Proposición.
> Una _proposición_ es un enunciado al cual podemos calificarlo como verdadero o falso. Por ejemplo:
> - Estudiamos en la facultad de Ciencias
> - Somos estudiantes de CC
> - Me gustan los tamales de mole

> [! Danger]- #Definición Alfabeto.
> Un ALFABETO es un conjunto finito y no vacío de elementos llamados caracteres. Por ejemplo:
> - $\epsilon_1 =$ {a, e i, o u}
>- $\epsilon =$ {0,1,2,...,9}

> [! Danger]- #Definición Cadena.
> Una cadena sobre $\epsilon$ es una sucesión finita de caracteres sobre $\epsilon$ Por ejemplo:
> - aeiou es una cadena en $\epsilon_1$
> - AeuA _NO_ es cadena sobre $\epsilon_1$ ya que "A" no está en $\epsilon_1$

> [! Abstract]- #MiniDefinicion. $\epsilon^*$
> Al conjunto de todas las posibles cadenas sobre un Alfabeto $\epsilon$ la denominamos por $\epsilon^*$. Por ejemplo:
> - si tenemos el Alfabeto $\epsilon _2 =$ {1,2,3,4,5,6,7,8,9} los naturales $N \in \epsilon_2^*$ pero $\epsilon_2^* \notin N$

>[! Danger]- #Definición  Lenguaje.
>Un Lenguaje sobre un alfabeto es un subconjunto de cadenas $\epsilon^*$ 

> [! Danger]- #Definición . Estado
> Un estado o asignación de las variables proposicionales es un función $I_v : Var P \implies Bool$

> [! Abstract]- Observación.
> Si tenemos n variables proposicionales entonces existen $2^n$ estados de esas variables.

> [! Danger]- Interpretación de una formula.
> Dado un estado de las variables $I:VarP \implies Bool$ definimos una interpretación de las formulas con respecto a $I$ como la función $I^\Omega$. Que va de $PROP \implies Bool$ tal que:
> - $I^\Omega (p) = I(p)$ si $p \in$ Var P
> - $I^\Omega (\bot) = 0$
> - $I^\Omega (\top) = 1$
> - $I^\Omega (¬A) = 0$ si y solo si $I^\Omega (A) = 1$
> - $I^\Omega (A \lor B) = 0$ si y solo si $I^\Omega (A) = 0$ y $I^\Omega (B) = 0$
> - $I^\Omega (A \land B) = 1$ si y solo si $I^\Omega (A) = 1$ y $I^\Omega (B) = 1$
> - $I^\Omega (A \implies B) = 0$ si y solo si $I^\Omega (A) = 1$ y $I^\Omega (B) = 0$
> - $I^\Omega (A \iff B) = 1$ si y solo si $I^\Omega (A) = I^\Omega (B) = 1$

> [! Danger]- #Definición  Sustitución textual.
> En una formula dada $A$, una variable Proposicional cambia por una formula $B$. Así se genera una nueva formula denotada por $A[p:=B]$, obtenida al sustiruir todas las presencias de $p$ en $A$ por $B$.
> 1. Si $p$ no figura en $A$ entonces $A[p := B$ = A
> 2. Si $p ≠ q$ y $p$ no figura en $C$ entonces $A[p:= B][q:= C] = A[q:= C][p:=B[q:=C]]$

> [! Danger]- #Definición Estado modificado o actualizado.
> Sean $\gamma :Var \implies Bool$ un estado de las variables, $p$ una variable proposicional y $v\in Bool$. Definimos la actualización de $\gamma$ en $p$ por $v$, denotado $\gamma [p/v]$ como sigue:
> $$
> \gamma[p/v](q) = 
> \begin{cases}
>  v & \text{si q = v}, \\
>  \gamma(q) \text{si q ≠ v}.
>  \end{cases}
> $$

Con $\gamma[p]$ una interpretación. Se supone que $\gamma$ debería de ser una $I$ como garigoleada, pero no sé ponerla, por eso lo sustituí por $\gamma$

> [! Abstract]- #Lema  - (Sustitución).
> Sea \gamma una iterpretación, p una Var prop y B una formula tal que $\gamma ^* (B) =v$. Entonces \gamma (A[p:=B]) = \gamma [p/v](A)
> Si tu formula A tenia u valor y tu la sustituyes por otra cosa, su interpretación debe ser igual.

>  [! Abstract]- #Lema De Incidencia.
> Sea $\alpha \in PROP$ y _I_$_1$, _I_$_2$ Var P $\rightarrow$ Bool dos estados. Si para todo $p \in vars (\alpha)$ ocurre que _I_$_1$ (p) = I$_2$ (p) entonces I$_1$ ($\alpha$) = I$_1$ ($\alpha$)
> Para evaluar una formula $\alpha$ nos basta saber únicamente el valor de las variables prop de $\alpha$

> [! Danger]- #Definición Sea $\alpha \in PROP$ entonces:
> 1. Si para toda interpretación I sucede que I($\alpha$) = 1 llamamos a $\alpha$ *tautología o válida* y escribimos $\models \alpha$
> 2. Si para toda interpretación I sucede que I($\alpha$) = 0 llamamos a $\alpha$ contradicción o insatisfacible y escribimos $\nvDash \alpha$
> 3. Si existe una iterpretación I tal que I($\alpha$) = 1, decimos que $\alpha$ es satisfacible y que I es modelo de $\alpha$. Escribimos I $\models \alpha$
> 4. Si no existe una interpretación I tal que I($\alpha$) = 1, decimos que $\alpha$ es insatisfacible en I y que I no es modelo de $\alpha$. 

> [! Danger]- #Proposición Satisfacibilidad de la contradicción y la tautología.
> Sea $\Gamma$ un conj de formulas $A \in \Gamma$, $\delta$ una tautología y C una contradicción. 
> 1. Si $\Gamma$ es satisfacible ent. 
> 	1. $\Gamma$ \\ \{A\} es satisfacible.
> 	2. $\Gamma \cup$ \{$\delta$\} es satisfacible.
> 	3. $\Gamma \cup$ \{C\} es insatisfacible.
> 2. Si $\Gamma$ es insatisfacible
> 	1. $\Gamma \cup$ \{B\} es insatisfacible.
> 	2. $\Gamma$ \\ \{$\delta$\} es insatisfacible.

> [! Danger]- #Proposición Satisfacibilidad e insatisfacibilidad.
> Sea $\Gamma$ = \{$A_1, ..., A_k$\} un conjunto de formulas.
> A) $\Gamma$ es satisfacible syss $A_1 \land A_2 \land ... \land A_k$ = 1
> B) $\Gamma$ es insatisfacible syss $A_1 \land A_2 \land ... \land A_k$ es contradicción.

> [! Danger]- #Definición  Equivalencia de Formulas.
> Dos formulas A y B son equivalentes si para toda interpretación I. I(A) = I(B). En tal caso escribimos A $\equiv$ B
> Sii Af $\equiv$ es una relación de Equivalencia ocurre:
> 1. $A \equiv A$
> 2. $A \equiv B$ entonces $B \equiv A$
> 3. $A \equiv B$ y $B \equiv C$ entonces $A \equiv C$

> [! Danger]-  #Proposición Equivalencia de Proposiciones.
> Sean $\alpha, \phi \in PROP$, $\alpha \equiv \phi$ syss $\models \alpha \iff \phi$.

> [! Danger]- #Proposición No entiendo bien jajaj
> Si $A \equiv B$ y $p \in Var p$, entonces $C[p = A]\equiv C [p:= B]$
> Ejemplos:
> Supongamos A=($p \land \neg q $) $\implies (s \lor q) \equiv \top$
> B = $\top$
> C = $r \lor t \immplies r \lor s$
> Entoces:
> $C[r:=A] \equiv C[r:= B] \equiv \top \lor t \implies \top \lor s$

> [! Danger]- #Definición  Consecuencia Lógica
> Sean $\Gamma$ un conj de formulas y A $\in PROP$. Diremos que A es consecuencia lógica de $\Gamma$ si para toda interpretación I que satisface $\Gamma$ se tiene que I(A)=1, en tal caso escribimos $\Gamma \models A$ (es decir A es consecuencia lógica de $\Gamma$)
> = Todo modelo de $\Gamma$ es modelo de A
> = Si I interpretació, I($\Gamma \equiv 1$) entonces I(A) = 1

> [! Danger]- #Proposición Propiedades de la relación de consecuencia lógica.
> 1. Si $A \in \Gamma$, ent $\Gamma \models A$
> 2. $\Gamma \models A$ syss $\Gamma \cup$ \{$\neg A$\} es insatisfacible (Principio de inducción.)
> 3. $\Gamma \models A \implies B syss $\Gamma \cup$ \{A\} $\models B$
> 4. ....
> 5. .....
> 6. ....

> [! Danger]- #Definición Sea $\Gamma$ un conj de formulas y $\alpha \in Prop$, $\Gamma \models \alpha$ syss para toda I interpretación tal que I($\Gamma$ = 1 se tiene que I($\alpha$ ) = 1, J($\Gamma$) =1 y J(A)=1




Llave de una Nissan de Ramiro
Llave de Arturo y María


$\gamma, \Gamma, \Delta, \delta, \Omega$   
#### Alfabeto de la Lógica Proposicional.
El Alfabeto de la lógica Proposicional es $\epsilon =$ {$\lor, \land, ¬, \implies, \iff$}$U${(,)}$U${$\top, \bot$} $U${Var $P$} . Con Var P = {$p, q, r, s, ...., p_1,p_2,...., q_1,1_2,....$}. El conjunto de _Formulas Atomicas_ denotado por _ATOM_ es: ATOM= Var P $U$ {$\top, \bot$}, $p,q,r,s,....$
El Lenguaje de la lógica Proposicional denotado por PROP está definido por las siguientes reglas:
1. *Si $A \in ATOM$, entonces $A \in PROP$* 
2. *Si $A \in PROP$, entonces $(¬A) \in PROP$*
3. *Si $A,B \in PROP entonces:$*
	1. $(A \lor B) \in PROP$
	2. $(A \land B) \in PROP$
	3. $(A \implies B) \in PROP$
	4. $(A \iff B) \in PROP$
4. *Son todas. Ninguna otra cadena sobre $\epsilon$ que no haya sido construido con las reglas 1-3 forma parte de PROP.*
A las cadenas de PROP las llamamos formulas bien formadas o simplemente _formulas._

## Precedencia de Operadores.
1. _¬_, afecta a la formula más pequeña a su derecha.
2. $\lor, \land$ afecta a las formulas mas "pequeñas" del lado izquierdo y derecho.
3. $\implies$ afecta a las formulas mas "pequeñas" del lado izquierdo y derecho.
4. $\iff$ afecta a las formulas mas "pequeñas" del lado izquierdo y derecho.
## Principio de Inducción Estructural para PROP.
Sea P una propiedad acerca de formulas del Lenguaje PROP, para probar que toda la formula tiene la tiene la propiedad P basta demostrar lo siguiente:
1. _Caso Base_ Demostrar que si $\phi, \psi \in ATOM$ entonces $\phi$ cumple $P$  
2. _Hipotesis de Inducción._ Supongamos que para $\phi, \psi \in PROP$ se cumple $P.$
3. _Paso inductivo._ Debemos probar que:
	1. $(¬\phi)$ cumple $P$
	2. $(\phi * \psi)$ se cumple $P$ con $* \in \lor, \land, \implies, \iff$
## Semántica y tablas de Verdad.
Prácticamente nos dice si algo es verdadero o falso. Bool= {1,0}, PROP = {0,1}, si por ejemplo $\phi \implies 1$ entonces $\phi$ es verdadero, si implica 0 entonces es falso.
### Tablas de Verdad.

| p   | q   | $p \land q$ | $p \lor q$ | $p \implies q$ | $p \iff q$ |
| --- | --- | ----------- | ---------- | -------------- | ---------- |
| 0   | 0   | 0           | 0          | 1              | 1          |
| 0   | 1   | 0           | 1          | 1              | 0          |
| 1   | 0   | 0           | 1          | 0              | 0          |
| 1   | 1   | 1           | 1          | 1              | 1          |
Cada renglón es un estado de las variables.

#### Equivalencias Lógicas
Algunas equivalencias lógicas. Sean A, B, C $\in Prop$ 
- Conmutatividad
	- $A \lor B \equiv B \lor A$
	- $A \land B \equiv B \land A$
- Asociatividad
	- $A \lor (B \lor C) \equiv (A \lor B) \lor C$

