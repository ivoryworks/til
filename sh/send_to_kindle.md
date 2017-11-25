# コマンドラインでKindleへ電子書籍を送信したい
Gmailでは25MB以上の添付ファイルを送信できない。  
30MBのPDFをKindleに送りたいのでmailコマンドで送信する。
## uuencode
添付したいファイルをエンコードするコマンド。
こんな感じで使う。第一引数は添付するファイル、第二引数は添付ファイル名(メール上の)。
```bash
$ uuencode ./xxxxxxxx.pdf a.pdf | mail xxxxxxxx@kindle.com
```
## uuencodeが存在しない
手元のMacには入っていたが、CentOSで建てたサーバーに無かった。  
uuencodeというパッケージは無かったので調べると、sharutilsというパッケージに含まれているらしい。
```bash
$ sudo yum install sharutils
```
