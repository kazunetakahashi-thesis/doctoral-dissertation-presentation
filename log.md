# $log$ についての補足

## $l(\epsilon) = \lvert \log \epsilon \rvert^{-k}$ について

感覚的にいうと「 $\gamma$ が $0$ より小さいが、負ではない」場合に相当する。すなわち *この手法は「 $\gamma < 0$ 」の場合にも適用可能である* と考えてよろしい。

> **Corollary 2.2.7**： $k > 0$ とし、 $l = l(\epsilon) = \lvert \log \epsilon \rvert^{-k}$ とする。このとき、 $\epsilon \to 0$ のとき次式が成立する。
> \[
>   \int_\Omega \Psi_0 u_{\epsilon, l}^2 dx
>   = \begin{cases}
>     O(\lvert \log \epsilon \rvert^{-\beta k} \epsilon^{-(N-4)/2})                    & N \geq 5, \\
>     O(\lvert \log \epsilon \rvert^{1 -\beta k}) & N = 4,    \\
>     O(\lvert \log \epsilon \rvert^{-(\beta + 1)k})  & N = 3
>   \end{cases}
> \]

### 標語「$\log$ は定数」

もともと計算機業界で言われている標語(？)。

> **例** ：長さ $n$ の文字列の suffix array を構築する。
>
> - 正直にやる方法：$O(n^2 \log n)$。
> - Mamber-Myers 法：$O(n (\log n)^2)$。
> - SA-IS 法：$O(n)$。
>
> 普通の計算機でやると、例えば以下のようになる。
>
> ||$O(n^2 \log n)$|$O(n (\log n)^2)$|$O(n)$|
> |---|---|---|---|
> |$n \approx 10^6$|数分| **一瞬** | **一瞬** |
> |$n \approx 10^{10}$|論外|(多分数日)|約 20 分|

### $N = 4$ の場合

(残余項) $< 0$ は以下と同値になる。

\[
  \left( S - S (1 - 2l)^ {2\alpha/2^ *} \right) + \left( C \epsilon \lvert \log \epsilon \rvert^ {2k} - C' \epsilon \lvert \log \epsilon \rvert^{1 - \beta k} \right) < 0.
\]

2 項目が負になるような $\epsilon > 0$ が存在するための条件は、

\[
  k < \frac{1}{2 + \beta}.
\]

以下同じ。
