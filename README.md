# Programming Words

## 【アプリ概要】
IT関係の単語の解説が登録＆管理＆検索が出来るアプリ。単語に関する別サイトのURLも一緒に表示される。


## 【仕様 (機能)】
* 単語が検索できる機能がついている
* 検索後、単語名・単語の意味・関連する記事のURLが表示される
* 管理者のみ単語の登録・編集ができる


## 【開発環境】
* Laravel 9
* PHP 8.1.3
* MySQL 8.0.28
* Docker


## 【ブランチ】
* develop (環境構築)
  * READMEの作成
  * GitHubにrepositoryを登録
  * Laravel 9をインストール
  * Laravelで作ったProgrammingWordsのディレクトリとrepositoryを連携させる
  * テーブルの作成
  

* feature/breeze (ユーザー管理機能)
  * ログイン機能(Breeze)のインストール
  * デザインの調整
  * 管理者のみログインされるように調整

    
* feature/word-register (単語の登録機能)
  * wordsテーブルの作成
  * デザインの調整
  * データベースに単語が保存される機能の実装
  * 登録完了アナウンスの実装


* feature/word-search (検索機能)
  * デザインの調整
  * 検索機能の実装


* feature/word-detail (単語詳細の表示)
  * デザインの調整
  * データベースに保存されている単語情報が表示されるように実装


* feature/word-edit (単語情報の編集)
  * デザインの調整
  * データベースに保存されている情報が編集できるように実装


## 【データベース】
* usersテーブル
  | Field             | Type            | Null | Key | Default | Extra          |
  | ----------------- | --------------- | ---- | --- | ------- | -------------- |
  | id                | bigint unsigned | NO   | PRI | NULL    | auto_increment |
  | name              | varchar(255)    | NO   |     | NULL    |                |
  | email             | varchar(255)    | NO   | UNI | NULL    |                |
  | email_verified_at | timestamp       | YES  |     | NULL    |                |
  | password          | varchar(255)    | NO   |     | NULL    |                |
  | remember_token    | varchar(100)    | YES  |     | NULL    |                |
  | created_at        | timestamp       | YES  |     | NULL    |                |
  | updated_at        | timestamp       | YES  |     | NULL    |                |


* wordsテーブル
  | Field             | Type            | Null | Key | Default | Extra          |
  | ----------------- | --------------- | ---- | --- | ------- | -------------- |
  | id                | bigint unsigned | NO   | PRI | NULL    | auto_increment |
  | name              | varchar(255)    | NO   |     | NULL    |                |
  | meaning           | varchar(255)    | NO   |     | NULL    |                |
  | user_id           | bigint unsigned | NO   |     | NULL    |                |
  | del_flg           | bigint unsigned | NO   |     | 0       |                |
  | created_at        | timestamp       | YES  |     | NULL    |                |
  | updated_at        | timestamp       | YES  |     | NULL    |                |


## 【カスタマイズ】
