## Vector Norms
normはそれぞれのベクトルに対して実数値の長さを割り当てる関数$\|\cdot\|:\mathbb{C}^m\to \mathbb{R}$である。そして、次の3つの条件を満たす必要がある。
- $\|x\|\geq 0 \text{ for all } x\in \mathbb{C}^m,\ \text{and } \|x\|=0 \iff x=0,$
- $\|x+y\| \leq \|x\| + \|y\| \text{ for all } x,y\in \mathbb{C}^m,$
- $\|\alpha x\| = |\alpha| \|x\| \text{ for all } x\in \mathbb{C}^m,\ \alpha\in \mathbb{C}$.
## Matrix Norms Induced by Vector Norms
### p-norm 
The most important class of vector norms are the **p-norms** are defined below.The closed unit ball $\{x \in \mathbb{C}^m : \|x\|_p = 1\}$ corresponding to each norm is illustrated to the right for the case $m=2$.
<p align="center">
    <img width="696" src="https://github.com/user-attachments/assets/d38ffc8c-1397-41bd-be64-cf5bb3018f19" />
</p>
$A\in\mathbb{C}^{m \times n}$,respectively, the induced matrix norm $\|A\|_{mn}$ is the smallest number C for which the following inequality holds for all $x\in \mathbb{C}^n$:
$$
\|Ax\|_m \leq C \|x\|_n
$$
In other words, $\|A\|_{mn}$is the supremum(上限) of the ratio $\|Ax\|_m/\|x\|_n$ over vectors $x\neq 0$ in $\mathbb{C}^n$-- the maximum factor by which A can "stretch" a vector x.
上限とは最大値のようなものである。たとえば、$x<5$は5は含まれないが、5より小さい値であればどんなに5に近くても良い。つまり、5は上限である。比率であり、上限であるから
$A$が作用したことによって、$x$がどれだけ伸びうるかを表しており、誤差に対して重要な役割を果たす。
\begin{align}
\|A\|_{mn}
= \sup_{\substack{x \in \mathbb{C}^n \\ x \neq 0}}
\frac{\|Ax\|_m}{\|x\|_n}
= \sup_{\substack{x \in \mathbb{C}^n \\ \|x\|_n = 1}}
\|Ax\|_m \label{eq:induced_matrix_norm}
\end{align}
行列ノルムは$A$によって誤差の最大何倍ベクトルを増幅させるかを表している。行列ノルムはを基準とし、どのp-normを使うかで行列ノルムの値が変わる。
\paragraph{1-norm}1ノルムは以下のように定義される。
\[\|x\|_1=\sum_{j=1}^{n}|x_j|\]
行列ではないので、要素の絶対値の和となる。
$Ax$は行単位でシグマを用いると、
\[Ax=
\begin{bmatrix}
    \sum_{j}^{} a_{1j}x_j\\
    \sum_{j}^{} a_{2j}x_j\\
    \dots\\
    \sum_{j}^{} a_{mj}x_j\\
\end{bmatrix}\]
\[
\|Ax\|_1 = \sum_{i=1}^{m}\left|\sum_{j=1}^{n}a_{ij}x_j\right|
\]
これは絶対値の和であるから、三角不等式より、
\[
\sum_{i=1}^{m}\left|\sum_{j=1}^{n}a_{ij}x_j\right|\leq
\sum_{i=1}^{m}\sum_{j=1}^{n}|a_{ij}x_j|=\sum_{i=1}^{m}\sum_{j=1}^{n}|a_{ij}||x_j|=\sum_{j=1}^{n}\left(\sum_{i=1}^{m}|a_{ij}|\right)|x_j|
\]
$\displaystyle\|x\|_1=\sum_{j=1}^{n}|x_j|$であるから、
\begin{equation}
    \sup_{\substack{x \in \mathbb{C}^n \\ x \neq 0}}
    \frac{\|Ax\|_1}{\|x\|_1}=\max_{1\leq j\leq n}\sum_{i=1}^{m}|a_{ij}|=\max_{1\leq j\leq n}\|a_j\|_1
