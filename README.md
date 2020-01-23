## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, uniqle: true|
|mail|string|null: false|

### Association
- bas_many :groups, through: members
- bas_many :messages
- bas_many :members

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|text||
|text|text||
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- has_many :comments

## commentsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|messages_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :messages
- belongs_to :user