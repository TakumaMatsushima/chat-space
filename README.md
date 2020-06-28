## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|string|null: false|

### Association
- belongs_to :groups
- has_many :comments

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_name|string|null: false|

### Association
- has_many :comments
- has_many :user

## commentsテーブル

|Column|Type|Options|
|------|----|-------|
|text|integer|null: false|
|user_id|integer|null: false|

### Association
- belongs_to :group
- belongs_to :user


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