\end{equation}
つまり行列$A$の1-normは\textbf{各列ベクトルの要素和における最大値}となる。
\paragraph{$\infty$-norm}$\infty$ノルムは以下のように定義される。
$$\|x\|_{\infty}=\max_{1\leq j\leq m}|x_j|$$
これは要素の絶対値の中での最大値となる。
同様にして、行列$Ax$では
$$
\|Ax\|_{\infty}=\max_{1\leq i\leq m}\left|\sum_{j=1}^{n}a_{ij}x_j\right|
\leq\max_{1\leq i\leq m}\left(\sum_{j=1}^{n}|a_{ij}|\right)|x_j|
=\max_{1\leq i\leq m}\sum_{j=1}^{n}|a_{ij}|\|x\|_{\infty}
$$
$
\begin{equation}
    \sup_{\substack{x \in \mathbb{C}^n \\ x \neq 0}}
    \frac{\|Ax\|_{\infty}}{\|x\|_{\infty}}=\max_{1\leq i\leq m}\sum_{j=1}^{n}|a_{ij}|=\max_{1\leq i\leq m}\|a^*_i\|_1
\end{equation}
$
つまり行列$A$の1-normは**各行ベクトルの要素和における最大値**となる。

### Cauchy--Schwarz and Hölder Inequalities
Computing matrix p-norm with $p\neq1,\infty$ is more difficult, and to approach this problem, 
we note that inner products can be bounded using p-norms. Let $p$ and $q$ satisfy $1/p + 1/q = 1$, with $1\leq p,q \leq \infty$. 
Then the **Hölder inequality** sates that, for any vectors $x$ and $y$,
$$
|x^* y| \leq \|x\|_p \|y\|_q.
$$
The Cauchy--Schwarz inequality is the special case of Hölder inequality with $p=q=2$:
$$|x^* y| \leq \|x\|_2 \|y\|_2.$$
### The 2-Norm of a Row Vector
Consider a matrix A containing a single row. The matrix can be written as $A=x^*$, where $a$ is a column vector. The Cauchy--Schwarz inequality allows us to obtain the induced matrix 2-norm.
For any $x$,  we have $\|Ax\|_2=|a^* x|\leq \|a\|_2\|x\|_2$.
$$
\|A\|_2 = \sup_{x\neq0}\frac{\|Ax\|_2}{\|x\|_2} = \|a\|_2.
$$
### The 2-Norm of an Outer Product
if $A=uv^*$, we can bounded $\|Ax\|_2$ as follows:
$$
\|Ax\|_2 = \|uv^*x\|_2 = \|u\|_2|v^*x|\leq \|u\|_2\|v\|_2\|x\|_2
$$
Therefore, $\|A\|_2 = \|u\|_2\|v\|_2$. Again, this inequality is equality: consider the case $x=v$.
\subsubsection*{General Matrix Norms}
行列も式\eqref{eq:norm_axioms}に従う。
$
\begin{equation}
\label{eq:norm_axiomsA}
\begin{aligned}
    &\|A\|\leq0,\text{and} \|A\|=0 \text{only if} A=0,\\
    &\|A+B\|\leq \|A\|+\|B\|,\\
    &\|\alpha A\|=|\alpha|\|A\|.
\end{aligned}$
The most important matrix norm which is **not induced** by a vector norm is the **Frobenius norm** or **Frobenius norm**, defined by
$$
    \|A\|_F = \left(\sum_{i=1}^{m}\sum_{j=1}^{n}|a_{ij}|^2\right)^{1/2}.
$$
2-normとトレースを用いても表すことができる。
$$
    \|A\|_F=\left(\sum_{j=1}^{n}\|a_j\|_2^2\right)^{1/2}=\sqrt{\mathrm{tr}(A^*A)}=\sqrt{\mathrm{tr}(AA^*)}
$$
’’’python3
import numpy as np

A = np.array([[1, 2], [3, 4]])
sum1 = np.sqrt(np.sum(A**2))
sum2 = np.sqrt(np.trace(A.T@A))
sum3 = np.sqrt(np.trace(A@A.T))
print(sum1) # 5.477225575051661
print(sum2) # 5.477225575051661
print(sum3) # 5.477225575051661
’’’
また、Unitary行列$Q$に対して、Frobenius normは不変である。
$$\|QA\|_F=\|A\|_F,\quad \|AQ\|_F=\|A\|_F$$
