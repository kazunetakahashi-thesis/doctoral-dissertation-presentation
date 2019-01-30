# Brézis-Nirenberg 型の予備知識

## 定理

\[
  \begin{align}
    \left\{
      \begin{aligned}
        - \Delta u & = \lambda u + u^{2^*-1}
                  &                                                     & \text{ in } \Omega,                        \\
        u          & > 0                                                 &              & \text{ in } \Omega,         \\
        u          & = 0                                                 &              & \text{ on } \partial\Omega.
      \end{aligned}
    \right. \tag{1}
  \end{align}
\]

> **定理** [Brézis-Nirenberg '83]:
> 1. $N \geq 4$ とする． (1) が解を持つ必要十分条件は $0 < \lambda < \lambda_ 1'$ である．
> 2. $N = 3$, $\Omega$ は球とする． (1) が解を持つ必要十分条件は $\lambda_ 1'/4 < \lambda < \lambda_ 1'$ である．

非存在定理は Pohozaev の議論に依る．

## 大まかな議論の流れ

存在を示す部分は，どの場合も以下の流れになる．

- 方程式の解は，汎関数 $I$ の非自明な臨界点．
- $I$ の $(\text{PS}) _c$ 条件が成立するのは，例えば $0 < c < S^{N/2} / N$ になる．ここで変分法の定理を適用するのを試みる．
  - Mountain pass theorem などにより， $I$ の mountain pass level が $S^{N/2} / N$ 未満なら，非自明な臨界点が見つかる．
- $I$ の実際の mountain pass level を評価しようとすると， $\sup_ {t > 0} I(t v_ \epsilon)$ を計算することになる． Talenti 関数を絞ることになり， $S^{N/2} / N + $ (残余項) の形になる．
  - 例えば (残余項) $\leq C \epsilon^\alpha - C' \epsilon^\beta$ のような形になる．
  - ゆえに $\alpha > \beta$ ならば，残余項が負になるので，解が存在することが示される．
