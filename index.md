
# 博士論文審査会

タイトル： **Hénon type elliptic equations with critical Sobolev growth** (臨界 Sobolev 指数を持つ Hénon 型楕円型方程式)

氏名： 高橋 和音 (Kazune Takahashi)

## 前提

- この審査会は、全て日本語で行う。
- 公開の審査会であるため、ノート記録、写真撮影、録音、動画撮影、動画配信等の記録行為は **一切制限しない** 。
  - ただし私の顔写真が公開の場に出るのはやめてください。
  - 他の方の権利も侵害しないでください。
- この文書は、審査会終了後インターネット上で公開する。
  - `https://github.com/kazunetakahashi-thesis/doctoral-dissertation-presentation`
  - 全てのコンテンツは白黒。強調は **太字** と *斜体* のみを使う。
  - 参考文献の正式名称は掲げないが、少なくとも博士論文の Bibliography には引いてある。 Bibliography はこの資料と同時に公開する。
- 博士論文をお読みくださった方に向けて発表を行う。
  - 種々の事情で論文に *書けなかった内容* を主に述べ、補足説明、意図の説明をする。

お断り：「指導教員、その他の人からの有効な示唆又は、助言を受けていれば、その主たるものについて」発表するように求められているが、一切ない。指導教員の宮本先生には論文を投稿する際にサポートいただいた。ゆえに、内容の全責任は私にある。全ての質問は私に聞くようにお願いしたい。

## 予備知識

時間が限られている上に、 **博士論文をお読みくださった審査の先生方に向けて発表する** ので、以下の予備知識は仮定する。

