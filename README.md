# テーブル設計

## usersテーブル
| Column   | Type    | Options     |
| -------- | ------- | ----------- |
| name     | string  | null: false |
| age      | integer | null: false |
| email    | string  | null: false |
| password | string  | null: false |

### Asociation
- has_one :address

## addressesテーブル
| Column      | Type      | Options      |
| ----------- | --------- | ------------ |
| postal_code | integer   |              |
| address     | text      |              |
| user        | reference | option: true |

### Asociation
- belongs_to :user
