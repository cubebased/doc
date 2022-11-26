---
order: 84
label: Smart Contract
icon: file-badge
tags: [architecture]
---

# Cbased Contract

The Cbased contract is the main contract and consists of functions and tables.

You can find a list of all data types [here](https://eosio.stackexchange.com/questions/1837/list-of-available-datatypes-for-action-parameter)

## Actions

### activateuser

This action active a user for the cbased contract.
Users who are not activated cannot perform any action in the cbased contract

Required authorization: cbased

| Parametername | type  |
|---|---|
| username | name |

### banuser

This action ban and deactive a user for the cbased contract. **This change cannot be undone.** Users can not longer perform any action in the cbased contract.

Required authorization: cbased

| Parametername | type  |
|---|---|
| username | name |


### addupload

This action add a new upload into the [Upload Table](###uploads).

Required authorization: any active user

| Parametername | type |
|---|---|
| autor | name | 
| ipfshash | string | 
| ipfshash_thumb | string |
| uploadtext | string |
| filetyp | string |
| flag | uint8 |

### delupload

### addcomment

This action add a comment to a specific upload

Required authorization: any active user

| Parametername | type |
|---|---|
| autor | name | 
| text | string | 
| uploadid | uint64 | 

### addccomment

This action add a comment to a comment.

Required authorization: any active user

| Parametername | type |
|---|---|
| autor | name | 
| text | string | 
| uploadid | uint64 | 
| parentcommentid | uint64 |


### addtag
### addtruster
### betruster
### claimrewards

### addcooldown
### remcooldown

### trustervote
### reportupload

### voteupload

### Action

## Tables


### uploads

| Parametername | type |
|---|---|
| uploadid | uint64 | 
| autor | name | 
| creationtime | time_point | 
| ipfshash | string |
| ipfshash_filetyp | string |
| ipfshash_thumb | string |
| uploadtext | string |
| flag | uint8 |
| token | int32 |


