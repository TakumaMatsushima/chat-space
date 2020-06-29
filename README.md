## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|string|null: false|

### Association
- has_many :groups,  through:  :users_groups
- has_many :comments
- has_many :users_groups

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|

### Association
- has_many :comments
- has_many :users,  through:  :users_groups
- has_many :users_groups

## commentsテーブル

|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|img|text|null: false|
|user_id|integer|null: false|
|group_id|integer|null: false|


### Association
- belongs_to :group
- belongs_to :user

## users_groupsテーブル

|Column|Type|Options|
|------|----|-------|
|users_id|integer|null: false, foreign_key: true|
|groups_id|integer|null: false, foreign_key: true|


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
