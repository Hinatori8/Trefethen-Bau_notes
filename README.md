# Numerical Linear Algebra Notes

Lloyd N. Trefethen & David Bau, III
『NUMERICAL LINEAR ALGEBRA』

<p align="center">
  <img width="200" src="https://github.com/user-attachments/assets/ae9bf857-3cda-4cf6-9817-c0bd7da4823d" />
</p>

## 目的

- 書籍内容の整理と理解

Strangの本のQR分解からがとても面白く、大学で履修した「数値解析」が面白かったので、この本を読むことにしました。この本はQR分解、SVD、Gram-Schmidtだけでなく、反復法も解説しているので、自分の興味に合う気がします。

## 方針

- 読んだ内容を自分の言葉に変換して丁寧に読んでいこうと思います。

---

## 前提知識

Gilbert Strang 著の和訳版『STRANG：線形代数イントロダクション』を主要教材として学習していた。第1〜6, 8, 9章は納得するまで繰り返し読み、他の章はサッと目を通した程度です。

<p align="center">
  <img width="200" src="https://github.com/user-attachments/assets/9fbc29a1-2e9b-48c3-ba34-d05e47589e0c" />
</p>

<details>
<summary>『STRANG：線形代数イントロダクション』章立て</summary>

1. ベクトル入門
2. 線型方程式の求解
3. ベクトル空間と部分空間
4. 直交性
5. 行列式
6. 固有値と固有ベクトル
7. 線形変換
8. 応用
9. 数値線形代数学
10. 複素ベクトルと行列

</details>

※ 書籍のPDF版は大学が無料で公開しています。
<https://www.stat.uchicago.edu/~lekheng/courses/309/books/Trefethen-Bau.pdf>

---

## 本書の構成（Lecture）

本書は40の「Lecture」を6つのPartにまとめた構成。

### Part I　Fundamentals（基礎）

<details>
<summary><b>Lecture 1〜5</b></summary>

- 1. Matrix-Vector Multiplication（行列ベクトル積）
- 2. Orthogonal Vectors and Matrices（直交ベクトルと直交行列）
- 3. Norms（ノルム）
- 4. The Singular Value Decomposition（特異値分解）
- 5. More on the SVD（SVDの補足）

</details>

### Part II　QR Factorization and Least Squares（QR分解と最小二乗法）

<details>
<summary><b>Lecture 6〜11</b></summary>

- 6. Projectors（射影子）
- 7. QR Factorization（QR分解）
- 8. Gram–Schmidt Orthogonalization（グラム・シュミット直交化）
- 9. MATLAB
- 10. Householder Triangularization（ハウスホルダー三角化）
- 11. Least Squares Problems（最小二乗問題）

</details>

### Part III　Conditioning and Stability（条件数と安定性）

<details>
<summary><b>Lecture 12〜17</b></summary>

- 12. Conditioning and Condition Numbers（条件付けと条件数）
- 13. Floating Point Arithmetic（浮動小数点演算）
- 14. Stability（安定性）
- 15. More on Stability（安定性の補足）
- 16. Stability of Householder Triangularization（ハウスホルダー三角化の安定性）
- 17. Stability of Back Substitution（後退代入の安定性）

</details>

### Part IV　Systems of Equations（連立方程式）

<details>
<summary><b>Lecture 18〜23</b></summary>

- 18. Conditioning of Least Squares Problems（最小二乗問題の条件付け）
- 19. Stability of Least Squares Algorithms（最小二乗アルゴリズムの安定性）
- 20. Gaussian Elimination（ガウスの消去法）
- 21. Pivoting（ピボッティング）
- 22. Stability of Gaussian Elimination（ガウス消去法の安定性）
- 23. Cholesky Factorization（コレスキー分解）

</details>

### Part V　Eigenvalues（固有値）

<details>
<summary><b>Lecture 24〜31</b></summary>

- 24. Eigenvalue Problems（固有値問題）
- 25. Overview of Eigenvalue Algorithms（固有値アルゴリズム概観）
- 26. Reduction to Hessenberg or Tridiagonal Form（ヘッセンベルク／三重対角化）
- 27. Rayleigh Quotient, Inverse Iteration（レイリー商・逆反復法）
- 28. QR Algorithm without Shifts（シフトなしQRアルゴリズム）
- 29. QR Algorithm with Shifts（シフト付きQRアルゴリズム）
- 30. Other Eigenvalue Algorithms（その他の固有値アルゴリズム）
- 31. Computing the SVD（SVDの計算）

</details>

### Part VI　Iterative Methods（反復法）

<details>
<summary><b>Lecture 32〜40</b></summary>

- 32. Overview of Iterative Methods（反復法概観）
- 33. The Arnoldi Iteration（アーノルディ反復）
- 34. How Arnoldi Locates Eigenvalues（アーノルディと固有値）
- 35. GMRES
- 36. The Lanczos Iteration（ランチョス反復）
- 37. From Lanczos to Gauss Quadrature（ランチョスからガウス求積へ）
- 38. Conjugate Gradients（共役勾配法）
- 39. Biorthogonalization Methods（双直交化法）
- 40. Preconditioning（前処理）

</details>

---

## 進捗

| Part | Lecture | 状態 |
|------|---------|------|
| I. Fundamentals | 1〜5 | ⬜ |
| II. QR & Least Squares | 6〜11 | ⬜ |
| III. Conditioning & Stability | 12〜17 | ⬜ |
| IV. Systems of Equations | 18〜23 | ⬜ |
| V. Eigenvalues | 24〜31 | ⬜ |
| VI. Iterative Methods | 32〜40 | ⬜ |
