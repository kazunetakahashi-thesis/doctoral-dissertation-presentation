# Hénon 型楕円型方程式

\[
  \begin{align}
    \left\{
    \begin{aligned}
      - \Delta u & = \lvert x \rvert^\alpha \lvert u \rvert^{p-2} u
                &                                                & \text{ in } \Omega,                          \\
      u          & = 0                                            &               & \text{ on } \partial \Omega.
    \end{aligned}
    \right.
  \end{align}
\]

## 基本的な定理

- [Ni '82] で $\Omega = B(0, 1)$ のとき， $2 \leq p < 2^*(\alpha) = 2(N + \alpha)/(N - 2)$ で球対称な正値解が存在することが示された．
  - 結局のところ $H_ {0, rad}^1 (B) \subset \subset L^{2^*(\alpha)}(B)$ の埋め込みがコンパクトであることが示された．ここで，$\Omega = B = B(0, 1)$, ただし測度に $\lvert x \rvert^\alpha$ の weight が付いているものとする．
- Pohozaev type の議論により， $\Omega$ が強星型のとき $p \geq 2^*(\alpha)$ のとき解は存在しない．
  - 評価の際 Bessel 関数が出てくる．

## 臨界 Sobolev 指数の場合

$p = 2^*$ の場合，一般の有界領域 $\Omega$ について， [Hirano '09] など，存在定理はある．

非存在定理は多分ない．その理由は，存在定理は Sobolev の意味での臨界指数以下 $p \leq 2^ *$ で出てくるが，非存在定理は Hénon の意味での臨界指数以上 $p \geq 2^ * (\alpha)$ で出てくるからであろうと思われる．

## 典型的な議論

私の好きな例ということで， [^1]を掲げる．

[^1]: M. Calanchi, S. Secchi and E. Terraneo, Multiple solutions for a Hénon-like equation on the annulus, J. Differential Equations, 245 (2008), 1507–1525.

\[
  \begin{align}
    \left\{
    \begin{aligned}
      - \Delta u & = \Psi_ \alpha u ^{p-1}
                &                                                & \text{ in } \Omega,                          \\
      u          & > 0                                            &               & \text{ in } \Omega, \\
      u          & = 0                                            &               & \text{ on } \partial \Omega.
    \end{aligned}
    \right. \tag{1}
  \end{align}
\]

ここで $N \geq 3$, $\Omega = \{ x \in \mathbb{R}^N \mid 1 < \lvert x \rvert < 3 \}$ は円環領域とし， $\Psi _\alpha(x) = \left \lvert \lvert x \rvert - 2 \right \rvert^ \alpha$ は Hénon 型とする． $2 < p < 2^*$ とする．

大きく $4$ つの解を，順次，条件をつけながら求める．

Hénon 型方程式の議論の多くは， Rayleigh 商を用いる． $u \in H_ 0^1(\Omega) \setminus \{ 0 \}$ に対し，
\[
  R_ {\alpha, p} (u) = \frac{\left\| Du \right\|_ {L^2(\Omega)}^2 }{
    \left\| \Psi_ \alpha^{1/p} u \right\|_ {L^p (\Omega)}^2
  }
\]
と定める．
\[
  \begin{align}
    S_ {\alpha, p}^{rad} &= \inf_ {u \in H_ {0, rad}^1(\Omega) \setminus \{ 0 \}} R_ {\alpha, p} (u), \\
    S_ {\alpha, p} &= \inf_ {u \in H_ {0}^1(\Omega) \setminus \{ 0 \}} R_ {\alpha, p} (u), \\
  \end{align}
\]

と定める．それぞれ $\inf$ を達成する $u$ があるとすれば，それは (1) の解である．

### 球対称解

まず $S^{rad}_ {\alpha, p}$ は必ず達成される． $0 \not \in \Omega$ より， $H_ {0, rad}^1(\Omega) \subset \subset L^q (\Omega)$ for $q \geq 1$ はコンパクトに埋め込まれているからである．

### 球対称でない解 その 1

$H_ {0}^1(\Omega) \subset \subset L^q (\Omega)$ for $1 \leq q < 2^*$ はコンパクトに埋め込まれているため，やはり $S_ {\alpha, p}$ は達成される．

$S_ {\alpha, p}$, $S_ {\alpha, p}^{rad}$ はそれぞれ $\alpha$ で適切に評価される．そこで $\alpha > 0$ を十分大きくすると， $S_ {\alpha, p} < S_ {\alpha, p}^{rad}$ が成立する．ゆえに球対称でない解が存在する．これを $u_ {\alpha, p}$ とおく．

### 球対称でない解 その 2

$p \to 2^*$ とする．すると[^2]により， $u_ {\alpha, p}$ は $\partial \Omega$ のある $1$ 点 $x_0$ に集積する．ところで $\partial \Omega = \{ \lvert x \rvert = 1 \} \cup \{ \lvert x \rvert = 3 \}$ であるので， $x_0$ はどちらか一方の連結成分の点である．そこである開集合 $A \subset H_ 0^1(\Omega)$ を構成し，
\[
  T_ {\alpha, p} = \inf_ {u \in A} R_ {\alpha, p}(u)
\]
の最小化点に近づく点列を，集積点が $x_0$ と *逆側の方の連結成分* なるように構成する．この極限として最小化点 $v_{\alpha, p}$ が存在し， $A$ の内部に存在することを示す．これが $u_ {\alpha, p}$ と別の解を与えており，しかも球対称ではない．

### 球対称でない解 その 3

$u_ {\alpha, p}$ と $v_{\alpha, p}$ を繋いで mountain pass theorem を使用すると，球対称ではない別の解が構成できる．

[^2]: D. Cao, S. Peng, The asymptotic behaviour of the ground state solutions for Hénon equation, J. Math. Anal. Appl. 278 (2003) 1–17.

