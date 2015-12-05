#zencoma

「cat」を「かｔ」と入力しても実行してくれるようなalias集を自動生成します。

半角に切り替え忘れて全角でコマンドを叩いてしまった時でも、そのままエンターキーを叩けばコマンドが実行できるようになります。

全角コマンドを生成するのは、$PATHに書かれたディレクトリ以下のコマンドのみで、シェルの設定ファイル(.bashrcや.zshrc)でaliasされているコマンドには効きません。

*※python2系でしか動きません。*

##インストール方法

1. zencomaスクリプトをダンロードしてください(https://raw.githubusercontent.com/roronya/zencoma/master/zencoma)
2. パスの通ったところにzencomaスクリプトを置いてください。(`~/bin` とか)
3. 実行権限を与えてください。(`chmod 755 ~/bin/zencoma`)
4. 使用しているシェルの設定ファイル(bashなら.bashrc,zshなら.zshrc)に以下を書き加えてください。

```shellscript
source $HOME/.zencoma
```

##使い方

zencomaを実行すると、~/.zencoma にalias集が書き込まれます。

```shellscript
$ zencoma
updating ~/.zencoma
done.
```

インストール方法の4番に則りシェルの設定ファイルから.zencomaを読み込むようにしてあれば、次回シェルへログインしたときから全角でのコマンドが有効になります。

またすぐに適用したい場合は以下を実行してください。

```shellscript
$ source ~/.zencoma
```

##例

```shellscript
#半角
> cat test.php                                                                                                                                                                                                        ~@MT-PRO1200
<?php

http_head('http://example.com');

#全角
> かｔ test.php                                                                                                                                                                                                       ~@MT-PRO1200
<?php

http_head('http://example.com');
```

##注意点
+ アルファベットからひらがなへの変換はibus-mozcの辞書にしたがっています。概ね同じ挙動だと想いますが、ibus-mozc以外のIMEの環境では完璧に動作しないかもしれません。
+ 新しくソフトウェアをインストールなどしてコマンドが増えた場合は逐一zencomaを実行しないと新しいコマンドの全角コマンドaliasは生成されません。

