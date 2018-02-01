# Gradleのお勉強
gradle ver4.5
## コマンドラインオプション
- -i (--info)
- -s (--stacktrace)
- -S (--full-stacktrace)
- -d (--debug)
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
