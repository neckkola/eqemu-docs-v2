# account_flags

## Relationships

```mermaid
erDiagram
    account_flags {
        intunsigned p_accid
    }
    account {
        int id
        varchar name
    }
    account_flags ||--o{ account : "One-to-One"


```


| Relationship Type | Local Key | Relates to Table | Foreign Key |
| :--- | :--- | :--- | :--- |
| One-to-One | p_accid | [account](../../schema/account/account.md) | id |


## Schema

| Column | Data Type | Description |
| :--- | :--- | :--- |
| p_accid | int | [Account Identifier](account.md) |
| p_flag | varchar | Name |
| p_value | varchar | Value |

