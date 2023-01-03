---
order: 84
label: Smart Contract
icon: file-badge
tags: [architecture]
---

# Cbased Contract

The account with the accountname Cbased is the main contract and consists of functions and tables. The order of the parameters is crucial for the integration with the Smart Contract. The developing of the cbased contract is still in process.

## Contact Overview & Status: ##

| Action_name | [Contract_Status](#Contract_Status)
|---|---|---|
| [activateuser](#activateuser) | :icon-tools: |
| [addccomment](#addccomment) | :icon-tools: |
| [addcomment](#addcomment) | :icon-tools: |
| [addcooldown](#addcooldown) | :icon-tools: |
| [addtag](#addtag) | :icon-tools: |
| [addtruster](#addtruster) | :icon-tools: |
| [addupload](#addupload) | :icon-tools: |
| [banuser](banuser) | :icon-tools: |
| [betruster](#betruster) | :icon-tools: |
| [claimrewards](#claimrewards) | :icon-tools: |
| [delupload](#delupload) | :icon-tools: |
| [remcooldown](#remcooldown) | :icon-tools: |
| [reportupload](#reportupload) | :icon-tools: |
| [trustervote](#trustervote) | :icon-tools: |
| [voteupload](#voteupload) | :icon-tools: |


## Contract_Status

| Level | Status | Descrition |
|---|---|---|
| 1 | :icon-issue-draft: | Todo. Developing not started yet |
| 2 | :icon-tools: | In developing |
| 3 | :icon-shield-check:  | Developing finished |
| 4 | :icon-verified: | code security reviewed |

## Actions

### activateuser

This action active a user for the cbased contract.
Users who are not activated cannot perform any action in the cbased contract

Required authorization: cbased

| Parametername | type  |
|---|---|
| username | name |

### addccomment

This action add a comment to a comment.

Required authorization: any active user

| Parametername | type |
|---|---|
| autor | name | 
| text | string | 
| uploadid | uint64 | 
| parentcommentid | uint64 |

### addcomment

This action add a comment to a specific upload

Required authorization: any active user

| Parametername | type |
|---|---|
| autor | name | 
| text | string | 
| uploadid | uint64 |


### addcooldown
### addtag

This action add a tag to a upload. This action effects the [Tag Table](#tags) and [withthistag Table](#withthistag). If the transmitted tagtext is also new in a global scope the [Global Tag Table](#globaltags) will be also effected.

Required authorization: any active user

| Parametername | type |
|---|---|
| autor | name | 
| uploadid | uint64 | 
| text | string |

### addtruster
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

### banuser
### betruster
### claimrewards
### delupload

This action delete the selected upload. In addition, all comments and tags will be deleted for this upload.

Required authorization: cbased

### remcooldown
### reportupload
### trustervote
### voteupload


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





You can find a list of all data types [here](https://eosio.stackexchange.com/questions/1837/list-of-available-datatypes-for-action-parameter)
