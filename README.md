![Free_Sample_By_Wix_waifu2x_art_noise3_scale_tta_1.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/639462/2aacbd0c-bbbc-5fc6-c802-0d5d8dc2ed79.png)

# Snitch

#### Snitchは**お土産一覧アプリケーション**です。

ここで紹介されるお土産は著名人御用達の特別なものばかり！

2018年3月に放送終了した 「とんねるずのみなさんのおかげでした」の人気コーナー「食わず嫌い王」にて、ゲスト出演した著名人が紹介したお土産のみを掲載しております。
番組のファンだった方、どんなお土産を買おうか迷っている方、小腹を満たしたい方などあらゆる方に楽しんでいただきたく当アプリケーションを開発しました。

## サイト

[こちら](https://snitch1.herokuapp.com/)のサイトにて公開しています。
読み込みに20秒ほどかかります。


## 機能一覧
- ユーザー登録/ログイン機能
- コンテンツ検索機能
- コンテンツお気に入り機能
  - お気に入り登録
  - お気に入り解除
  - お気に入り一覧
- 登録情報更新
- 退会機能
- バリデーション機能
- コンテンツ詳細画面での地図掲載

## 使用技術
- Java SE 14.0.1
- spring-boot 2.3.3
- maven 3.6.3
- spring JDBC
- jquery 3.3.1-1
- postgresql.version 42.2.14
- bootstrap 4.2.1
- thymeleaf
- Google Maps API
- spring-security.version　5.3.4.
- lombok　1.18.12
- thymeleaf-layout-dialect.version 2.4.1
- Junit 5
- Mockito 3.3.3
- Hamcrest

![使用技術](https://user-images.githubusercontent.com/63634976/115809434-1355c500-a427-11eb-802a-bc3d0fac8bba.jpeg)


## テーブル構造

![QuickDBD-Snitch20210419](https://user-images.githubusercontent.com/63634976/115809376-f28d6f80-a426-11eb-9693-a6ec462106d4.png)


## 制作期間

7ヶ月

## コードカバレッジ率

82.2%


## 会員登録の方法

![registration](https://user-images.githubusercontent.com/63634976/115824625-31312300-a443-11eb-82fa-3a5e4617e7f3.gif)

サイト上部にある「Login」をクリックすると、ログインページに移動します。
「新規登録」 ボタンを押すと登録フォームの入力を促されます。
登録が無事に完了すると、マイページに移動します。
マイページではお気に入りしたお土産を見たり、登録した情報を変更したり、退会処理ができます。

## ログイン

![login](https://user-images.githubusercontent.com/63634976/115831389-7c036880-a44c-11eb-9583-8986e336bdf1.gif)

サイト上部にある「Login」をクリックすると、ログインページに移動します。
フォームに登録したユーザーネーム、パスワードを入力し認証が成功するとマイページに遷移します。


## 検索

![search](https://user-images.githubusercontent.com/63634976/115827456-41e39800-a447-11eb-910b-e513abf8cd47.gif)

検索フォームでキーワードを入力すると、お土産を検索することができます。
検索フォームは画面上部中央にあります。

## お気に入り登録

![addfavorite](https://user-images.githubusercontent.com/63634976/115825243-17dca680-a444-11eb-977f-1f23aac2a850.gif)

ログイン済みの場合、お気に入り機能が使えるようになります。
お土産の詳細画面にある「お気に入り」と書かれた黄色のボタンを押すと、お気に入りに追加することができます。
お気に入りしたお土産は、マイページの「お気に入り」で確認できます。

## お気に入り解除

![deletefavorite](https://user-images.githubusercontent.com/63634976/115825608-a2bda100-a444-11eb-829f-df81e4886b8e.gif)

お気に入りリストからお土産を外すには、お土産の詳細画面を開き「お気に入り解除」を押します。

## 登録情報更新

![update](https://user-images.githubusercontent.com/63634976/115826568-144a1f00-a446-11eb-9ef5-9aaa8cdf51b7.gif)

登録情報更新はマイページから行えます。
マイページにある「登録情報更新」と書かれたボタンを押すと、登録情報更新ページに遷移します。
フォームに新しいユーザーネーム、もしくは新しいメールアドレスを入力し、パスワードを入力します。
パスワードを変更しない場合は、現在使用中のものを入力してください。
「更新」と書かれたボタンを押すと、更新処理が行われ再度マイページに移行します。


## 退会

![withdrawal](https://user-images.githubusercontent.com/63634976/115826848-79057980-a446-11eb-9b87-bfb238196e7f.gif)

退会はマイページから行えます。
マイページにある「退会」と書かれたボタンを押すと、退会ページに遷移します。
「退会」と書かれたボタンを押すと、退会処理が行われます。

## バリデーション機能

### 検索フォーム

![searchvalidation](https://user-images.githubusercontent.com/63634976/115828296-786de280-a448-11eb-9a73-e9fda4059f01.gif)

入力された内容が下記のパターンの場合にバリデーションエラーが発生します。
- 空白 → 「キーワードを入力してください」と表示


### 新規ユーザー登録フォーム

![signupvalidation](https://user-images.githubusercontent.com/63634976/115829888-7dcc2c80-a44a-11eb-94bc-ff861d618cbe.gif)

入力された内容が下記のいずれかのパターンの場合にバリデーションエラーが発生します。
- 空白 → 「ユーザーネーム/メールアドレス/パスワードを入力してください」と表示
- 3字以下/20字以上 →　「ユーザーネーム/パスワードは3字以上20字以下で入力してください」と表示
- 半角英数字以外 →　「ユーザーネーム/パスワードは半角英数字で入力してください」と表示
- メールアドレス形式でない →　「メールアドレス形式で入力してください」と表示
- ユーザーネームが既に登録済み →　「入力されたユーザーネームは既に使用されています」

### ログインフォーム

![loginvaildation](https://user-images.githubusercontent.com/63634976/115828975-56289480-a449-11eb-83ae-243af7f5c871.gif)

入力された内容が下記のパターンの場合にバリデーションエラーが発生します。
- 入力内容の誤り → 「ユーザーネームまたはパスワードが間違っています。」と表示

### ユーザー登録情報更新フォーム

![updatevalidation](https://user-images.githubusercontent.com/63634976/115830550-6b9ebe00-a44b-11eb-9388-893581bd2eb4.gif)

入力された内容が下記のいずれかのパターンの場合にバリデーションエラーが発生します。
- 空白 → 「ユーザーネーム/メールアドレス/パスワードを入力してください」と表示
- 3字以下/20字以上 →　「ユーザーネーム/パスワードは3字以上20字以下で入力してください」と表示
- 半角英数字以外 →　「ユーザーネーム/パスワードは半角英数字で入力してください」と表示
- メールアドレス形式でない →　「メールアドレス形式で入力してください」と表示
- ユーザーネームが既に登録済み →　「入力されたユーザーネームは既に使用されています」※1

※1
ユーザーネーム以外を変更したいという場合もあるので、
ユーザーネームが認証済みのものと同一の場合はバリデーションエラーは発生せずに正常に登録内容が更新されます。

## 作者
佐藤博紀(https://qiita.com/hiroki1994)
