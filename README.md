## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|
|password|integer|null: false|
### Association
- has_many :posts
- has_many :comments

## groups
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
### Association
- has_many :posts_tags
- has_many  :posts,  through:  :posts_tags

## messages
|Column|Type|Options|
|------|----|-------|
|image｜string｜null: false|
|text|text｜null: false|
|group_id|int|foreign_key: true|
### Association
- belongs_to :post
- belongs_to :tag

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|memder|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :post
- belongs_to :user