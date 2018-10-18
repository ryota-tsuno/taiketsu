# README

## taiketsusテーブル

|Column|Type|Options|
|------|----|-------|
|topic_id1|text|null: false|
|topic_id2|text|null: false|

### Association
- has_one :topic

## topicsテーブル

|Column|Type|Options|
|------|----|-------|
|title|string|null: false, foreign_key: true|

### Association
- belongs_to :taiketsu
- has_many   :comments

## commentsテーブル

|Column|Type|Options|
|------|----|-------|
|comment|text|null: false|
|good_count|integer||
|bad_count|integer||

### Association
- belongs_to :topic
