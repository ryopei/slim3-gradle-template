# slim3-gradle-template
gradleでslimを使うためのテンプレート。今さら新規でslim3を採用する人も少ないと思うけど…

# 必要なもの

- gcloud SDK
- ant
- gradle (gradle wrapperを使用するなら不要)


# 使い方

## プロジェクトをクローンする
```
git clone git@github.com:ryopei/slim3-gradle-template.git
```

## web.xml
/src/main/webapp/WEB-INF/web.xmlを編集してslim3.rootPackageのparam-valueを任意のパッケージ名にする。
```
<context-param>
    <param-name>slim3.rootPackage</param-name>
    <param-value>** ここ **</param-value>
</context-param>
```

## コントローラの作成
gradlew gen-controllerコマンドを実行すると"Input a controller path."と聞かれるので"/hello"と入力

```
./gradlew gen-controller
> Task :gen-controller 
Input a controller path.
/hello
```

## 実行
gradlew gen-controllerでサーバーを起動.
http://localhost:8080/hello で動いていることを確認する

```
./gradlew appengineRun
```