# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## userテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false|
|name|integer|null: false|
|email|integer|null: false|
|password|integer|null: false|

### Association
- belongs_to :user_group
- belongs_to :message

### groupテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false|
|group_name|integer|null: false|

### Association
- belongs :user_group
- belongs :message

## user_groupテーブル

|Column|Type|Options|
|------|----|-------|
|user_group_id|integer|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- has_many :user
- has_many :group

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|message_id|integer|null: false|
|message|text|null: false|
image|string|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign:true|

### Association
- has_many :user
- has_many :group