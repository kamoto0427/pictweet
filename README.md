## アプリ名
Pictweet

## アプリの概要
テックキャンプの基礎カリキュラムで作成した簡易版twitter

## 機能
- ユーザー新規登録・ログイン
- 投稿
- 投稿の詳細・編集・削除
- 投稿にコメント
- 検索

## 新規登録
![demo](https://gyazo.com/e9386f1f42df32201f1ddf7fd54a37ad/raw)

## ログイン
![demo](https://gyazo.com/cd306e0e2e9c7d670db000a65871ef5b/raw)

## 投稿
![demo](https://gyazo.com/8e94462c3d32664928bbd0bb2f886a46/raw)

## 投稿の詳細画面・コメント
![demo](https://gyazo.com/d8a4adc647b72f02416e8c1eca6c30a2/raw)

## 投稿の編集
![demo](https://gyazo.com/28b48ed5a657f3baa129de0e6f26c8d7/raw)

## 投稿の削除
![demo](https://gyazo.com/d14a09ab038878ab89aef91f7a93a8ba/raw)

## 投稿の検索
![demo](https://gyazo.com/e7e3b65bd4cae0bb581553979368334c/raw)

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|nickname|string||
|email|string|null :false|
|password|string|null :false|

### Association
- has_many :tweets
- has_many :comments

## tweetsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer||
|name|string||
|text|string||
|image|string||

### Association
- belongs_to :user
- has_many :comments

## commentsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer||
|tweet_id|integer||
|text|text||

### Association
- belongs_to :user
- belongs_to :tweet

