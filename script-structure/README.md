# スクリプトファイルの構造
スクリプトファイルの構造や記述についての勉強

## システムプロパティ

### コマンドライン引数で渡す場合
`-D<プロパティ名>=<値>` で渡す。

例：greetタスクを起動する際に `Hello` という文字列をmessageに渡す。
 
 `gradle -Dmessage=Hello greet`

greetタスクの定義
```
task greet << {
	println System.properties['message']
}
```

### プロパティファイルで指定する
[gradle.properties](./gradle.properties)に `systemProp` をプレフィックスとして付けてプロパティを記述する。

## 拡張プロパティ
編集中。

## プロジェクトプロパティ
ビルド対象のプロジェクトのプロパティとして利用する。拡張プロパティの仕組みを利用しているため内部的には拡張プロパティとの違いはない。

### コマンドライン引数で渡す場合
`-P<プロパティ名>=<値>` で渡す。

例：hogeタスクを起動する際に `HogeHoge` という文字列をhogehogeに渡す。

`gradle -Phogehoge=HogeHoge hoge`

hogeタスクの定義
```
task hoge << {
	println hogehoge;
}
```

### プロパティファイルで指定する
[gradle.properties](./gradle.properties)に `<プロパティ名>=<値>` と記述する。

## プロジェクトプロパティのロード順
|ロード順|設定方法|
|---|---|
|1|プロパティファイル(プロジェクトディレクトリ)|
|2|プロパティファイル(ホームディレクトリ)|
|3|環境変数|
|4|コマンドライン引数 -D|
|5|コマンドライン引数 -P|
