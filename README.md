## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, uniqle: true|
|mail|string|null: false|

### Association
- bas_many :groups, through: members
- bas_many :messages
- bas_many :messages