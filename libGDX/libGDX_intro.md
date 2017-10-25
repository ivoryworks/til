# libGDX setup for Android Studio
## libGDXプロジェクトの生成
[libGDXのDownloadページ](https://libgdx.badlogicgames.com/download.html)からsetup用のjarファイルをダウンロードする。  
jarフィアルを実行するとsetupアプリが起動する。
```bash
$ java -jar gdx-setup.jar
```
<img src="https://raw.githubusercontent.com/ivoryworks/image_store/master/libGDX/libGDX_setup_app.png" width=480px />

各々の項目を入力し、扱いたいProjects(AndroidやiOSなど)を選択した後にGenerateをクリックする。  
なお、Destinationの項目は、初期値が絶対パスのように書いてあるが相対パスとして扱われるので注意。  

数分の後にDestinationで指定したパスにプロジェクトファイルが作成される。

## Android Studioへのインポート
Import project(Eclipse ADT,Gradle,etc.)でインポートする。インポートで指定するのは、setappアプリで生成したプロジェクトにandroidディレクトリのbuild.gradle。  
libGDXのコア実装が、androidディレクトリより上の階層にあるため、androidフォルダ単体ではビルドできない。

<img src="https://raw.githubusercontent.com/ivoryworks/image_store/master/libGDX/libGDX_sample_app.png" width=480px />
