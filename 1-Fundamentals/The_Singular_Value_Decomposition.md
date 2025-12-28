(全体:2025/12/21)
## Reduced SVD
Aはfull rank nでVはunitayであるため、 $V^{-1}=V^*$ 、$\hat{U}$ は $m\times n$ の直交行列、 $\hat{\Sigma}$ は正方行列とする。

$$A=\hat{U}\hat{\Sigma}V^*$$

This factorization of A is called a **reduced singular value decomposition**, or **reduced SVD**, of A. Schematically, it looks likes this:
<p align="center">
    <img width="716" src="https://github.com/user-attachments/assets/3447684b-556f-4e75-97f0-782fb9850418" />
</p>

## Full SVD
$\hat{U}$ is not unitary. However, by adjoining an additional $m-n$ orthonormal columns to $\hat{U}$ can be extended to a unitary matrix $U$.

If $\hat{U}$ is replaced by $U$ , then $\hat{\Sigma}$ will have to change too. the last $m-n$ columns of $U$ should be multiplied by zero.
<p align="center">
   <img width="656" src="https://github.com/user-attachments/assets/d0904e35-3a6b-4a58-afb6-5dc8d8a2f338" />
</p>

 $U$ と $V$ はユニタリー行列となるから、

$$
\begin{equation}
A=U\Sigma V^* 
\end{equation}$$

より、

$$
A^{-1}=V\Sigma^{-1}U^*
$$

と逆行列演算が高速で安定する利点がある。

Having described the full SVD, we can now discard the simplifying assumption that A has full rank. if A is rank-deficient, the factorization 式(1) is still appropriate.
行列 $A$ が横長でも式(1)は成り立つ
