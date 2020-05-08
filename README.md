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
|user_id|integer|null: false, foreign_key: true|
|password_id|integer|null: false, foreign_key: true|
|address_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :groups_users
- belongs_to :message

## groupテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :groups_users
- belongs_to :message

## messageテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|text_id|integer|null: false, foreign_key: true|
|image_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
