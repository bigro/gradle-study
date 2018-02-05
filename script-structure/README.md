# スクリプトファイルの構造
スクリプトファイルの構造や記述についての勉強

## システムプロパティ

### システムプロパティをコマンドライン引数で渡す場合
`-D<プロパティ名>=<値>` で渡す。

例；greetタスクを起動する際に `Hello` という文字列をmessageに渡す。
 
 `gradle -Dmessage=Hello greet`

greetタスクの定義
```
task greet << {
	println System.properties['message']
}
```

### プロパティファイルで指定する
[gradle.properties](./gradle.properties)に `systemProp` をプレフィックスとして付けてプロパティを記述する。