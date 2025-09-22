\#include <stdio.h>                       // 標準入出力ライブラリをインクルード

int main(void){                          // プログラムのエントリーポイント
    char buf[100];                       // 標準入力から読み取る一時バッファを定義（100文字分）
    fgets(buf, sizeof(buf), stdin);      // 標準入力から1行を読み込み、bufに格納

    char name[100];                      // 名前を格納する配列を定義（100文字分）
    sscanf(buf,"%s", name);              // bufの先頭から空白区切りの文字列をnameにコピー
    printf("Hello %s\n", name);          // nameを使って挨拶を出力

    return 0;                            // 正常終了を意味する戻り値
}

scanfと違い、 fgetsは、スペース（␣）を含めた1行丸ごと読み込みが可能。またバッファサイズに余裕がある場合は、改行文字もそのまま読み込む。

fgets(buf, sizeof(buf), stdin);
↓
fgets(<mark style="background: #70b8ff;">char変数</mark>,<mark style="background: #D2B3FFA6;">sizeof(char変数), <mark style="background: #9df578;">入力方法</mark></mark>)

<mark style="background: #70b8ff;">char変数</mark>：char で宣言した変数
<mark style="background: #D2B3FFA6;">sizeof(char変数)</mark>：直接数字を打ち込んでも良いが、先に変数宣言でサイズを指定しておいたほうが、後からサイズ変更が容易になる。
<mark style="background: #9df578;">入力方法</mark>：
・stdin　キーボードから入力を受け取る。
・ファイルから読み込む


fgets関数の用途は、「入力をそのまま文字列として扱う」場面に向いている。