- [Brézis-Nirenberg '83] の結果を *自分で計算したことがある* 程度の知識を仮定する。
  - Mountain pass theorem without $(\text{PS})$ condition
  - $(\text{PS})_c$ 条件
  - Brézis-Nirenberg に出てくる Talenti 関数の積分の具体的な計算内容

審査の先生でない方へ： 私が **「ここは覚える」** と書いているところだけ覚えて進んでください。

## 記号

特に、流儀が異なりうる記号について規約する。

領域の次元は $N \geq 3$ とする。臨界 Sobolev 指数は $2^* = 2N/(N-2)$ で表す。

Talenti 関数 $U \colon \mathbb{R}^N \to \mathbb{R}$ を
\[
  U(x) = \frac{1}{\left( 1 + \lvert x \rvert^2 \right)^{(N - 2)/2}}
\]
と定める。 $\epsilon > 0$ の付き方は
\[
  u_\epsilon = \frac{\xi(x)}{\left( \epsilon + \lvert x \rvert^2 \right)^{(N - 2)/2}}
\]
の流儀を採用する。 Sobolev 定数は
\[
  S = \inf_{u \in H_0^1(\Omega), u \not\equiv 0} \frac{ \left\| Du
  \right\|_{L^2(\Omega)}^2}{\left\| u \right\|_{L^{2^*}(\Omega)}^2}
\]
で表す。 [Talenti '76] により、
\[
  S = \frac{ \left\| DU
  \right\|_{L^2(\mathbb{R}^N)}^2}{\left\| U \right\|_{L^{2^*}(\mathbb{R}^N)}^2}
\]
が成立する。すなわち Talenti 関数によって臨界 Sobolev 指数は達成される。

汎関数 $I \colon H_0^1(\Omega) \to \mathbb{R}$ について、 $H_0^1(\Omega)$ 上の点列 $\{ u_j \}$ が $I$ の $(\text{PS})_c$ 列であるとは、以下の条件を充たすことをいう。

1. $I(u_j) \to c$ as $j \to \infty$,
2. $I^\prime(u_j) \to 0$ in $H^{-1}(\Omega)$ as $j \to \infty$.

$I$ が $(\text{PS})_c$ 条件を充たすとは、 $I$ の任意の $(\text{PS})_c$ 列が precompact であることをいう。

## $O$ 記法について

### 本来の $O$ 記法

「上界」を表す記法である。

- 例えば $n$ 個の配列を merge sort する際の時間計算量は $O(n \log n)$ であるが、別にこれを $O(n^2)$ と言っても $O(2^n)$ と言っても、本来は間違いではない。上界を表す記号であるから。
  - 下界は $\Omega$ を使う。それらが一致する場合は $\Theta$ を用いるのが一般的である。

### この分野での $O$ 記法

$f(\epsilon) = O(g(\epsilon))$ as $\epsilon \to 0$ であるとは、 $C, C' > 0$ が存在して、小さな $\epsilon > 0$ に対し、
\[
  C g(\epsilon) \leq f(\epsilon) \leq C' g(\epsilon)
\]
が成立し、 $f, g$ は同じ極限(大抵 $0$ か$\infty$ )に達することをいう。

このように規約していることが、特に後半に重要になる。

## 領域

領域 $\Omega \subset \mathbb{R}^N$ は共通である。 Hénon 型を考察するために、以下の条件を置く。

- 境界は区分的 $C^1$ 級。
- 有界領域。特に単位球に部分集合として含まれる： $\Omega \subset B(0, 1)$.
  - $B(x, r) = \{ y \in \mathbb{R}^N \mid \lvert y - x \rvert < r \}$ は開球である。
- $x_0 = (1, 0, \dots, 0) \in \partial \Omega$ で内部球条件を充たす。

## 博士論文の構成

2 つの方程式を考察している。

- Chapter 3 で臨界 Sobolev 指数を持つ Hénon 方程式の解の存在を示した(Theorem 1.1.1)。
  - Chapter 2 で移動する Talenti 関数の積分の評価を正確に行った。 $N \geq 3$ で $\epsilon$-order を決定 or 残余項を評価した。
  - $\partial \Omega$ で項が消える非自明な例も含まれている(Corollary 1.1.3)。
- Chapter 4 で Kirchhoff 型に、その手法を適用した(Theorem 1.1.2)。
  - Chapter 2 の手法の汎用性の高さの証拠となった。
  - 応用する際に non-local term を拡張してから適用した。

## 復習：臨界 Sobolev 指数はなぜ興味深いか

### Sobolev 埋め込み

$u^{p - 1}$ の項が出てくる半線形楕円型方程式を変分法で取り扱う。

- $2 \leq p < 2^* $ の場合： $H_ 0^1(\Omega) \subset \subset L^p(\Omega)$ はコンパクトに埋め込まれている。
  - 解析が比較的容易。
- $p = 2^* $ の場合： $H_ 0^1(\Omega) \subset L^ {2^ *}(\Omega)$ はコンパクトに埋め込まれていない。
  - 変分法で解析はできるが、難しい。
  - 解析は汎関数の評価と $(\text{PS})_c$ 条件に持ち込まれる。
  - コンパクト性を破るのが Talenti 関数を絞る列。
- $p > 2^*$ の場合： $H_ 0^1(\Omega) \not\subset L^p(\Omega)$ はそもそも埋め込まれていない。
  - 変分法では解析は困難。

### 臨界 Sobolev 指数の解析はどうなるか

どの手法も、大体以下のような手順になる([Brézis-Nirenberg '83] 型の手法)。

- 方程式の解は、汎関数 $I$ の非自明な臨界点。
- $I$ の $(\text{PS}) _c$ 条件が成立するのは、例えば $0 < c < S^{N/2} / N$ になる。
  - Mountain pass theorem などにより、 $I$ の mountain pass level が $S^{N/2} / N$ 未満なら、非自明な臨界点が見つかる。
- $I$ の実際の mountain pass level を評価しようとすると、 Talenti 関数を絞ることになり、 $S^{N/2} / N + $ (残余項) の形になる。
  - 例えば (残余項) $\leq C \epsilon^\alpha - C' \epsilon^\beta$ のような形になる。
  - ゆえに $\alpha > \beta$ ならば、残余項が負になるので、解が存在することが示される。

ここだけ覚える：

- mountain pass level や $(\text{PS})_ c$ 条件は、 **定数部分は「正確な値」が必要** になる。
- Talenti 関数の積分に由来する **残余項の $\epsilon$-order が、解の存在に直結**する。

## Chapter 3: Hénon 型方程式

### 主定理

\[
  \begin{align}
    \left\{
      \begin{aligned}
        - \Delta u & = \lambda \Psi u + \lvert x \rvert^\alpha u^{2^*-1}
                  &                                                     & \text{ in } \Omega,                        \\
        u          & > 0                                                 &              & \text{ in } \Omega,         \\
        u          & = 0                                                 &              & \text{ on } \partial\Omega.
      \end{aligned}
    \right. \tag{1}
  \end{align}
\]

定数 $\lambda$ は $\lambda < \lambda_1$ を充たすものとする．ここで $\lambda_1$ は，次の Dirichlet 固有値問題の第 $1$ 固有値とする： $-\Delta \phi = \lambda \Psi \phi \text{ in } \Omega$. また， $\alpha > 0$ とする．

関数 $\Psi \in L^\infty(\Omega) \setminus \{ 0 \}$ について，以下の条件を導入する．

- **(T1)**: $m > 0$, $\beta \geq 0$ 及び開球 $B \subset \Omega$ が存在し，$x_0 \in \partial \Omega$ 及び $\Psi \geq \Psi_0 \text{ in } \Omega$ が成立する．ここで， $\Psi_0$ は以下で定める．
\[
  \Psi_0(x) =
  \begin{cases}
    m \left\lvert x - x_0 \right\rvert^\beta
    & x \in B, \\
    0 & x \not\in B.
  \end{cases}
\]

> **Theorem 1.1.1**: $N \geq 4$, $0 < \lambda < \lambda_1$ とする．$\Psi \in L^\infty(\Omega) \setminus \{ 0 \}$ は $0 \leq \Psi \leq 1 \text{ in } \Omega$ を充たすものとする． (T1) を仮定する．このとき，十分小さな $\alpha > 0$ に対し，方程式 (1) は解 $u \in H_0^1(\Omega)$ を持つ．

## Hénon 方程式の先行研究

### Hénon 方程式

\[
  \begin{align}
    \left\{
    \begin{aligned}
      - \Delta u & = \lvert x \rvert^\alpha \lvert u \rvert^{p-2} u
                &                                                & \text{ in } B(0, 1),                          \\
      u          & = 0                                            &               & \text{ on } \partial B(0, 1).
    \end{aligned}
    \right.
  \end{align}
\]

- [Hénon '73] で $N = 1$ で、 $u$ に絶対値がついた方程式を数値解析しているのが興りである。
- [Ni '82] で、 $2 \leq p < 2^*(\alpha) = 2(N + \alpha)/(N - 2)$ で球対称な正値解が存在することが示された。
- 我々の (1) は Hénon 方程式と Brézis-Nirenberg 問題を合わせたものである。

### 直接の先行研究

先行研究は 2 件しかない。

\[
\begin{align}
  \left\{
  \begin{aligned}
    - \Delta u       & = \lambda u + \lvert x \rvert^\alpha \lvert u
    \rvert^{2^*-2} u &                                               & \text{ in } \Omega,                         \\
    u                & = 0                                           &              & \text{ on } \partial \Omega.
  \end{aligned}
  \right. \tag{2}
\end{align}
\]

$\alpha > 0$, $\lambda > \lambda_1'$ は定数である．ここで $\lambda_1'$ は，次の Dirichlet 固有値問題の第 $1$ 固有値とする：$-\Delta \phi = \lambda \phi \text{ in } \Omega$. ここで sign-changing solution の存在が、それぞれ以下の条件で示されている。

- [Long-Yang '12]: $N \geq 7$ 、 $\partial \Omega$ が滑らか。
- [Secchi '12]: $N \geq 5$ 、 $\Omega = B(0, 1)$ 。

我々は、 $0 < \lambda < \lambda _1$ の時に、 $N \geq 4$ で正値解の存在を示す。 $\Psi$ は関数で、 $\Omega$ はより一般的である。

## 臨界 Sobolev 指数を持つ Hénon 型方程式はなぜ困難か

以下の、 **太字の部分は覚える** 。

- 臨界 Sobolev 指数を持つ場合、 [Brézis-Nirenberg '83] の手法が有効であるが、 Talenti 関数を $u^{2^* - 1}$ の係数の関数の **最大値を取る部分を中心に絞る** 必要がある。
  - 例えば私の修士論文は、それをやっている。
  - 係数が定数の場合、これは関係ないから、大抵 $0$ を中心に絞る。
- ところが Hénon 型の場合、 $\lvert x \rvert^\alpha$ は $\Omega$ 上 **最大値を取らない** 。$x_0$ に近づくと $\sup_{x \in \Omega} \lvert x \rvert^\alpha = 1$ に近づく。
  - **新たな Talenti 関数の積分の評価が必要** になる。
    - [Brézis-Nirenberg '83] と計算が違う。 *既存の論文の引用では済まされない* 。
  - その「影響」をどこまで抑え込めるかが焦点となる。

## Chapter 2: 移動する Talenti 関数 $u_{\epsilon, l}$

\[
  \begin{align}
    u_{\epsilon, l}(x) &= \frac{\xi_l(x)}{\left( \epsilon + \left\lvert x - x_l \right\rvert^2 \right)^{(N - 2)/2}}, \\
    v_{\epsilon, l}(x) &= \frac{u_{\epsilon, l}(x)}{\left\| \lvert x \rvert^{\alpha/2^*} u_{\epsilon, l} \right\|_{L^{2^*(\Omega)}}}.
  \end{align}
\]

- $\epsilon > 0$, $0 < l < 1$.
- $x_l = (1 - l, 0, \dots, 0) \in \mathbb{R}^N$.
- $\{ \xi_l \}_{0 < l < 1} \subset C^\infty_c (\Omega)$ はいくつかの条件を充たすカットオフ関数。

以下では $l = l(\epsilon)$ は $\epsilon > 0$ の関数と見る。 $\epsilon \leq l$ と、 $l \to 0$ as $\epsilon \to 0$ を充たすものとする。

### 評価について

以下、積分の評価を述べる。複雑なので **眺めるだけで良い** 。ポイントを口頭で概説する。

> **Lemma 2.2.1**： $C_1, C_2, C > 0$ が存在し、小さい $\epsilon > 0$ に対し次式が成立する。
> \[
>   \begin{multline}
>     \left\| DU \right\|_{L^2(\mathbb{R}^N)}^2 \epsilon^{-(N-2)/2} - C_1
>     l^{-(N-2)} \\ \leq
>     \left\| Du_{\epsilon, l} \right\|_{L^2(\Omega)}^2 \\
>     \leq
>     \left\| DU \right\|_{L^2(\mathbb{R}^N)}^2 \epsilon^{-(N-2)/2} + C_2
>     l^{-(N-2)},
>   \end{multline}
> \]
> \[
>   \begin{multline}
>    (1 - 2l)^ {2\alpha/2^ *} \left( \left\| U
>     \right\|^ {2^ *}_{L^ {2^ *}(\mathbb{R}^N)}\epsilon^{-N/2} - Cl^{-N}
>     \right)^{2/2^*} \\ \leq
>     \left\|
>     \left\lvert x \right\rvert^{\alpha/2^*} u_{\epsilon, l
>       }\right\|_{L^{2^*}(\Omega)}^2
>     \leq \left\| U
>    \right\|^{2}_{L^{2^*}(\mathbb{R}^N)}\epsilon^{-(N-2)/2}.
>   \end{multline}
> \]

## $l(\epsilon) = \epsilon^\gamma$ について

$\sqrt{\epsilon}$ に「追いつかない」ようにしなくてはならないので、 $0 < \gamma < 1/2$ である。

[Long-Yang '12], [Secchi '12] は $\gamma$ を固定している。我々は、 $\Psi$ が $\partial \Omega$ で消える可能性があるので、 $0 < \gamma < 1/2$ を *選ぶ* 必要がある。

> **Corollary 2.2.6**： $0 < \gamma < 1/2$ とし、 $l = l(\epsilon) = \epsilon^\gamma$ とする。このとき、 $\epsilon \to 0$ のとき次式が成立する。
> \[
>     \int_\Omega \Psi_0 u_{\epsilon, l}^2 dx
>     = \begin{cases}
>       O(\epsilon^{\beta\gamma-(N-4)/2})                    & N \geq 5, \\
>       O(\epsilon^{\beta\gamma}\lvert \log \epsilon \rvert) & N = 4,    \\
>       O(\epsilon^{(\beta + 1)\gamma})                      & N = 3.
>     \end{cases}
> \]

(残余項) $< 0$ は以下と同値になる。

\[
  \left( S - S (1 - 2l)^ {2\alpha/2^ *} \right) + \left( C \epsilon^{(N-2)(1/2 - \gamma)} - C' \epsilon^{(\beta \gamma + 1)} \right) < 0. \tag{3}
\]

2 項目が負になるような $\epsilon > 0$ が存在するための条件は、

\[
  \gamma < \frac{N-4}{2(\beta + N - 2)}.
\]

これを充たす $0 < \gamma < 1/2$ は、 $N \geq 5$ のとき存在する。よって 2 項目を負にする $\epsilon > 0$ が得られる。それを固定して $\alpha > 0$ を小さくすれば、 (3) は達成される。よって解が得られる。

$N = 4$ の場合： $l(\epsilon) = \lvert \log \epsilon \rvert^{-k}$ ($k > 0$) とすると、[同様に解が得られる](log.html)。

## Chapter 2: $u_{\epsilon, l}$ の評価手法の適用範囲と限界

臨界 Sobolev 指数を持つ方程式を Hénon 型に拡張する際に使える。

既存の臨界 Sobolev 指数を持つ方程式の結果のうち、

- 指数の比べ合いになるもの(例： $C\epsilon^\alpha - C'\epsilon^\beta < 0$ の型)は **ほぼそのまま存在定理が出てくる** と見込まれる。
  - たとえ $\lvert \log \epsilon \rvert$ の差しかなくても、勝てる。
    - Brézis-Nirenberg の $N = 4$ で今回勝った。
  - 将来、 *これ以上強い結果を得る必要がない* と思われる。
- 一方で、指数が一致していて係数の比べ合いになる場合(例： $(A - A') \epsilon^\alpha < 0$ の型)は、 **必ず負ける** 。
  - Brézis-Nirenberg の $N = 3$ がその例。今回は存在定理が出てこなかった。
    - しかし少し工夫した方程式になると、すぐにこの場合は存在定理が出なくなる傾向にある。だから *適用範囲に改めて大きな制約を与えた訳ではない* 。

## (T1) について

> - **(T1)**: $m > 0$, $\beta \geq 0$ 及び開球 $B \subset \Omega$ が存在し，$x_0 \in \partial \Omega$ 及び $\Psi \geq \Psi_0 \text{ in } \Omega$ が成立する．ここで， $\Psi_0$ は以下で定める．
> \[
>   \Psi_0(x) =
>   \begin{cases}
>     m \left\lvert x - x_0 \right\rvert^\beta
>     & x \in B, \\
>     0 & x \not\in B.
>   \end{cases}
> \]

### $\Psi$ が境界で消える非自明な例

$\beta_0 > 0$, $\Omega = B(0, 1)$, $\Psi(x) = (1 - \lvert x \rvert)^{\beta_0}$ が、 (T1) を充たす。この例では $\Psi$ が境界で消える。

証明は、 2 次元平面に射影し、初等幾何を用いる。 $B$ の直径を $1$ 未満とし、 $\beta = 2 \beta_0$ とし、 $m > 0$ を小さくする。

## Chapter 4: Kirchhoff 型方程式

\[
  \begin{align}
    \left\{
    \begin{aligned}
      - \left( a + b \left( \int_\Omega \lvert Du \rvert^2 dx \right)^{(p-2)/2} \right) \Delta u &= \Psi u^{q-1} + \lvert x \rvert^\alpha u^{2^* - 1}
                &                                                     & \text{ in } \Omega,                        \\
      u          & > 0                                                 &              & \text{ in } \Omega,         \\
      u          & = 0                                                 &              & \text{ on } \partial\Omega.
    \end{aligned}
    \right.
  \end{align} \tag{4}
\]

- $\alpha \geq 0$, $p > 2$, $q \geq 2$ は定数。
- $a \geq 0$ と $b \geq 0$ は $a + b > 0$ を充たす定数。

Kirchhoff-Hénon 型方程式と呼ぶことにした。

### 主定理

> **Theorem 1.1.2**: $2 < p < q < 2^*$ を仮定する。 $\Psi \in L^\infty(\Omega) \setminus \{ 0 \}$ は ある定数 $\kappa > 0$ が存在し $0 \leq \Psi \leq \kappa \text{ in } \Omega$ を充たすとする。次の (1), (2) のいずれかの成立を仮定する。<br>(1) $N = 3$ and $4 < q < 2^* = 6$,<br>(2) $N \geq 4$.
>
> 1. $\alpha = 0$ の場合： $\Psi \geq \kappa_0 \text{ in } \omega$ を充たす開集合 $\omega \subset \Omega$ と $\kappa_0 > 0$ が存在すると仮定する。このとき、方程式 (4) は解 $u \in H_0^1(\Omega)$ を持つ。
> 2. $\alpha > 0$ の場合： 前述の (T1) を仮定する。このとき，十分小さな $\alpha > 0$ に対し，方程式 (4) は解 $u \in H_0^1(\Omega)$ を持つ．

主な定理は 2. の $\alpha > 0$ の場合であり、以下これを議論する。前項の知見を用いて、これを導く。

## Kirchhoff 型方程式の先行研究

前提：先行研究は全て $\alpha = 0$ である。つまり Hénon 型ではない。

Kirchhoff 方程式は、もともと時間発展する方程式。電磁気学と関係する。 $p = 4$ とした

\[
  -\left( a + b \left( \int_\Omega \lvert Du \rvert^2 dx \right) \right) \Delta u = f(u)
\]

の型の方程式を *Kirchhoff 型の楕円型方程式* という。この場合、対応する汎関数は

\[
  I(u) = \frac{a}{2} \left\| Du \right\|_ {L^ 2(\Omega)}^ 2 + \frac{b}{4} \left\| Du \right\|_ {L^ 2(\Omega)}^ 4 - F(u)
\]

の型になるが、真ん中の項(に由来する元の方程式の項)を *non-local term* という。

### 変分法的研究の興り

- [Ma-Rivera '03] が Kirchhoff 型の楕円型方程式に変分法を導入した。
- [Alves-Corrêa-Ma '05] が truncated method を導入した。

### 臨界 Sobolev 指数を持つ場合

ここは覚える： 臨界 Sobolev 指数を持つ Kirchhoff 型方程式は、 **次元によって手法が異なる** 。その根本的な理由は、 $p = 4$ と $2^* = 2N/(N - 2)$ の大小関係が、次元によって異なるからである。

\[
  p = 4
  \begin{cases}
    < 2^* = 6 & N = 3, \\
    = 2^* = 4 & N = 4, \\
    > 2^* & N \geq 5.
  \end{cases}
\]

- $N = 3$ の場合
  - $4 < q < 2^* = 6$ の場合： [Naimen '14 NoDEA] で $\lambda > 0$ に対して解が存在することが示されている。
    - 今回我々が参考にする手法。
  - $2 < q < 4$ の場合： [Figueiredo '13], [Naimen '14 NoDEA] で、ある $\lambda^ * \geq 0$ が存在し、 $\lambda > \lambda^*$ に対して解が存在することが示されている。
    - それぞれ異なる truncated method が使われている。
  - $q = 2$ は[複雑な結果が出ている](q_2.html)。
- $N = 4$ の場合
  - [Naimen '14 JDE] が[最初である](n_4.html)。特に活発に研究がされている。
- $N = 5$ の場合
  - 最近いくつか存在定理が出ていると見られる。

## 問題点

$N = 3$, $4 < q < 6$ の場合に、私が適用したい手法がある。しかし、できれば $N \geq 3$ で結果を得たい。どうするか。

### non-local term を拡張

そこで $4$ のところを $p$ として、動かすことにした。 $N = 3$, $4 < q < 6$ の場合は、 $N \geq 3$, $2 < p < q < 2^*$ の場合に対応する。つまり定理の仮定が出てくる。

## 次の問題点

途中で、次の方程式の正の解が必要になる。

\[
  \left( a + b \eta^{(p-2)/2} \right) \eta - \left( \frac{\eta}{S} \right)^{2^*/2} = 0. \tag{5}
\]

この方程式は [explicitly に解けない](explicitly.html)。解けないと「mountain pass level や $(\text{PS})_ c$ 条件は、 **定数部分は『正確な値』が必要** になる」の部分で非常に困る。

解けない方程式の解に関連する道具の解析的性質を、導く必要がある。

## 根に記号を置く

(5) の唯一の正値解を $\eta _0$ とおく。

- $(\text{PS})_c$ 条件が成立する上界 $c$ を求める。
- $\sup_{t > 0} I(t v_\epsilon)$ の計算をし、 $I$ の mountain pass level を評価する。

どちらも成功した。後者をここでは取り上げる。

## 鍵となる補題

$v _{\epsilon} = v _{\epsilon, l}$ とする。
\[
  A_\epsilon = \int_\Omega \lvert Dv_\epsilon \rvert^2 dx
\]
と定める。また、 $T _\epsilon > 0$ を次式を充たす唯一の正値とする。
\[
  a A_\epsilon + b A_\epsilon^{p/2} T_\epsilon^{p - 2} - T_\epsilon^{2^* - 2} = 0. \tag{6}
\]
この $T _\epsilon$ は $\sup _{t > 0} I(t v _\epsilon)$ を評価する際に情報が必要となる値である。

> **Lemma 4.2.2**: 次式が成立する。
> \[
>   \lim_{\epsilon \to 0} T_ \epsilon^2 A_ \epsilon = \eta_0. \tag{7}
> \]
> 特に、
> \[
>   T_ \epsilon^2 A_ \epsilon - \eta_ 0 = O\left( A_ \epsilon - S \right) \tag{8}
> \]
> as $\epsilon \to 0$ が成立する。

- 「よくわからないもの $T_ \epsilon^2 A_ \epsilon$」が「よくわからないもの $\eta_0$」に収束する。
- それどころか、「よくわからない order $O(T_ \epsilon^2 A_ \epsilon - \eta_ 0)$」が「よく *わかる* order $O(A_ \epsilon - S)$」に一致している。
  - 十分な情報が引き出せている。

### 証明の概略

$t \geq 0$ に対し、
\[
  g(t) = at + b t^{p/2} - \frac{1}{S ^ {2 ^ * /2}} t ^ {2 ^ * /2}
\]
とする。まず $\lim_{\epsilon \to 0} g(T_ \epsilon ^2 A_ \epsilon) = 0$ が示される。

この段落は黒板で説明する： $g(t) = 0$ が $t = 0, \eta _0$ が同値であることに気をつけて、 $T _\epsilon ^2 A _\epsilon$ の下界の評価を経ると (7) が得られる。

(5), (6) より、
\[
\begin{multline}
  a \left( T_\epsilon^2 A_\epsilon - \eta_0 \right)
  +b \left( \left(T_\epsilon^2 A_\epsilon \right)^{p/2}
  -\eta_0^{p/2} \right) \\
  -\frac{1}{S^{2^* /2}}
  \left( \left(T_\epsilon^2 A_\epsilon \right)^{2^* /2}
  -\eta_0^{2^* /2} \right) \\
  = \frac{1}{S^{2^* /2}} \left( S^{2^* /2} - A_\epsilon^{2^* /2} \right)
  T_\epsilon^{2^*}.
\end{multline}
\]
が得られるが、左辺は全ての項が $O(T _\epsilon^2 A _\epsilon)$ 、右辺は $O(A _\epsilon - S)$ である。さらに $g(T _\epsilon^2 A _\epsilon) < 0$ であることも鑑みると、 $T _\epsilon^2 A _\epsilon > 0$ もわかる。よって (8) が得られる。

### 補足

実は、このような手法は、よく調べると [Zeng-Tang '16] で導入されていた。こちらは $\alpha = 0$, $a > 0$ に止まっている。しかし私は [Naimen '14 NoDEA] の[直接拡張に成功した](ps_c.html)ので、 $a = 0$, $b > 0$ の場合が含まれている。これは Hénon 型 $\alpha > 0$ との相性も良い。

## 「研究の意義と将来の目標に関する見解について」

### 研究の意義

- 移動する Talenti 関数の積分の評価を正確に行った。 $N \geq 3$ で $\epsilon$-order を決定 or 残余項の評価に成功した。
  - 結果も、強い。存在条件をほとんど損わない。
- その手法が、単純な方程式だから適用できたわけではなく、他の方程式にも広く応用可能であることを示唆した。
  - その例として Kirchhoff 型に適用した。

### 将来の目標

- Mountain pass theorem を用いて他の方程式にも結果が出そう。
  - 今やっている。
- 他の変分法の手法とも相性が良いことが示唆される。
  - Linking を適用、 Nehari manifold の詳しい解析、 Struwe の方法など。
    - 例えば Kirchhoff 型は複数の既存の結果があるので、それらを「 Hénon 化」するのもうまくいくだろう。
  - 人によって得意な手法が異なる。私 1 人では全部はできないだろう。手法が広がっていってほしい。