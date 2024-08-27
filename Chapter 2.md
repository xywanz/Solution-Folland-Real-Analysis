**2.29 Proposition.** If $f_n \rightarrow f$ f in $L_1$, then $f_n \rightarrow f$ in measure.

Proof. $\int |f_n - f| \ge \int_{E_{n,\epsilon}} |f_n - f| \ge \int_{E_{n,\epsilon}} \epsilon = \epsilon \mu(E_{n,\epsilon})$, so $\mu(E_{n,\epsilon}) \le \epsilon^{-1} \int |f_n - f| \rightarrow 0$.


**2.30 Theorem**. Suppose that $\{f_n\}$ is Cauchy in measure. Then there is a measurable function $f$ such that $f_n \rightarrow f$ in measure, and there is a subsequence ${f_{n_j}}$ that converges to $f$ a.e. Moreover, if also $f_n \rightarrow g$ in measure, then $g= f$ a.e.

Proof. $\forall j \in \mathbb N^+$, $\exists N_j > 0$, s.t.$$\mu(\{ x: |f_n(x) - f_m(x)| >= 2^{-j} \}) < 2^{-j}$$whenever $n,m \ge N$.
So we can choose a subsequence $\{g_j\}$ from $\{f_n\}$ such that if $$E_j = \{ x: |g_j(x) - g_{j+1}(x)| >= 2^{-j} \}$$then $\mu(E_j) < 2^{-j}$. 
Let $$\{F_k\} = \bigcup_{j=k}^{\infty} E_j$$then $$\mu(F_k) \le \sum_{j=k}^{\infty} \mu(E_j) = \sum_{j=k}^{\infty} 2^-j = 2^{1-k}$$Let $$F = \bigcap_{k=1}^{\infty} F_k$$then $\mu(F) = 0$ because $\mu(F) \le \mu(F_k) \le 2^{1-k}$ for every $k$.
Given $\epsilon > 0$, if $x \notin F$, then there exists $k$ such that $x \notin F_k$ and $2^{1-k} < \epsilon$. If $m \ge n \ge k$, then$$|g_n(x) - g_m(x)| \le \sum_{i=n}^{m-1} |g_i - g_{i+1}| \le \sum_{i=n}^{m-1} 2^{-i} \le 2^{1-j} \le 2^{1-k} < \epsilon$$So $\{g_j\}$ is Cauchy a.e.

Define $f(x) = \lim_{j \to \infty} g_j(x)$ if $x \notin F$, otherwise $f(x) = 0$. Then $f$ is measurable and $g_j \rightarrow f$ a.e. by exercise 2.5 ($f|_{F^c}$ is the pointwise limit of measurable functions $\{g_n\}$, so $f$ is measurable on $F^c$. Also, $f$ is a constant function on F, so f is measurable on $F$. Thus $f$ is measurable on $X$).

Given $\epsilon > 0$, there is $k \in \mathbb N^+$, such that $2^{1-k} < \epsilon$. If $x \notin F_k$ and $m,n \ge k$, then $$|g_n(x) - g_m(x)| < \epsilon$$Let $m \rightarrow \infty$, then for every $n \ge k$, $|g_n(x) - f(x)| < \epsilon$, implying that $$\{ x: |g_n(x) - f(x)| \ge \epsilon \} \subseteq F_k$$Then $\mu(\{ x: |g_n(x) - f(x)| \ge \epsilon \}) \le \mu(F_k) < \epsilon$ for every $n \ge k$, so $\{g_j\}$ converges in measure.

