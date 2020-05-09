## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|password|integer|null: false|
|address|string|null: false|

### Association
- has_many :groups, through :groups_users
- has_many :groups_users
- has_many :messages

## groupテーブル

|Column|Type|Options|
|------|----|-------|
|group-name_id|integer|null: false, foreign_key: true|

### Association
- has_many :groups, through :groups_users
- has_many :groups_users
- has_many :message

## messageテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|text|integer|foreign_key: true|
|image|integer|foreign_key: true|

### Association
- belongs_to :groups
- belongs_to :user
