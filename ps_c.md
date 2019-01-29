# Concentration compactness について

## Sobolev 埋め込み

> - $p = 2^* $ の場合： $H_ 0^1(\Omega) \subset L^ {2^ *}(\Omega)$ はコンパクトに埋め込まれていない。
>   - 変分法で解析はできるが、難しい。
>   - 解析は汎関数の評価と $(\text{PS})_c$ 条件に持ち込まれる。
>   - コンパクト性を破るのが Talenti 関数を絞る列。

どのくらいコンパクトに埋め込まれていないか？ 有界列 $\{ u _j \}$ in $H _0^1(\Omega)$ を持ってきたときに、何が言えるか？

誤解を恐れずに言えば、 **ほとんどが precompact** in $L^ {2^ *}(\Omega)$ である。ただそのうち例外があって、それは **事実上、 Talenti 関数を絞る列** しかない。

\[
  u_ \epsilon = \frac{\xi(x)}{\left( \epsilon + \lvert x \rvert^2 \right)^{(N - 2)/2}}
\]

「事実上」と書いたのは、中心は $\overline{\Omega}$ 上のどこでもいいし、可算無限個までは絞る中心があってもいいからである。

この部分を定式化する方法は、大きく分けて、 Lions の補題と Struwe の方法がある。

## The second concentration compactness lemma by Lions

[Lions '85] による。定式化すると長くて却ってわかりづらいので、エッセンスだけ記す。

The second concentration compactness lemma は *関数空間に対する定理* である。その結論は、上の $\{ u_ j \}$ は $L^ {2^ *}(\Omega)$ 上 precompact であるか、もしそうでなければ、$u \in H_0^1(\Omega)$ $\mathcal{J} \neq \emptyset$ が存在し、
\[
\begin{align}
  \left\{
  \begin{aligned}
    \lvert Du_j \rvert^2 \rightharpoonup & d\eta
    \geq \lvert Du \rvert^2 + \sum_{k \in \mathcal{J}}
    \eta_k \delta_{x_k},     \\
    (u_j)_+^{2^*} \rightharpoonup & d\nu
    = (u_+)^{2^*} + \sum_{k \in \mathcal{J}}
    \nu_k \delta_{x_k}
  \end{aligned}
  \right. \tag{1}
\end{align}
\]
と書ける測度に弱測度収束する。 $\eta _k$ と $\nu _k$ の間には $\eta _k \geq S \nu _k^{2/2^*}$ という関係式がある。

## 拡張の方法

本論文の Chapter 4 では [Naimen '14 NoDEA] の直接の拡張に成功している。その概略を述べる。

$(\text{PS})_ c$ 条件の上界を求める際に the second concentration compactness lemma を用いている。背理法を使う。「$\{ u_ j \}$ は、示したい上界未満の $(\text{PS})_ c$ 列であるのに precompact でない」と仮定し (1) を用いる。すると、 [Naimen '14 NoDEA] は
\[
  0 \geq (a + b \eta_ k) \eta_ k - \nu_ k \tag{2}
\]
が出てくる。 $\eta _k \geq S \nu _k^{2/2^*}$ を用いて、 (2) からそれぞれ、
\[
  \begin{align}
    0 &\geq \left(a + b \eta_ k \right) \eta_ k - \left( \frac{\eta _k}{S} \right)^3, \\
    0 &\geq \left( a + b S \nu_ k ^{1/3} \right) S \nu_ k ^{1/3} - \nu _k
  \end{align}
\]
としている。これらを **それぞれ** 直接解いている。その後 $c$ を評価して、矛盾を導く。

我々の場合、 (2) に相当するものは
\[
  0 \leq \left( a + b \eta_k^{(p - 2)/2} \right) \eta_k - \lvert x_k \rvert^\alpha \nu_k \tag{3}
\]
である。まずここに Henon 型との相性の良さが出ている。

直接解くことはできない。そこでまず $\lvert x_ k \rvert \leq 1$ と $\eta_ k \geq S \nu_ k^{2/2^*}$ を用いて $\eta_ k \geq \eta_ 0$ であることを導く。その後 $c$ を評価する際に、 (3) を用いて **$\lvert x_k \rvert^\alpha \nu_k$ の項を消去** する。矛盾を導く。

以上により、 $a \geq 0$, $b \geq 0$, $a + b > 0$ という条件を損なわずに、議論を拡張することができた。