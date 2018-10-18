# README

## taiketsusテーブル

|Column|Type|Options|
|------|----|-------|
|topic_id1|text|null: false, foreign_key: true|
|topic_id2|text|null: false, foreign_key: true|

### Association
- has_one :topic

## topicsテーブル

|Column|Type|Options|
|------|----|-------|
|title|string|null: false|
|taiketsu_id|string|null: false|

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
