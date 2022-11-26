---
order: 84
label: Smart Contract
icon: file-badge
tags: [architecture]
---

# Cbased Contract

The Cbased contract is the main contract and consists of these functions:

## activateuser

This action active a user for the cbased contract.
Users who are not activated cannot perform any action in the cbased contract

Required authorization: cbased

Parameter:

| name | type  |
|---|---|
| username | name |

#  addcomment

This action add a comment to a specific upload

Required authorization: any active user

Parameter:

| name | type  |
|---|---|
| autor | name | 
| text | string | 
| uploadid | uint64 | 

## addccomment

This action add a comment to a comment.

Required authorization: any active user

Parameter:

| name | type  |
|---|---|
| autor | name | 
| text | string | 
| uploadid | uint64 | 
| parentcommentid | uint64 |


- addcooldown
- addtag
- addtruster
- addupload
- banuser
- betruster
- claimrewards
- delupload
- init
- remcooldown
- reportupload
- trustervote
- voteupload

## Action

