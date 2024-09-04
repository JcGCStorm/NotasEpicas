## Introducción.
El algebra lineal es geometria en donde las lineas con las que dibujamos tienen dos operaciones algebraicas _(suma y producto)_. Estas lineas junto co sus operaciones cumplen varias propiedades y son los llamados campos o cuerpos y los espacios geométricos que podemos dibujar con estas lineas se llaman espacios vectoriales, pueden ser finitos o infinitos.
### Axiomas de Zermelo-Fraenkel + Axiomas de Elección.

#### #Axioma 1. De existencia o del conjunto vacío.
>[! Danger] Axioma 1. De existencia o del Conjunto Vacío:
>Existe un conjunto que no tiene elementos. Es decir,
>$\exists a, [\forall X, ¬(X \in A)] \equiv \exists A, \forall X(X \notin A)$

>[! Warning]- Lema del conjunto vacío.
>Existe un único conjunto sin elementos. Por ser único lo llamaremos el _Conjunto Vacio_ y lo denotaremos por $\emptyset$

#### #Axioma 2. De extensionalidad.
>[! Danger] Axioma 2. De extensionalidad:
>Sean $X$ y $Y$ conjuntos, $X = Y$ se lee $X$ es igual a $Y$
>$\forall X [\forall Y ([X = Y]) \iff [\forall Z [(Z \in X) \iff (Z \in Y)]])]$
>En cristiano este axioma nos dice que dos conjuntos $X$ y $Y$ son iguales exactamente cuándo tienen los mismos elementos.
#### #Axioma 3. Esquema de Comprensión o de Especificación.
>[! Danger] Axioma 3. Esquema de Comprensión o de Especificación:
>Sea $P(x)$ una proposición en $x$. Entonces para todo conjunto $A$ la colección de los elementos de $A$ que cumplen $P(x)$ (ie., tales que $P(x)$ es verdad) es un conjunto.
>$\forall A [\exists S, (\forall X [(X \in S) \iff ((X \in A) \land P(X))])]$
>Nota: Para A conjunto y para cada proposición en x, $P(x)$, es conjunto $S$ es único, por lo que lo denotaremos como ${x \in A; P(x)}$
#### #Axioma 4.  Del par.
>[! Danger] Axioma 4. Del Par:
>Para cada $X$ y $Y$ conjuntos, existe un conjunto cuyos únicos elementos son $X$ y $Y$
>$\forall X \forall Y, \exists B, \forall Z((Z \in B) \iff ([Z =X] \lor [Z = Y]))$ 
>Este conjunto $B$ es único  lo denotaremos por ${X, Y}$
#### #Axioma 5. De la union.
>[! Danger] Axioma 5. De la unión:
>$\forall S \exists U, \forall X [(X \in U) \iff (\exists A, [(A \in S) \land (X \in A)])]$

>[! Example]- Ejemplo:
>Sea $S= {A_1 = (0,1), A_2 = (0,2), A_3 = (3,4,5)}$. Entonces $\cup S = (0,1,2,3,4,5)$
>

#### #Axioma 6. Del conjunto potencia.
>[! Danger] Axioma 6. Del Conjunto Potencia:
>$\forall X (\exists S, [\forall A((A \in S) \iff (A \subseteq X))])$ 
>Nos dice que para cada conjunto X existe un conjunto $P(x)$ que contiene todos los subconjuntos de X. Es decir si un conjunto Y es un subconjunto de X, entonces Y también es un elemento de $P(X)$. En resumen, para cualquier conjunto podemos construir otro conjunto que contiene todos los posibles subconjuntos del conjunto original.

#Que_Insano

#### #Axioma 7. De regularidad o de Fundación.
> [! Danger] Axioma 7. De regularidad o de Fundación.
> $\forall A [(A ≠ \emptyset) \Rightarrow [\exists u, [(u \in A) \land (\forall x (x \in A) \Rightarrow (x \notin u))]]]$
> Nos está diciendo que todo conjunto no vacio A contiene al menos un elemento x que es disjunto *(no tiene intersección)* de A, es decir un conjunto no puede ser miembro de sí mismo, ningún conjunto puede ser elemento de si mismo directa o indirectamente, asegurandonos que no hay conjuntos infinitamente descendentes. Por lo que yo entiendo, nos están dando un limite inferior que sería el vacío.

> [! Important] Teorema.
> 		a)  $\forall A [(A ≠ \emptyset) \Rightarrow (A \notin A)]$
> 		b) La colección de todos los conjuntos _NO_ forma un conjunto.  

