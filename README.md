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
|body|text|null: false|
|image|string|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :post
- belongs_to :user