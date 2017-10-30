# 電池残量の疑似変化
## shellコマンドによってBATTERY_CHANGEDのBroadcastを発行する(残量50%)
正規のBATTERY_CHANGEDが発行されたタイミングでもとに戻る。
```bash
$ adb shell am broadcast -a android.intent.action.BATTERY_CHANGED --ez present false --ei state 2 --ei level 50
```