$|f_n(x) - f(x)| \le |g_j(x) - f_n(x)| + |g_j(x) - f(x)|$
$\implies \{ x: |f_n(x) - f(x)| \ge \epsilon \} \subseteq \{ x: |g_j(x) - f_n(x)| \ge \frac{\epsilon}{2} \} \cup \{ x: |g_j(x) - f(x)| \ge \frac{\epsilon}{2} \}$$\implies \mu(\{ x: |f_n(x) - f(x)| \ge \epsilon \}) \le \mu(\{ x: |g_j(x) - f_n(x)| \ge \frac{\epsilon}{2} \}) + \mu(\{ x: |g_j(x) - f(x)| \ge \frac{\epsilon}{2} \})$Given $\epsilon > 0, \epsilon' > 0$. There is $N \in \mathbb N^+$ such that $\mu(\{ x: |g_j(x) - f_n(x)| \ge \frac{\epsilon}{2} \}) < \frac{\epsilon'}{2}$ whenever $j,n \ge N$ because $\{f_n\}$ is Cauchy in measure. Also, there is $M \in \mathbb N^+$ such that $\mu(\{ x: |g_j(x) - f(x)| \ge \frac{\epsilon}{2} \}) < \frac{\epsilon'}{2}$ whenever $j \ge M$ because $g_j \rightarrow f$ in measure. So, if $j,n \ge \max(N,M)$, then $\mu(\{ x: |f_n(x) - f(x)| \ge \epsilon \}) < \epsilon'$, which implies $f_n \rightarrow f$ in measure.

$|g(x) - f(x)| \le |f_j(x) - g(x)| + |g_j(x) - f(x)|$
$\implies \{ x: |g(x) - f(x)| \ge \epsilon \} \subseteq \{ x: |f_j(x) - f(x)| \ge \frac{\epsilon}{2} \} \cup \{ x: |g_j(x) - f(x)| \ge \frac{\epsilon}{2} \}$$\implies \mu(\{ x: |g(x) - f(x)| \ge \epsilon \}) \le \lim_{j \to \infty} \mu(\{ x: |f_j(x) - f(x)| \ge \frac{\epsilon}{2} \}) + \lim_{j \to \infty} \mu(\{ x: |g_j(x) - f(x)| \ge \frac{\epsilon}{2} \}) = 0$Because $\{ x: |g(x) - f(x)| > 0 \} = \bigcup_{k=1}^{\infty} \{ x: |g(x) - f(x)| \ge \frac{1}{k} \}$, we have $\mu(\{ x: |g(x) - f(x)| > 0 \}) = \lim_{k \to \infty} \mu(\{ x: |g(x) - f(x)| \ge \frac{1}{k} \}) = 0$. Thus $g=f$ a.e.


**2.33 Egoroff's Theorem.** Suppose that $\mu(X)<\infty$, and $f_1,f_2,...$ and $f$ are mea­surable complex-valued functions on X such that $f_n \rightarrow f$ a.e. Then for every $\epsilon > 0$ there exists $E \subseteq X$ such that $\mu(E) < \epsilon$ and and $f_n \rightarrow f$ uniformly on $E^c$.

Proof. Without loss of generality, we can assume $f_n \rightarrow f$ everywhere. Let $E_{n,k} = \bigcup_{j=n}^{\infty} \{ x: |f_j(x) - f(x)| \ge \frac{1}{k} \}$. Then, for fixed $k$, $\{E_{n,k}\}_n$ is a decreasing sequence, $\mu(E_{1,k}) < \infty$ and $\bigcap_{n=1}^{\infty} E_{n,k}$. So $\mu(\bigcap_{n=1}^{\infty} E_{n,k}) = \lim_{n \to \infty} E_{n,k} = 0$. Therefore, for every $k \in \mathbb N^+$, there exists $n_k$ such that $\mu(E_{n_k,k}) < \epsilon 2^{-k}$. Let $E = \bigcup_{k=1}^{\infty} E_{n_k,k}$, then $\mu(E) < \epsilon$, and we have $|f_n(x) - f(x)| < \frac{1}{k}$ for $n \ge n_k$ and $x \notin E$. Thus $f_n \rightarrow f$ uniformly on $E^c$.


#### Exercises

2.3. If $\{f_n\}$ is a sequence of measurable functions on $X$, then $\{x: \lim f_n(x) \text{ exists}\}$ is a measurable set.

Proof. Suppose $\{f_n\}$ are extended real-valued functions. Let
$$A = \{x: \lim f_n(x) \text{ exists and is finite}\}$$
$$B = \{ x: \lim_{n \to \infty} f_n(x) = \infty \}$$
$$C = \{ x: \lim_{n \to \infty} f_n(x) = -\infty \}$$
Then
$$\{x: \lim f_n(x) \text{ exists}\} = A \cup B \cup C$$
Because $\{f_n\}$ converges to a real number iff $\{f_n\}$ is Cauchy, we can rewrite $A$ as
$$A = \bigcap_{k=1}^{\infty} \bigcup_{N=1}^{\infty} \bigcap_{n,m \ge N} \{ x: |f_n(x) - f_m(x)| < \frac{1}{k} \}$$
$B$ and $C$ can be rewritten as$$B = \bigcap_{M=1}^{\infty} \bigcup_{N=1}^{\infty} \bigcap_{n \ge N}^{\infty} \{ x: f_n(x) > M \}$$and$$C = \bigcap_{M=1}^{\infty} \bigcup_{N=1}^{\infty} \bigcap_{n \ge N}^{\infty} \{ x: f_n(x) < -M \}$$Given $k,N,n,m$, then $\{ x: |f_n(x) - f_m(x)| < \frac{1}{k} \}$ is measurable, so $A$ is measurable. Also, Given $M,N,n$, $\{ x: f_n(x) > M \}$ and $\{ x: f_n(x) < -M \}$ are measurable, so are B and C. Therefore, $\{x: \lim f_n(x) \text{ exists}\}$ is measurable when $\{f_n\}$ are measurable real-valued functions.
If $\{f_n\}$ are measurable complex-valued functions, then $lim f_n(x)$ exists iff both $\lim Ref(x)$ and $\lim Imf(x)$ exist and are finite. Then $\{x: \lim f_n(x) \text{ exists}\}$ is measurable by applying the result in the previous paragraph to $Ref$ and $Imf$ respectively.


2.5. If $X = A \cup B$ where $A,B \in \mathcal M$, a function $f$ on $X$ is measurable iff $f$ is measurable on $A$ and on $B$.

Proof. $\forall E \in \mathcal B$, $f^{-1}(E) = (f^{-1}(E) \cap A) \cup (f^{-1}(E) \cap B)$.


2.33. If $f_n \ge 0$ and $f_n \rightarrow f$ in measure, then $\int f \le \liminf \int f_n.$

Proof. Suppose $\liminf \int f_n < \int f$. Then there is $c \in \mathbb R$ such that $\liminf \int f_n < c < \int f$. So we can choose a subsequence $\{f_{n_j}\}$ from $\{f_n\}$ such that $\lim f_{n_j} < c$. Because $\{f_{n_j}\}$ also converges to $f$ in measure, there is a subsequence $\{g_k\}$ of $\{f_{n_j}\}$ such that $\{g_k\} \rightarrow f$ a.e. Then we have $\int f \le \liminf \int g_k = \lim \int g_k < c$ by Fatou' lemma, which implies a contradiction.

2.34. Suppose $|f_n| \le g \in L^1$ and $f_n \rightarrow f$ in measure.
	a. $\int f = \lim \int f_n.$
	b. $f_n \rightarrow f$ in $L^1.$

Proof.
a. 

#### Supplement
**S.1 Proposition.** If $\{f_n\}$ converges in measure, then $\{f_n\}$ is Cauchy in measure.

Proof. Let $$E_{n,\epsilon} = \{ x: |f_n(x) - f(x)| \}$$ and $$F_{m,n,\epsilon} = \{ x: |f_n(x) - f(x)| \}$$Then$$\forall \epsilon > 0,\exists N, \text{ s.t. } \forall n \ge N, \mu(E_{n,\epsilon}) < \frac{\epsilon}{2}$$If $m, n \ge N$, then $$F_{m,n,\epsilon} \subseteq E_{m,\epsilon} \cup E_{n,\epsilon}$$following from $$|f_m(x) - f_n(x)| \le |f_m(x) - f(x)| + |f_n(x) - f(x)|$$Thus$$\mu(F_{m,n,\epsilon}) <= \mu(E_{m,\epsilon}) + \mu(E_{n,\epsilon}) < \epsilon$$implying $\{f_n\}$ is Cauchy in measure.
