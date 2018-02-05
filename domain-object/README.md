# ドメインオブジェクト
スクリプトブロックとドメインオブジェクトの関係やドメインオブジェクト自身の機能

## スクリプトブロックの正体
スクリプトファイルはGradleのドメインオブジェクトに委譲される。
スクリプトブロックとは、その委譲先のドメインオブジェクトのメソッドである。
```
repositories {
    mavenCentral()
}
```
例えば上記のコードだと `repositories` は委譲先の `Project`　オブジェクトのメソッド `Project#repositories(Closure closure)` に `{mavenCentral()}` というクロージャを引数に渡して呼んでいることになる。
