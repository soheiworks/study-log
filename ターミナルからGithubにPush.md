① GitHub作業用のディレクトリに移動する

②git clone ttps://github.com/soheiworks/<mark style="background: #FF5582A6;">Rot-addict.git</mark> ←リポジトリ名
（git cloneはローカルPCにリポジトリの内容をコピーするので、PCごとに最初の1回だけで良い。）

③Rot-addictというディレクトリが生成されるので、中にアップロード(push)したいファイルを入れる。

④git add Rot-addict.c
   pushしたいファイルをセット
   ※ git add . にすれば、ディレクトリ内のファイルが全てセットされる
   ※git addしたファイルのaddを止めたい場合は、git reset <mark style="background: #ABF7F7A6;">Rot-addict.c </mark> ←ファイル名
   　git addしたすべてのファイルのaddを止めたい場合は、git reset

⑤git commit -m "pushしたいファイルの修正内容" 
   ※commit済のファイルを止めたい場合は、 git reset HEAD^

⑥git push <mark style="background: #FFB86CA6;">origin</mark> <mark style="background: #D2B3FFA6;">main</mark>
　（リモートリポジトリ<mark style="background: #FFB86CA6;">origin </mark>に、ローカルの<mark style="background: #D2B3FFA6;">main</mark> branchの内容を飛ばすという意味）

<mark style="background: #FFB86CA6;">origin</mark>　は、Githubのリポジトリのこと
<mark style="background: #D2B3FFA6;">main</mark>　は、デフォルトのブランチ名（昔はmasterと呼ばれた）



④の　add　は、発射台にロケットを載せるようなもの
⑤の　git commit -m は、打ち上げ前にどんなロケットかアナウンスするようなもの
⑥の　git push origin main で、打ち上げ
