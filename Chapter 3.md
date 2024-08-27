3.8. $v \ll \mu$ iff $|v| \ll \mu$ iff $v^+ \ll \mu$ and $v^- \ll \mu$

Proof. If $v \ll \mu$, then $\forall E \in M (\mu(E) = 0), v(E) = 0, v^+(E) = v(E \cap P) = 0, v^-(E) = v(E \cap N) = 0$, which implies $|v|(E) = 0$, so $|v| \ll \mu$. If $|v| \ll \mu$, then $\forall E \subseteq M(\mu(E) = 0), |v|(E) = v^+(E) + v^-(E) = 0$, which implies $v^+(E) = 0$ and $v^-(E) = 0$, so $v^+ \ll \mu$ and $v^- \ll \mu$. If $v^+ \ll \mu$ and $v^- \ll \mu$, then $\forall E \subseteq M(\mu(E) = 0), v^+(E) = 0, v^-(E) = 0, v(E) = v^+(E) - v^-(E) = 0$, which implies $v \ll \mu$.


3.9. Suppose $\{v_j\}$ is a sequence of positive measures. If $v_j \perp \mu$ for all $j$, then $\sum_1^{\infty} v_j \perp \mu;$ and if $v_j \ll \mu$ for all $j$, then $\sum_1^{\infty} v_j \ll \mu$.

Proof. Suppose $X = E_j \cup F_j, E_j \cap E_j = \phi, F_j \text{ is null for } v_j \text{ and } E_j \text{ is null for } \mu$. Let $F = \bigcap_{1}^{\infty} F_j \text{ and } E = F^c$. It's obvious that $F$ is null for all $v_j$, and thus for $\sum_1^{\infty} v_j$. Now we need to claim E is null for $\mu$. Let $D_1 = E_1$ and $D_j = E_j \text{\\} \bigcup_1^{n-1} E_j$ for $j >= 2$, then $D_j$ is a disjoint sequence, $\sum_1^{\infty} D_j = \sum_1^{\infty} E_j$, and $D_j$ is null for $\mu$ for all $j$ because $D_j \subseteq E_j$ and $E_j$ is null for $\mu$ since $v_j \perp \mu$. Therefore, $\forall A \in M(A \subseteq E), \mu(A) = \sum_1^{\infty} \mu(A \cap D_j) = 0$. The second assertion is trivial.


3.10. Theorem 3.5 may fail when $v$ is not finite.

Proof. Let $v$ be the counting measure and $\mu(E) = \sum_{n \in E} 2^{-n}$ on $N$. Then $\forall \delta > 0$, Choose $n$ such that $2^{-n} < \delta$, then $\mu(\{n\}) < \delta$ but $v(\{n\}) = 1$. 


3.11. Let $\mu$ be a positive measure. A collection of functions $\{f_{\alpha}\}_{\alpha \in A} \subseteq L^1(\mu)$ is called uniformly integrable if for every $\epsilon > 0$ there exists $\delta > 0$ such that $|\int_E f_{\alpha} d\mu| < \epsilon$ for all $\alpha \in A$ whenever $\mu(E) < \delta$.
	a. Any finite subset of $L^1(\mu)$ is uniformly integrable.
	b. If $\{f_n\}$ is a sequence in $L^1(\mu)$ that converges in the $L^1$ metric to $f \in L_1(\mu)$, then $\{f_n\}$ is uniformly integrable.

Proof.
(a) Let $\delta = min\{\delta_1, \delta_2, ..., \delta_n\}$.
(b) $\forall \epsilon > 0$, there exists $n_0 \in N$ such that $\int |f_n - f|d\mu < \frac{\epsilon}{2}$ whenever $n >= n_0$. $\int_E |f_n - f|d\mu = \int \chi_E|f_n - f| <= \int |f_n - f|d\mu < \frac{\epsilon}{2}$. We have
$$
	|\int_E f_n d\mu| <= \int_E |f_n| d\mu <= \int_E |f_n - f + f| d\mu <= \int_E |f_n - f| d\mu + \int_E |f| d\mu
