printfとの使い分け：printfに直接書く場合は、毎回固定された表示になる。

char変数を使う場合

①Yes / No 判定に使う
―　―　―　―　―　―　―　―　―　―　―　
\#include <stdio.h>

int main(void){

char c;

printf("続けますか？(y/n):");
scanf("%c", &c);

if ( c == 'y' || c == 'Y'){
    printf("はい、続けます。\n");}

else if ( c == 'n' || c == 'N'){
    printf("いいえ、終了します。\n");}

else {
    printf("yまたはnを入力してください\n");}

return 0;

}
―　―　―　―　―　―　―　―　―　―　―　
↑このコードでは、char に y, Y, n, N, それ以外の文字を代入して、代入された文字を判定する。
 条件分岐をさせるには変数を使う必要があり、文字を変数に入れるためにchar を使う。


②繰り返し処理で使う
―　―　―　―　―　―　―　―　―　―　―　
\#include<stdio.h>

int main(void){
    char c;

    for (c = 'A'; c <= 'Z'; c++){
        printf("%c",c);
    }

    printf("\n");

    return 0;
}
―　―　―　―　―　―　―　―　―　―　―　


③文字列から文字を抜き出して使う
―　―　―　―　―　―　―　―　―　―　―　
\#include <stdio.h>
int main (void){

    char str[] = "HELLO";
    int i;

    for (i = 0; str[i] != '\0'; i++){
        char c = str[i];
        printf("%c\n",c);
    }

    return 0;
}
―　―　―　―　―　―　―　―　―　―　―　