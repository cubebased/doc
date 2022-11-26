---
order: 84
label: Smart Contract
icon: file-badge
tags: [architecture]
---

# Cbased Contract

The Cbased contract is the main contract and consists of functions and tables.

You can find a list of all data types [here](https://eosio.stackexchange.com/questions/1837/list-of-available-datatypes-for-action-parameter)

The order of the parameters is crucial for the integration with the Smart Contract. The order in the table corresponds to the order of the parameters.

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

This action add a new upload into the [Upload Table](#uploads).

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

This action delete the selected upload. In addition, all comments and tags will be deleted for this upload.

Required authorization: cbased

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

This action add a tag to a upload. This action effects the [Tag Table](#tags) and [withthistag Table](#withthistag). If the transmitted tagtext is also new in a global scope the [Global Tag Table](#globaltags) will be also effected.

Required authorization: any active user

| Parametername | type |
|---|---|
| autor | name | 
| uploadid | uint64 | 
| text | string |

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

### tags

| Parametername | type |
|---|---|
| tagid | uint64 | 
| text | string |
| autor | name | 
| token | int32 | 


### globaltags

| Parametername | type |
|---|---|
| globaltagid | uint64 | 
| text | string |

### withthistag

| Parametername | type |
|---|---|
| uploadid | uint64 | 