$$
There exists $\delta_0 > 0$ such that $\int_E |f| d\mu < \frac{\epsilon}{2}$ whenever $\mu(E) < \delta_0$ due to $f \in L^1$. Let $\delta = min\{\delta_0, \delta_1, ..., \delta_{n-1}\}$, then $|\int_E f_n d\mu| <= \int_E |f_n - f| d\mu + \int_E |f| d\mu < \epsilon$ for every $n \in N$ whenever $\mu(E) < \delta$.


3.12. For $j=1,2$, let $\mu_j, v_j$ be $\sigma$-finite measures on $(X_j, \mathcal M_j)$ such that $v_j \ll \mu_j$. Then $v1 \times v2 \ll \mu_1 \times \mu_2$ and
$$
	\frac{d(v_1 \times v_2)}{d(\mu_1 \times \mu_2)}(x_1, x_2) = \frac{dv_1}{d\mu_1}(x_1) \frac{dv_2}{d\mu_2}(x2).
$$

Proof. First claim that $\frac{dv_j}{d\mu_j} \ge 0 \text{ } \mu_j\text{-a.e.}$
By Tonelli's theorem, 
$$
\begin{aligned}
	v1 \times v2(E) &= \int_{X_1 \times X_2} \chi_E d(v_1 \times v_2) \\
	&= \int_{X_1} \int_{X_2} \chi_E dv_2 dv_1 \\
	&= \int_{X_1} \int_{X_2} \chi_E f_2 d\mu_2dv_1 \\
	&= \int_{X_1} \int_{X_2} \chi_E f_1f_2 d\mu_2d\mu_1 \\
	&= \int_E f_1f_2 d(\mu_1 \times \mu_2)
\end{aligned}
$$

$$
	\frac{d(v_1 \times v_2)}{d(\mu_1 \times \mu_2)}(x_1, x_2) = \frac{dv_1}{d\mu_1}(x_1) \frac{dv_2}{d\mu_2}(x2).
$$


3.13. Let $X = [0, 1]$, $\mathcal M = \mathcal B_{[0,1]}, m =$ Lebesgue measure, and $\mu=$ counting measure on $\mathcal M$.
	a. $m \ll \mu$ but $dm \ne f d\mu$ for any $f$.
	b. $\mu$ has no Lebesgue decomposition with respect to $m$.

Proof. 
a. $\mu(E) = 0$ iff $E=\phi$, so $m \ll \mu$. Suppose there exists $f$ such that $dm = fd\mu$, then $\int_{[0,1]} f d\mu = \sum_{x \in [0,1]} f(x) = 1$, which implies there exists $a \in [0,1]$ such that $f(a) > 0$, and $m(\{a\}) = \int_{\{a\}} f d\mu = f(a) > 0$, contradicting $m(\{a\}) = 0$.
b. If $\mu$ has a Lebesgue decomposition with respect to $m$, $d\mu = d\lambda + \rho$. Obviously, $\lambda \ne 0$. Then there exist $E, F$ such that $E \cup F = X, E \cap F = \phi, E$ is null for $m$ and $F$ is null for $\lambda.$ $E$ is a $m$-null set, so $m(F) = 1$, so there is a countable subset $A$ of $F$ satisfying $\mu(A) = \rho(A)$. $\mu(A) = \infty$ but $\rho(A) = 0$ due to absolute continuity, which is a contradiction.


3.14. If $v$ is an arbitrary signed measure and $\mu$ is a $\sigma$-finite measure on $(X, \mathcal M)$ such that $v \ll \mu$, there exists and extended $\mu$-integrable function $f: X \to [-\infty, \infty]$ such that $dv = fd\mu$. Hints:
	a. It suffices to assume that $\mu$ is finite and $v$ is positive.
	b. With these assumptions, there exists $E \in \mathcal M$ that is $\sigma$-finte for $v$ such that $\mu(E) \ge \mu(F)$ for all sets $F$ that are $\sigma$-finite for $v$.
	c. The Radon-Nikodym theorem applies on $E$. If $F \cap E = \phi$, then either $v(F) = \mu(F) = 0$ or $\mu(F) > 0$ and $|v(F)| = \infty$.

Proof. 