#### #Axioma 8. De infinitud.
> [! Danger] Axioma 8. De infinitud:
> $\exists X, [(\emptyset \in X) \land [\forall Y ((Y \in X) \Rightarrow (Y \cup$ {$Y$} $\in X))]]$ 
> Es decir, existe un conjunto X tal que 
> 		- $\emptyset \in X$ y
> 		- $\emptyset$  $\cup$ {$\emptyset$} =  {$\emptyset$} $\in X$ y
> 		- {$\emptyset$} $\cup$ {{$\emptyset$}} = {$\emptyset$, {$\emptyset$}} $\in X$ y ...
> Se explica solito, podemos hacer conjuntos infinitos con el conjunto vacío, es meter conjuntos sobre conjuntos sobre conjuntos sobre....

#Que_Insano 
#### #Axioma 9. De reemplazo.
Sean X un conjunto y tenemos para $i \in X$ un conjunto $A_i$. Entonces, la colección {$A_i; i\in X$} (ó {$A_i$}$_{i \in X}$) es un conjunto.
		_Equivalentemente:_ 
Sean X un conjunto y $\alpha$ una colección de conjuntos tales que cumplen lo siguiente
	1. A cada $A \in \alpha$ le podemos asociar una única $i_A \in X$, y 
	2. Si $A, B \in \alpha$ son tales que $i_A = i_B$ entonces $A=B$.
	Entonces $\alpha$ es un conjunto.

#### #Axioma de Elección.
> [! Danger] Axioma de Elección.
> $\forall X [(\emptyset \notin X) \Rightarrow [\exists f: X -> \cup X \text{  función  }, [\forall A [(A \in X) \Rightarrow (f(A) \in A)]]]]$.
> 	En otras palabras: Dado un conjunto cuyos elementos son conjuntos no vacíos podemos escoger un elemento de cada conjunto.
> IBelieveInAxiomaDeElección

___
> [! Success] #Corolario: 
> Los naturales forman un conjunto por axioma de infinitud.
> $N \cup$ {$\emptyset$} es un conjunto.
> Los enteros forman un conjunto.

___
### Interpretación geometrica de la raíz cuadrada de reales.
$\sqrt{a}, a \in R$ con $\alpha > 0$
 ![[Interpretación Geometrica.png]] 
 Parte $1$ y Parte $2$ 
 ![[Interpretación_Geometrica.excalidraw.png]]

___


### Métodos de demostración de la lógica proposicional.
Prácticamente tablas de verdad xD
Si tenemos dos proposiciones, p y q para demostrar un p -> q basta con demostrar que p es verdadera ya que de ser verdadera entonces q debe de ser verdadera también, para más información por favor acudir a [[Metodos-de-demostracion-2024-2.pdf]]
___
## Campos:
Sea k un conjunto con dos operaciones, que son funciones:
  Suma: +:   
			 - _kxk -> k_ 
			 - ($\alpha, \beta$) |-> +($\alpha, \beta$) =: $\alpha + \beta$
  Producto:   ·: kxk ->  k
			 -($\alpha, \beta$) |-> $(\alpha, \beta) =: \alpha · \beta$


> [! Abstract]- #Definición de Campo.
> Diremos que (k, +, ·) es un _campo_ si satisface lo siguiente:
> $+_.$ 1. Conmutatividad
> $+_.$ 2. Asociatividad
> $+_.$ 3. Neutro Aditivo
> $+_.$ 4. Inverso Aditivo
> 
> $·_.$ 0. Cerradura. a, b \in T -->  a * b $\in T$
> $·_.$ 1. Conmutatividad
> $·_.$ 2. Asociatividad  
> $·_.$ 3. Neutro multiplicativo
> $·_.$ 4. Inverso múltiplicativo


>[! Question] Lema:
>Sea (k, +, ·) un campo. Entonces el neutro aditivo y el neutro múltiplicativo son únicos 

>[! Question] Lema:
>Sea (k, +, ·) un campo. Entonces el neutro aditivo y el neutro múltiplicativo son únicos 
>
>

>[! Question]- #Lema de la unicidad de los neutros:
>Sea (k, +, ·) un campo. Entonces el neutro aditivo y el neutro múltiplicativo son únicos 

