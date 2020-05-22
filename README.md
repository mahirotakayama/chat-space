# ChatーSpaceDB設計

## users table

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null:false,unique: true|
|email|string|null: false|

### Association
- has_many :groups,through: members
- has_many :messages
- has_many :members


## members table
|Column|Type|Options|
|------|----|-------|
|user|refertences|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

## Assosiation
- belongs_to :group
- belongs_to :user



## messages table
|Column|Type|Options|
|------|----|-------|
|user|refertences|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|
|content|string|
|imgae|string|

## Assosiation
- belonds_to :user
- has_many :groups


## groups table
Column|Type|Options|
|------|----|-------|
|user|refertences|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|
|
|

## Assosiation
- belongs_to :group
- belongs_to :user-

