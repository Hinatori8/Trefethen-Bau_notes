(全体:2015/12/07)
## Adjoint
hermitian conjugate もしくは adjoint はエルミート転置もしくは共役転置を意味する。

$$
A=\begin{bmatrix}
    a_{11} & a_{12} \\
    a_{21} & a_{22} \\
    a_{31} & a_{32} 
\end{bmatrix}
\qquad \Rightarrow \qquad
A^*=\begin{bmatrix}
    \overline{a}_{11} & \overline{a}_{21} & \overline{a}_{31} \\
    \overline{a}_{12} & \overline{a}_{22} & \overline{a}_{32}
\end{bmatrix}
$$

もし、

$A=A^*$

であるなら行列Aはhermitian matrix（エルミート行列）であると言う。行列の要素が複素数であった場合は、転置と同時に共役な要素に変わることを意味するが、
実数のみの行列であるならば、単純に行列が転置しただけと変わらない。実対称行列もエルミート行列の仲間である。今まで使ってきた$A^T$は実行列の中ではtransposeとなるが、複素数まで拡大するとエルミート転置を意味していると考えられる。
つまり、実行列に対する転置を意味する記号として、hermitian conjugateを意味する$*$を使うことができる。
## Inner Product 
$x,y\in \mathbb{C}^m$ に対して、内積は

$$
x^* y = \sum_{i=1}^{m} \overline{x}_i y_i
$$

と定義される。今までは実数ベクトルに対しての内積を考えていたため、転置するだけであったが、複素数まで対応させた内積はエルミート転置を使う必要がある。前述の通り、実数であったために共役を考える必要がなかった。
## Orthogonal Vectors
- A set of nonzero vectors S is **orthogonal**(直交) if its elements are pairwise orthogonal, i.e., if for $x,y\in S,\;x\neq y\Rightarrow x^* y = 0$.
- A set of nonzero vectors S is **orthonormal**(正規直交) if it is orthogonal and if for all $x\in S,\;\|x\| = 1$.

## Unitary Matrices
 $Q^*=Q^{-1},\;Q^*Q=I$ を満たす正方行列$Q$を**unitary**という。また、 $Q$ が実行列であるなら、Orthogonalとなる。つまり、実行列は大きく言えばunitaryであり、同じく条件を満たす。
