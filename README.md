#zencoma

「cat」を「かｔ」と入力しても実行してくれるようなalias集を自動生成します。

半角に切り替え忘れて全角でコマンドを叩いてしまった時でも、そのままエンターキーを叩けばコマンドが実行できるようになります。

##インストール方法

1. zencomaスクリプトをダンロードしてください(https://raw.githubusercontent.com/roronya/zencoma/master/zencoma)
2. パスの通ったところにzencomaスクリプトを置いてください。(`~/bin` とか)
3. 実行権限を与えてください。(`chmod 755 ~/bin/zencoma`)
4. 使用しているシェルの設定ファイル(bashなら.bashrc,zshなら.zshrc)に以下を書き加えてください。

```shellscript
source $HOME/.zencoma
```

##使い方

```shellscript
$ zencoma
```
