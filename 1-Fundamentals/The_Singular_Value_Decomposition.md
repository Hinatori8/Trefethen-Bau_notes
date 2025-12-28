## Reduced SVD
Aはfull rank nでVはunitayであるため、$V^{-1}=V^*$、$\hat{U}$は$m\times n$の直交行列、$\hat{\Sigma}$は正方行列とする。
$$A=\hat{U}\hat{\Sigma}V^*$$
This factorization of A is called a **reduced singular value decomposition**, or **reduced SVD**, of A. Schematically, it looks likes this:
\begin{figure}[H]\centering
    \includegraphics[width=0.4\hsize]{reducedSVD.png}
\end{figure}
## Full SVD
$\hat{U}$ is not unitary. However, by adjoining an additional $m-n$ orthonormal columns to $\hat{U}$ can be extended to a unitary matrix $U$.

If $\hat{U}$ is replaced by $U$, then $\hat{\Sigma}$ will have to change too. the last $m-n$ columns of $U$ should be multiplied by zero.
\begin{figure}[H]\centering
    \includegraphics[width=0.4\hsize]{FullSVD.png}
\end{figure}
$U$と$V$はユニタリー行列となるから、
\begin{equation}
A=U\Sigma V^* \label{eq:FullSVD}
\end{equation}
より、
\[
A^{-1}=V\Sigma^{-1}U*
\]
と逆行列演算が高速で安定する利点がある。

Having described the full SVD, we can now discard the simplifying assumption that A has full rank. if A is rank-deficient, the factorization \eqref{eq:FullSVD} is still appropriate.
行列$A$が横長でも式\eqref{eq:FullSVD}は成り立つ