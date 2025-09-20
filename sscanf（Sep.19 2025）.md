\#include <stdio.h>

int main(void){
    fgets(buf, sizeof(buf), stdin); 

    char name[100]; // ←配列の形式。配列（の先頭アドレス）は自動で決められ、２番目以降のアドレスも順次＋1のアドレスで割り振られる。
    
    return 0;

}

scanfが標準入力（キーボード）から読むのに対して、
sscanfは文字列（メモリの中のデータ）から読むという違いがある。

scanf("%d", &age);
sscanf(<mark style="background: #9df578;">buf.</mark> <mark style="background: #FC81F973;">"%s"</mark>, <mark style="background: #70b8ff;">name</mark>);

<mark style="background: #9df578;">buf</mark>：既に宣言している変数
<mark style="background: #FF70E35C;">"%s"</mark>：空白で区切られた1単語を読み取る
<mark style="background: #70b8ff;">name</mark>：ユーザーから入力された結果を格納する変数

