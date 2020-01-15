
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :massages
- has_many :groups_users


## groups テーブル
|Column|Type|Options|
|------|----|-------|
|name|strings|null: false|

### Association
- has_many :users
- has_many :users, through: :members
- has_many :messages has_many :members


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## messageテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|strings｜
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user










