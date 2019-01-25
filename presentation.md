
# 博士論文審査会

タイトル：

高橋 和音 (Kazune Takahashi)

## 前提

- この審査会は、全て日本語で行う。
- 公開の審査会であるため、ノート記録、写真撮影、録音、動画撮影、動画配信等の記録行為は **一切制限しない** 。
  - ただし私の顔写真が公開の場に出るのはやめてください。
  - 他の方の権利も侵害しないでください。
- この文書は、審査会終了後インターネット上で公開する。
  - 全てのコンテンツは白黒。強調は **太字** と *斜体* のみを使う。
  - 参考文献の正式名称は掲げないが、少なくとも博士論文の Reference には引いてある。 Reference はこの資料と同時に公開する。
- 博士論文をお読みくださった方に向けて発表を行う。
  - 種々の事情で論文に *書けなかった内容* を主に述べ、補足説明、意図の説明をする。

お断り：「指導教員、その他の人からの有効な示唆又は、助言を受けていれば、その主たるものについて」発表するように求められているが、一切ない。指導教員の宮本先生には論文を投稿する際にサポートいただいた。ゆえに、内容の全責任は私にある。全ての質問は私に聞くようにお願いしたい。

## 予備知識

時間が限られている上に、 **博士論文をお読みくださった審査の先生方に向けて発表する** ので、以下の予備知識は仮定する。

