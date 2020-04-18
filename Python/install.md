## anacpnda をインストール
### jupyter notebookが失敗する
上記コマンド実行で、以下のエラーが発生
``` code
～
～
指定されたプロシージャが見つかりません。
```
色々環境変数を設定したんだけど、以下の内容で解決  
「Anaconda3\Library\bin」の中にある
「libcrypto-1_1-x64.dll」と「libssl-1_1-x64.dll」を
「Anaconda3\DLLs」にコピーする

これで、コマンドプロンプトから「jupyter notebook」が実行できる

## jupyter notebook のデフォルト参照先の変更
```
jupyter notebook --generate-config
```
を実行する。

作成された、jupyter_notebook_config.pyを開き、
#c.NotebookApp.notebook_dir = ''
を探して、そこに変更後のパスを指定
