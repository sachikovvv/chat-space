# README

This README would normally document whatever steps are necessary to get the
application up and running.
Things you may want to cover:

# DB設計

## userテーブル
|Column|Type|Options|
|------|----|-------|
|user_name|string|null: false|
|emailaddress|string|null: false|
|password|intenger|null: false|

### Association
- has_many :body
- has_many :group
- has_many :members

## bodyテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user

## groupテーブル
|Column|Type|Options|
|------|----|-------|
|group_name|string|null: false|
|members_id|integer|null: false, foreign_key: true|

### Association
- has_many :members
- belongs_to :user


## membersテーブル
|Column|Type|Options|
|------|----|-------|
|member_name|string|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

### 

* Ruby version
- 2.5.1
* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
