printf の "f" はフォーマットの "f"


printf("<mark style="background: #FFB8EBA6;">書式</mark>",値1, 値2, ...);  //←理論上はいくつでも値を入れられる




printf("%d円\n",100);



printf("%d",100 + 30 * 2);
printf("%d",(100 + 30) * 2);

↑ 計算は左から順に行われるが、四則演算の優先順位の法則は適用される。

<mark style="background: #FFB8EBA6;">書式</mark>の中に%で始まる書式指定子を書くことで、値を埋め込める。
書式指定子には「型」 「幅」 「精度」 「フラグ」 「長さ」 を組み合わせて指定する。

■型
・整数系
　%d / %i ：符号付き10進整数
　%u ：符号なし10進整数
　%o ：8進数
　%x / %X : 16進整数（小文字 / 大文字）
・浮動小数点系
　%f：小数点表記（固定小数点）
　%F：小数点表記（INF / MAN を大文字で）
　%e / %E：指数表記（大文字 / 小文字）
　%d / %G：%fまたは%eを自動選択

・文字 / 文字列
　%c：文字
　%s：文字列
  
・ポインタ / その他
　%p：ポインタ（実装依存の表記、通常は16進）
　\%%：%そのもの

・長さ修飾子（整数の大きさを指定）
　hh：signed char / unsigned char
　h  ：short
　l  ：long
　ll ：long long
　z  ：size_t
　j  ：intmax_t / uintmax_t
　t  ：ptrdiff_t
　L  ：long double （浮動小数点に使う）