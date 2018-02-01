# Gradleのお勉強
gradle ver4.5
## コマンドラインオプション
- -i (--info)
- -s (--stacktrace)
- -S (--full-stacktrace)
- -d (--debug)
## ビルド
### ビルド実行時に実行されるスクリプト
- 初期化スクリプト `init.gradle`
	ビルドの最初に実行されるスクリプト。主にユーザー情報や実行環境などの初期設定を行う。
- 設定スクリプト `settiongs.gradle`
	ビルド対象のプロジェクトの設定を行うスクリプト。ビルドに参加するプロジェクトを定義する用途で使用し、マルチプロジェクトでは必須のスクリプト。
- ビルドスクリプト `build.gradle`
	ビルドのスクリプトを定義する。
### ビルド時に使用されるインプット
- プロパティファイル　`gradle.properties`
	環境によって値が変わるようなパラメータをビルドスクリプトの外で記述した場合に使用する。
- 環境変数/コマンドライン引数
	Gradleがインストールされてるマシンの環境変数とビルド実行時にコマンドに渡す引数。
- buidSrcプロジェクト
	編集中。（説明読んでも今はよくわからない）
## コンフィグレーション
依存関係をグループ化して分類するコンフィグレーションという仕組みがある。
- compile
- runtime
- testCompile
- testRuntime
- archives
- default

各々の特徴はなんとなく名前から察しがつくので割愛。 `archives` と `default` はよくわからないけど、使ってるところみた事ないし割愛。

例：
```
dependencies {
    compile('org.springframework.boot:spring-boot-starter')
    compile('org.springframework.boot:spring-boot-starter-web')
    compile('org.thymeleaf:thymeleaf-spring4')
    compile('org.springframework.boot:spring-boot-starter-jooq')
    compile('org.thymeleaf.extras:thymeleaf-extras-java8time')
    compile('org.springframework:spring-jdbc')
    compile('mysql:mysql-connector-java')
    testCompile('org.springframework.boot:spring-boot-starter-test')
    testCompile('com.ninja-squad:DbSetup:2.1.0')
 }
```
## その他
.gitigonreは[gibo](https://github.com/simonwhitaker/gibo)使ってみたけどなんか多いな
