2.1
$(X, M)$ is a measurable space and $f$ is a extended real measurable function on $X$. If $E$ is a measurable set, let $a \in \bar R$ and define $g$ as
$$
g(x) = \left\{\begin{matrix} 
  f(x), x \notin E\\
  a, x \in E
\end{matrix}\right.
$$
then $g$ is measurable.

Proof. For any borel subset $B$ of $\bar R$, $g^{-1}(B) = (g^{-1}(B) \cap E) \cup (g^{-1}(B) \cap E^{c})$ and $g^{-1}(B) \cap E^{c} = f^{-1}(B) \cap E^{c}$. If $a \notin B$, then $g^{-1}(B) \cap E = \phi$, else $g^{-1}(B) \cap E = E$. Thus $g^{-1}(B) \in M$ and $g$ is measurable.


2.2
$(X, M)$ is a measurable space and $f, g$ are extended real measurable functions on $X$. Let $E = \left \{ x \in X | f=-g=\infty \text{ or } f=-g=-\infty \right \}$ and $a \in \bar R$, define $f_{1}, g_{1}, h$ as
$$
f_{1}(x) = \left\{\begin{matrix} 
  f(x), x \notin E\\
  a, x \in E
\end{matrix}\right.
$$
$$
g_{1}(x) = \left\{\begin{matrix} 
  g(x), x \notin E\\
  a, x \in E
\end{matrix}\right.
$$
$$
h(x) = f_1(x)+g_1(x)
$$
then $f_1,g_1,h$ is measurable.

Proof. $E = (\left \{ f=\infty \right \} \cap \left \{ g=\infty \right \}) \cup (\left \{ f=-\infty \right \} \cap \left \{ g=-\infty \right \})$ is measurable, so $f_1, g_1, h$ is measurable due to 2.1.


2.3
$(X, M)$ is a measurable space and $\{f_n\}_n$ are extended real measurable functions on $X$. $E = \left \{ x \in X | \lim  f_n(x) \text{ exists} \right \}$ is measurable.

Proof. $f_1=\lim \sup f_n, f_2=-\lim \inf f_n$. Let $a=1$ and define $h$ as 2.2. Limits exist iff $x \in Ker(h)$. $Ker(h)$ is measurable so $E = Ker(h)$ is measurable.


