# SSH通信時のパスフレーズを省略する

pullの度にpassphraseを聞かれるのをssh-agentを用いて省略する。  
ssh-agentに秘密鍵を登録する。
```bash
$ eval `ssh-agent`
```
ログインの際にと自動登録できるよう~/.bashrcに追加しておく。
```
eval `ssh-agent`
```
