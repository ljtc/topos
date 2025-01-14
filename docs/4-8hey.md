---
layout: page
title: Objetos retícula y álgebra de Heyting en un topos
description: >
  Definición del concepto de topos
hide_description: true
sitemap: false
---

Empezamos esta sección describiendo quiénes serán los objetos que queremos encontrar de manera interna en un topos.

### Definición
Una retícula es una categoría de orden parcial finitamente completa y cocompleta.

### Definición
Un álgebra de Heyting es una retícula cartesianamente cerrada, es decir, el producto tiene adjunto derecho.

En una categoría en general el adjunto izquierdo del producto se denota con una exponencial. En el caso de categorías de 
orden parcial es común denotar a este adjunto derecho con una implicación. Así, si $$H$$ es un álgebra de Heyting, 
entonces la biyección de "flechas" que define la adjunción es

$$
\begin{array}{c}
a\land b\leq c\\
\hline
b\leq (a\Rightarrow c)
\end{array}
$$

El ejemplo canónico de un álgebra de Heyting es la categoría generada por los abiertos de un espacio topológico ordenados 
con la contención. Otro ejemplo, con el cual podemos explicar la notación de la exponencial en este contexto, es 
considerar formulas proposicionales y ordenarlas como $$\alpha\leq\beta\iff \alpha\vdash\beta$$ si queremos hacer un 
álgebra a partir de la sintaxis, o bien, $$\alpha\leq\beta\iff \alpha\vDash\beta$$ si preferimos la semántica. 
Desgraciadamente esta relación no satisface la antisimetría, así que no ordena parcialmente al conjunto de fórmulas (que 
denotaremos $$Form$$). Esto nos obliga a hacer un cociente módulo la relación de ser lógicamente equivalente. Así, 
$$(Form/\equiv,\leq)$$ es un orden parcial.

El orden parcial $$(Form/\equiv,\leq)$$ tiene la estructura que nos interesa, ya que la conjunción induce un ínfimo 
(producto), la disyunción un supremo (coproducto), la clase de una tautología es el máximo (terminal) y la clase de una 
contradicción es el mínimo (inicial). Con esto tenemos que nuestro orden parcial es de hecho una retícula. Más aún, si 
escribimos la relación que define a la implicación desde el punto de vista sintáctico obtenemos

$$
a\land b\vdash c \iff b\vdash(a\Rightarrow c)
$$

Esta relación, en lógica de proposiciones, se conoce como el teorema de la deducción. Así, el teorema de la deducción 
afirma que $$(Form/\equiv,\leq)$$ es cartesiana cerrada. En otras palabras, $$(Form/\equiv,\leq)$$ es un álgebra de 
Heyting.

La unidad y la counidad de la adjunción también se interpretan como relaciones conocidas en lógica de proposiciones. La 
unidad es una forma de expresar al primer axioma del cálculo de proposiciones de Mendelson y la counidad es el 
*modus ponens*.

<p>
<iframe width="560" height="315" src="https://www.youtube.com/embed/IvSG0WNIb_s" title="Clase40" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</p>

Es posible demostrar muchas de las propiedades conocidas de la implicación en lógica. En nuestra aproximación a la 
implicación, no es necesario hacer tablas de verdad ni ninguna justificación sintáctica para obtener dichas propiedades. 
Con nuestra técnica las adjunciones son más que suficiente para deducir todo lo que necesitamos.

En este contexto se define la negación en términos de la implicación. Por lo tanto, sus propiedades son inducidas por la s 
de la implicación y así, a final de cuentas, por las adjunciones.

<p>
<iframe width="560" height="315" src="https://www.youtube.com/embed/333MjEvSFTQ" title="Clase41" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</p>

Una vez que tengamos las propiedades correctas acerca de la implicación podremos definir un álgebra de Heyting como una 
estructura algebraica que satisface ciertos axiomas. Una de las ventaja de la visión algebraica sobre la de retículas es 
que es más fácil de dotar de estructura algebraica a un objeto de una categoría para obtener, en nuestro caso, un álgebra 
de Heyting interna.

<p>
<iframe width="560" height="315" src="https://www.youtube.com/embed/h6BFIKP8QaU" title="Clase42" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</p>

Ahora podemos demostrar el objetivo de hace algunas clases, demostrar que $$Sub(A)$$ es un álgebra de Heyting, para todo 
$$A\in\mathcal{E}$$ y que si $$k\colon B\to A$$ está en $$\mathcal{E}$$ entonces $$k^{-1}\colon Sub(A)\to Sub(B)$$ es un 
morfismo de álgebras de Heyting.

Para demostrar que $$Sub(A)$$ es un álgebra de Heyting empezaremos mostrando que $$Sub(1)$$ es un álgebra de Heyting y 
luego el *teorema fundamental de la teoría topos* ($$\mathcal{E}/A$$ es un topos) para deducir el resto. Luego, para 
demostrar $$k^{-1}\colon Sub(A)\to Sub(B)$$ usaremos al funtor cambio de base $$k^* \colon\mathcal{E}/A\to\mathcal{E}/B$$
y lo que ya sabemos de él, tiene adjunto izquierdo y derecho, además es un morfismo lógico.

El siguiente paso en este camino es demostrar que $$PA$$ es un álgebra de Heyting interna, para todo $$A\in\mathcal{E}$$.
En particular tendremos que $$\Omega=P1$$ tiene estructura de álgebra de Heyting. Para esto consideramos el isomorfismo 
natural

$$
Sub(A\times X)\cong\mathcal{E}(X,PA)
$$

y el lema de Yoneda-Grothendieck para inducir la estructura de álgebra de Heyting interna para $$PA$$.

<p>
<iframe width="560" height="315" src="https://www.youtube.com/embed/jsH_sfh9Hng" title="Clase43" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</p>

La estructura sobre $$\Omega$$ es de especial importancia en un topos ya que una flecha $$A\to\Omega$$ se puede 
interpretar como una fórmula con una variable libre de tipo $$A$$. Debido a esta interpretación estas flechas se denotan 
con $$\varphi$$, $$\psi$$, etc. 

Ver el primer vídeo en [La condición de Beck-Chevalley](./4-9bc.md).