>[! Question]- Leyes de la cancelación.
> #Ley de la cancelación de la suma:
>- $\forall \alpha, \beta, \gamma \in k, [\alpha + \beta = \alpha + \gamma] \Rightarrow [\beta = \gamma]$
>Ley de la cancelación del Producto:
>- $\forall \beta, \gamma \in k, \forall \alpha \in k -$ {$0$}, $[\alpha \beta = \alpha \gamma] \Rightarrow [\beta = \gamma]$

> [! Question]- Elemento idéntico (neutro) e inversos.
> 
> Si el elemento idéntico derecho no existe, entonces el izquierdo tampoco
> Para saber si el idéntico derecho existe simplemente recordamos esto:
> Supongamos que tenemos una propiedad "?" Que es igual a a ? B = a +3b +1 es decir el elemento 1 màs 3 veces el elemento 2 mas 1
 > - a ? e = a por def del elemento identico   
 > - a ? e = a + 3e +1
 > - a = a +3e + 1
 > Aquí no existe el idéntico derecho, por lo que no existe el izquierdo, pero vamos a hacerlo igual
 > - e ? A = a 
 > - e ? A = e + 3a +1
 > -por transitividad
 > - a =e +3a+1
 > Si no existe el idéntico, no existe el inverso

### Grupos, campos y no-campos
#### Sistema algebraico.
Cuando un conjunto está provisto de una o varias operaciones binarias se tiene un sistema algebraico, por ejemplo $R,N,Q$
#### Grupos
Grupos - Grupo abeliano - Anillo - anillo conmutativo-  anillo on unidad - Dominio entero - Campo
1. Cerradura
2. Asociatividad
3. Existencia del neutro
4. Existencia de inveros
#### Campos
Sea k un conjunto no vacío con al menos dos elementos y las operaciones binarias 
Los que tienen
- $Q$ los racionales
- $R$ los reales
- $Z$ Los enteros modulo 2
#### No campos
- ({0}, 0+0 =0, 0·0=0), cumple todos los axiomas excepto que el neutro aditivo y el neutro múltiplicativo son el mismo
- $N$  los números naturales no tienen inversos multiplicativos ni inversos aditivos.
- $Z$ Los enteros no tienen inversos multiplicativos

___
### Espacios Vectoriales.
#### Sub-espacios vectoriales
Sea V, W espacios vectoriales 
## Los Enteros Modulo n
##### El #algoritmo de la Division.
Sean $n, m \in Z$ números enteros con n ≠ 0. Entonces existen únicos $d, r \in Z$ con 0 ≤ r < |n| tales $m = nd + r$.
Prácticamente lo que hacíamos con Arilin
28/5
28 = 5 * 5 +3
O tambien 28 mod 5 = 3
#### El máximo común divisor.
###### Valor Absoluto:
$$
|n|= \begin{cases} 
n, & \text{si n ≥ 0} \\
-n, & \text{si n < 0}
\end{cases}
$$

> [! Danger]- #Proposición. 
> Sea n ≥ 1 un numero natural. Al siguiente conjunto se le llama el conjunto de los enteros módulo n y son los residuos al dividir entre n:
> $$
> Z_n := (\vec 0, \vec 1, ..., \vec{n-1})
> $$
> Y tiene dos funciones bien definidas:
> Suma. +: $Z_n x Z_n \Rightarrow Z_n$
> 	- $(\vec a, \vec b) |-> \vec {a+b}$
> Producto. ·: $Z_n x Z_n \Rightarrow Z_n$  
> 	- $(\vec a, \vec b) |-> \vec {ab}$
> donde la suma cumple conmutatividad, asociatividad, tiene un neutro aditivo y el producto cumple conmutatividad, asociatividad, tiene neutro multiplicativo, cumplen la distributividad y el neutro aditivo es distinto del neutro multiplicativo. PERO hay casos en dónde no se cumple el axioma (regla) del inverso multiplicativo.