- [Brezis-Nirenberg '83] の結果を *自分で計算したことがある* 程度の知識を仮定する。
  - Mountain pass theorem without $(\text{PS})$ condition
  - $(\text{PS})_c$ 条件
  - Brezis-Nirenberg に出てくる Talenti 関数の積分の具体的な計算内容

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

$H_0^1(\Omega)$ 上の点列 $\{ u_j \}$ が $I$ の $(\text{PS})_c$ 列であるとは、以下の条件を充たすことをいう。

1. $I(u_j) \to c$ as $j \to \infty$,
2. $I^\prime(u_j) \to 0$ in $H^{-1}(\Omega)$ as $j \to \infty$.

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
が成立し、 $f, g$ は同じ極限(大抵 $0$ か $\infty$ )に達することをいう。

このように規約していることが、特に後半に重要になる。

## 領域

領域 $\Omega \subset \mathbb{R}^N$ は共通である。 Henon 型を考察するために、以下の条件を置く。

- 境界は区分的 $C^1$ 級。
- 有界領域。特に単位球に部分集合として含まれる： $\Omega \subset B(0, 1)$.
  - $B(x, r) = \{ y \in \mathbb{R}^N \mid \lvert y - x \rvert < r \}$ は開球である。
- $x_0 = (1, 0, \dots, 0) \in \partial \Omega$ で内部球条件を充たす。

## 博士論文の構成

2 つの方程式を考察している。

- Chapter 3 で臨界 Sobolev 指数を持つ Henon 方程式の解の存在を示した(Theorem 1.1.1)。
  - Chapter 2 で移動する Talenti 関数の積分の評価を正確に行った。 $N \geq 3$ で $\epsilon$-order を決定 or 残余項を評価した。
  - $\partial \Omega$ で項が消える非自明な例も含まれている(Corollary 1.1.3)。
- Chapter 4 で Kirchhoff 型に、その手法を適用した(Theorem 1.1.2)。
  - Chapter 2 の手法の汎用性の高さの証拠となった。
  - 応用する際に non-local term を拡張してから適用した。

## 復習：臨界 Sobolev 指数はなぜ興味深いか

### Sobolev 埋め込み

$u^{p - 1}$ の項が出てくる半線形楕円型方程式を変分法で取り扱う。

- $2 \leq p < 2^* $ の場合： $H_0^1(\Omega) \subset \subset L^p(\Omega)$ はコンパクトに埋め込まれている。
  - 解析が比較的容易。
- $p = 2^* $ の場合： $H_0^1(\Omega) \subset L^ {2^ *}(\Omega)$ はコンパクトに埋め込まれていない。
  - 変分法で解析はできるが、難しい。
  - 解析は汎関数の評価と $(\text{PS})_c$ 条件に持ち込まれる。
  - コンパクト性を破るのが Talenti 関数を絞る列。
- $p > 2^*$ の場合： $H_0^1(\Omega) \not\subset L^p(\Omega)$ はそもそも埋め込まれていない。
  - 変分法では解析は困難。

### 臨界 Sobolev 指数の解析はどうなるか

どの手法も、大体以下のような手順になる([Brezis-Nirenberg '83] 型の手法)。

- 方程式の解は、汎関数 $I$ の非自明な臨界点。
- $I$ の $(\text{PS}) _c$ 条件が成立するのは、例えば $0 < c < S^{N/2} / N$ になる。
  - Mountain pass theorem などにより、 $I$ の mountain pass level が $S^{N/2} / N$ 未満なら、非自明な臨界点が見つかる。
- $I$ の実際の mountain pass level を評価しようとすると、 Talenti 関数を絞ることになり、 $S^{N/2} / N + $ (残余項) の形になる。
  - 例えば (残余項) $\leq C \epsilon^\alpha - C' \epsilon^\beta$ のような形になる。
  - ゆえに $\alpha > \beta$ ならば、残余項が負になるので、解が存在することが示される。

ここだけ覚える： **Talenti 関数の積分の残余項が、どういう $\epsilon$-order になるのかが、解の存在に直結する。**

## Chapter 3: Henon 型方程式

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

## Henon 方程式の先行研究

### Henon 方程式

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

- [Henon '73] で $N = 1$ で、 $u$ に絶対値がついた方程式を数値解析しているのが興りである。
- [Ni '82] で、 $2 \leq p < 2^*(\alpha) = 2(N + \alpha)/(N - 2)$ で球対称な正値解が存在することが示された。
- 我々の (1) は Henon 方程式と Brezis-Nirenberg 問題を合わせたものである。

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

$\alpha > 0$, $\lambda > \lambda_1'$ は定数である．ここで $\lambda_1'$ は，次の Dirichlet 固有値問題の第 $1$ 固有値とする：$-\Delta \phi = \lambda \phi \text{ in } \Omega$. A sign-changing solution の存在が、それぞれ以下の条件で示されている。

- [Long-Yang '12]: $N \geq 7$ 、 $\partial \Omega$ が滑らか。
- [Secchi '12]: $N \geq 5$ 、 $\Omega = B(0, 1)$ 。

我々は、 $0 < \lambda < \lambda _1$ の時に、 $N \geq 4$ で正値解の存在を示す。 $\Psi$ は関数で、 $\Omega$ はより一般的である。

## 臨界 Sobolev 指数を持つ Henon 型方程式はなぜ困難か

以下の、 **太字の部分は覚える** 。

- 臨界 Sobolev 指数を持つ場合、 [Brezis-Nirenberg '83] の手法が有効であるが、 Talenti 関数を $u^{2^* - 1}$ の係数の関数の **最大値を取る部分を中心に絞る** 必要がある。
  - 例えば私の修士論文は、それをやっている。
  - 係数が定数の場合、これは関係ないから、大抵 $0$ を中心に絞る。
- ところが Henon 型の場合、 $\lvert x \rvert^\alpha$ は $\Omega$ 上 **最大値を取らない** 。$x_0$ に近づくと $\sup_{x \in \Omega} \lvert x \rvert^\alpha = 1$ に近づく。
  - **新たな Talenti 関数の積分の評価が必要** になる。
    - [Brezis-Nirenberg '83] と計算が違う。 *既存の論文の引用では済まされない* 。
  - その「影響」をどこまで抑え込めるかが焦点となる。

## 移動する Talenti 関数 $u_{\epsilon, l}$

## $l(\epsilon) = \epsilon^\gamma$ について

$\sqrt{\epsilon}$ に「追いつかない」ようにしなくてはならないので、 $0 < \gamma < 1/2$ である。

### $N \geq 5$ の場合

## $l(\epsilon) = \lvert \log \epsilon \rvert^{-k}$ について

感覚的にいうと「 $\gamma$ が $0$ より小さいが、負ではない」場合に相当する。すなわち *この手法は「 $\gamma < 0$ 」の場合にも適用可能である* と考えてよろしい。

### 標語「$\log$ は定数」

もともと計算機業界で言われている標語(？)。

例：長さ $n$ の文字列の suffix array を構築する。

- 正直にやる方法：$O(n^2 \log n)$。
- Mamber-Myers 法：$O(n (\log n)^2)$。
- SA-IS 法：$O(n)$。

普通の計算機でやると、例えば以下のようになる。

||$O(n^2 \log n)$|$O(n (\log n)^2)$|$O(n)$|
|---|---|---|---|
|$n \approx 10^6$|数分| **一瞬** | **一瞬** |
|$n \approx 10^{10}$|論外|(多分数日)|約 20 分|

### $N = 4$ の場合

## $u_{\epsilon, l}$ の評価手法についてのまとめ

臨界 Sobolev 指数を持つ方程式を Henon 型に拡張する際に使えるが、既存の臨界 Sobolev 指数を持つ方程式の結果のうち、

- 指数の比べ合いになるもの(例： $C\epsilon^\alpha - C'\epsilon^\beta < 0$ の型)は *ほぼそのまま存在定理が出てくる* と見込まれる。
  - たとえ $\lvert \log \epsilon \rvert$ の差しかなくても、勝てる。
    - Brezis-Nirenberg の $N = 4$ で今回勝った。
- 一方で、指数が一致していて係数の比べ合いになる場合(例： $(A - A') \epsilon^\alpha < 0$ の型)は、 *必ず負ける* 。
  - Brezis-Nirenberg の $N = 3$ がその例。今回は存在定理が出てこなかった。
    - しかし少し工夫した方程式になると、すぐにこの場合は存在定理が出なくなる傾向にある。だから *適用範囲に改めて大きな制約を与えた訳ではない* 。

## $\Psi$ が境界で消える非自明な例



## Kirchhoff 型方程式

Kirchhoff-Henon 型方程式と呼ぶことにした。

### 主定理 2

## Kirchhoff 型方程式の先行研究

もともと時間発展する方程式。電磁気学と関係する。全体を概観することは、私の手に余る。

### 変分法的研究の興り



### Sobolev 臨界指数を持つ方程式

$N = 3$

## 次元によって手法が異なる

「次元が手法を決定する」

## 問題点

$N = 3$, $4 < q < 6$ の場合に、私が手法したい手法がある。しかし、

## non-local term を拡張

## 次の問題点

## 「explicitly に解ける」とは

標数 $0$ の体は素体として $\mathbb{Q}$ を部分体として含む。ここから出発する。

- $\sqrt{2}$ という数は、 $x^2 - 2 \in \mathbb{Q}[x]$ の正の根として *定義される* 。
- そうやって $\alpha > 0$ に対して $\sqrt{\alpha}$ という数を「知っている」ことにした結果、「 $2$ 次方程式も $2$ 次不等式も explicitly に解けるようになった」ことにしている。
  - $3, 4$ 次方程式も、 $\sqrt[k]{\alpha}$ を知っていることにした結果、解けるようになっただけとも言える。
  - 「解けない」 $5$ 次方程式 $x^5 + x - b = 0$ も $x = \alpha_b$ と解を置いたことにすれば、解けたことになる。
- もともとは **根に記号を置いているだけ** と言える。
  - その関数としての性質を、解析的に理解している。

## 根に記号を置く

- $(\text{PS})_c$ 条件が成立する上界 $c$ を求める。
- $\sup_{t > 0} I(t v_\epsilon)$ の計算をし、 $I$ の mountain pass level を評価する。

後者をここでは取り上げる。

## 補題

- 「よくわからないもの $T_\epsilon^2 A_\epsilon$」が「よくわからないもの $\eta_0$」に収束することが示せている。
- それどころか、「よくわからない order $O(T_\epsilon^2 A_\epsilon - \eta_0)$」が「よく *わかる* order $O(A_\epsilon - S)$」に一致している。
  - 十分な情報が引き出せている。

## 証明の概略



### 補足

実は、このような手法は、よく調べると [Zeng-Tang '16] で導入されていた。こちらは $\alpha = 0$, $a > 0$ に止まっている。しかし私は [Naimen '14 NoDEA] の直接拡張に成功したので、 $a = 0$, $b > 0$ の場合が含まれている。これは Henon 型 $\alpha > 0$ との相性も良い。

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
    - 例えば Kirchhoff 型は複数の既存の結果があるので、それらを「 Henon 化」するのもうまくいくだろう。
  - 人によって得意な手法が異なる。私 1 人では全部はできないだろう。手法が広がっていってほしい。

## 博士課程の数学研究のまとめ

- 楕円型方程式はとても難しい。研究課題を見つけて、新規性の高い結果を出すのは難しい。
  - どの分野もそうだが、中国の勢いはすごい。
  - 東大数理で楕円型方程式を研究している学生は、最近では私しかいないらしい。
- 私が出した全ての結果は、大学 3 年生以下の数学で理解可能な工夫がポイントになっている。
  - 手法が初等的でも、新規の結果が出れば良いと考える。
  - その意味では、大学院生でも、教員の入れ知恵がなくても結果は出せる。
  - 中学生の頃から大学院まで、数学やっていたのが結実した。

私にとって、数学は「人生をかけてやるもの」ではない。人生なら、やり直しができるから。私にとって数学は **寿命を削ってやるもの** だった。