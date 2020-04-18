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

