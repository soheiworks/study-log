\#include <stdio.h>

int main(void){
    char buf[100];
    fgets(buf, sizeof(buf), stdin);

    char name[100];
    sscanf(buf,"%s", name);
    printf("Hello %s\n", name);
    
    return 0;
}

scanfと違い、 fgetsは、スペース（␣）を含めた1行丸ごと読み込みが可能。またバッファサイズに余裕がある場合は、改行文字もそのまま読み込む。

fgets(buf, sizeof(buf), stdin);
↓
fgets(<mark style="background: #70b8ff;">char変数</mark>,<mark style="background: #8d81fc;">sizeof(char変数</mark>), <mark style="background: #9df578;">入力方法</mark>)

<mark style="background: #70b8ff;">char変数</mark>：char で宣言した変数
<mark style="background: #8d81fc;">sizeof(char変数)</mark>：直接数字を打ち込んでも良いが、先に変数宣言でサイズを指定しておいたほうが、後からサイズ変更が容易になる。
<mark style="background: #9df578;">入力方法</mark>：
・stdin　キーボードから入力を受け取る。
・ファイルから読み込む