___
## Espacios Vectoriales.
Sea V un conjunto no vacío y sea (K, +, * ) un campo. Se dice que V es un espacio vectorial sobre K si están definidas dos leyes de composición, la adicio y la multiplicación por escalar tales que:
> [! Abstract] #Definición de Espacio Vectorial.
> Diremos que V es un _k-espacio vectorial_ si satisface lo siguiente:
> $·+.$ 0. Cerradura. $\forall \vec u, \vec v \in V : \vec u + \vec v \in V$
> $+_.$ 1. Conmutatividad. $\forall \vec u, \vec v \in V : \vec u + \vec v = \vec v + \vec u$
> $+_.$ 2. Asociatividad. $\forall \vec u, \vec v, \vec w \in V: \vec u + (\vec v + \vec w) = (\vec u + \vec v) + \vec w$
> $+_.$ 3. Neutro Aditivo $\exists \vec 0 \in V : \vec 0 + \vec v = \vec v, \forall \vec v \in V$
> $+_.$ 4. Inverso Aditivo. $\forall \vec v \in V, \exists -\vec v \in V$ tal que $-\vec v + \vec v = \vec 0$
> $·_.$ 5. Cerradura. $\forall \alpha \in K, \vec u \in V : \alpha \vec u \in V$
> $·_.$ 6. Distributividad. $\forall \alpha \in K : \vec u, \vec v \in V : \alpha (\vec u + \vec v) = \alpha \vec u + \alpha \vec v$
> $·_.$ 7. Distributividad 2. $\forall \alpha, \beta \in K : \vec v \in V : (\alpha + \beta ) \vec v = \alpha \vec v + \beta \vec v$
> $·_.$ 8. \forall \alpha, \beta \in K; \vec v \in V: \alpha (\beta \vec v) = (\alpha \beta) \vec v
> $·_.$ 9. Si "1" es la unidad de $K: 1 \vec v, \forall \vec v \in V$

A los elementos de V se les llama vectores y a los de K escalares. A partir del sexto axioma se toma en cuenta el campo, los escalares toman la forma del campo.
La suma de $R^n$ es entrada por entrada, por ejemplo: $(x_1,y_1,z_1) + (x_2,y_2,z_2) = (x_1 + x_2, y_1 + y_2, z_1 + z_2)$
De igual forma con la multiplicación de los escalares: $\alpha (x,y,z) = (\alpha x, \alpha y, \alpha z)$
#### Propiedades de la adición.
> [! Abstract] Características en un espacio vectorial.
> Si $V$ es un espacio vectorial sobre K, entonces:
> 1. $\forall \vec u, \vec v, \vec w \in V : \vec u + \vec v = \vec u + \vec w \rightarrow \vec v = \vec w$
> 2. El vector $\vec 0$ es _único_ y es tal que $\vec v + \vec 0 = \vec v, \forall \vec v \in V$
> 3. El vector $-\vec v$ es único (para cada vector)y es tal que $-\vec v + \vec v = \vec 0$ para cada vector
> 4. La ecuación $\vec u + \vec x = \vec v$ tiene solución única en $V$. Es decir si sumamos "algo" a un vector v y nos dan un tercer vector entonces ese "algo" tambien es un vector de V
> 5. $\forall \vec v \in V : - (-\vec v) = \vec v$

#### Propiedades de la multiplicación de un escalar.
> [! Abstract ] Características  en un espacio vectorial
lkfs> Sea $V$ un espacio vectorial sobre $K$, $\forall \vec u, \vec v \in V; \alpha, \beta \in K$
> 1. $0 \vec v = \vec 0$, donde 0 es el cero de $K$, es decir un 0 escalar.
> 2. $\alpha \vec 0 = \vec 0$ es decir siempre nos da el cero vector.
 > 3. $(- \alpha) \vec v = - (\alpha \vec v) = \alpha(-\vec v)$ donde $- \vec v$ _NO_ es el inversos, simplemente es el vector pero con un menos.
 > 4. $\alpha \vec v = \vec 0 \rightarrow \alpha = 0$ ó $\vec v = \vec 0$
 > 5. $\alpha \vec u = \alpha \vec v$  y  $\alpha ≠ 0 \rightarrow \vec u = \vec v$
 > 6. $\alpha \vec v = \beta \vec v$  y  $\vec v ≠ \vec 0 \rightarrow \alpha = \beta$
 





### Subespacios vectoriales.
Sea V un espacio vectorial sobre K y sea S un subconjunto de $V$. Se dice que $S$ es un subespacio de $V$ si es un espacio vectorial sobre K la adicion y la multiplicación por un escalar definidas en $V$:
Se ve algo así: ![[SubespacioVectorial.excalidraw.png]]

> [! Important] Teorema para no verificar los 10 axiomas de espacio vectorial.
> Sea V un espacio vectorial sobre $K$ y sea $S$ un subconjunto de $V$. $S$ es un subespacio de $V$ si y solo si:
> 1. $\forall \vec u, \vec v \in S: \vec u + \vec v \in S$, la cerradura en la suma de vectores
> 2. $\forall \alpha \in K, \vec v \in S: \alpha \vec v \in S$, la cerradura en la multiplicación de vectores y escalares.