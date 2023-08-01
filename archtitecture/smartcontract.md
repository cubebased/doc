---
order: 84
label: Smart Contract
icon: file-badge
tags: [architecture]
---

# Cbased Contract
The account with the accountname Cbased is the main contract and consists of functions and tables. The order of the parameters is crucial for the integration with the Smart Contract. The developing of the cbased contract is still in process.
## Actions
### activateuser
Type: activateuser

  - **username** (name)

### addccomment
Type: addccomment

  - **autor** (name)
  - **text** (string)
  - **uploadid** (uint64)
  - **parentcommentid** (uint64)

### addcomment
Type: addcomment

  - **autor** (name)
  - **text** (string)
  - **uploadid** (uint64)

### addcooldown
Type: addcooldown

  - **autor** (name)
  - **action** (uint16)

### addfavorite
Type: addfavorite

  - **autor** (name)
  - **uploadid** (uint64)

### addfavotag
Type: addfavotag

  - **autor** (name)
  - **globaltagid** (uint64)

### addtag
Type: addtag

  - **autor** (name)
  - **uploadid** (uint64)
  - **text** (string)

### addtruster
Type: addtruster

  - **trustername** (name)

### addupload
Type: addupload

  - **autor** (name)
  - **ipfshash** (string)
  - **ipfshash_thumb** (string)
  - **uploadtext** (string)
  - **filetyp** (string)
  - **flag** (uint8)

### banuser
Type: banuser

  - **username** (name)

### betruster
Type: betruster

  - **autor** (name)
  - **applicationtimeinweek** (uint8)

### claimrewards
Type: claimrewards

  - **autor** (name)
  - **symbol** (string)
  - **value** (uint64)

### deldm
Type: deldm

  - **autor** (name)
  - **dmid** (uint64)

### delfavorite
Type: delfavorite

  - **autor** (name)
  - **uploadid** (uint64)

### delfavotag
Type: delfavotag

  - **autor** (name)
  - **globaltagid** (uint64)

### delupload
Type: delupload

  - **uploadid** (uint64)

### init
Type: init

  - **value** (uint16)

### remcooldown
Type: remcooldown

  - **autor** (name)
  - **action** (uint16)

### reportupload
Type: reportupload

  - **autor** (name)
  - **uploadid** (uint64)
  - **violatedrule** (uint8)

### senddm
Type: senddm

  - **from** (name)
  - **to** (name)
  - **message** (string)

### trustervote
Type: trustervote

  - **trustername** (name)
  - **uploadid** (uint64)
  - **vote** (int8)

### voteupload
Type: voteupload

  - **autor** (name)
  - **vote** (int8)
  - **uploadid** (uint64)

## Tables
### badges
Type: badges

  - **badgeid** (uint64)
  - **badgetext** (string)
  - **creationtime** (time_point)
  - **ipfshash** (string)
  - **ipfshash_thumb** (string)
  - **filetyp** (string)

### comments
Type: comments

  - **commentid** (uint64)
  - **parentcommentid** (uint64)
  - **autor** (name)
  - **creationtime** (time_point)
  - **uploadid** (uint64)
  - **commenttext** (string)
  - **token** (int32)

### configs
Type: configs

  - **configid** (uint64)
  - **uintvalue** (uint64)
  - **stringvalue** (string)

### cooldown
Type: cooldown

  - **cooldownid** (uint64)
  - **user** (name)
  - **action** (uint16)
  - **counter** (uint16)
  - **lastaction** (time_point)

### dms
Type: dm

  - **messageid** (uint64)
  - **creationtime** (time_point)
  - **autor** (name)
  - **messagetext** (string)

### globaltags
Type: globaltags

  - **globaltagid** (uint64)
  - **numoffavorites** (uint32)
  - **text** (string)

### notifys
Type: notify

  - **notificationid** (uint64)
  - **creationtime** (time_point)
  - **type** (uint16)
  - **notificationtext** (string)

### reports
Type: report

  - **uploadid** (uint64)
  - **reportername** (uint64)
  - **violatedrule** (uint8)
  - **reporttime** (time_point)
  - **numberoftrusters** (uint8)
  - **outstandingvotes** (uint8)
  - **vote_weight** (int8)

### reportvotes
Type: reportvote

  - **trustername** (uint64)
  - **vote** (int8)

### tags
Type: tags

  - **tagid** (uint64)
  - **text** (string)
  - **autor** (name)
  - **token** (int32)

### trusters
Type: truster

  - **trustername** (uint64)
  - **karma** (uint16)
  - **status** (uint8)
  - **election_date** (time_point)

### uploads
Type: uploads

  - **uploadid** (uint64)
  - **autor** (name)
  - **creationtime** (time_point)
  - **ipfshash** (string)
  - **ipfshash_filetyp** (string)
  - **ipfshash_thumb** (string)
  - **uploadtext** (string)
  - **flag** (uint8)
  - **numofcomments** (uint32)
  - **numoffavorites** (uint32)
  - **token** (int32)

### userbadge
Type: userbadge

  - **userbadgeid** (uint64)
  - **user** (name)
  - **badgeid** (uint64)
  - **handover** (time_point)

### userconfig
Type: userconfig

  - **configid** (uint64)
  - **active** (uint8)
  - **last_act_reset** (time_point)
  - **act_token** (uint16)
  - **last_claim_time** (time_point)

### userfavorite
Type: userfavorite

  - **uploadid** (uint64)

### userfavotags
Type: userfavotag

  - **globaltagid** (uint64)

### useruploads
Type: userupload

  - **id** (uint64)
  - **uploadid** (uint64)

### votecomments
Type: votecomments

  - **votecommentsid** (uint64)
  - **commentsid** (uint64)
  - **autor** (name)
  - **vote** (int8)

### votetags
Type: votetags

  - **votetagsid** (uint64)
  - **tagid** (uint64)
  - **autor** (name)
  - **vote** (int8)

### voteuploads
Type: voteuploads

  - **uploadid** (uint64)
  - **vote** (int8)

### withthistag
Type: withthistag

  - **uploadid** (uint64)

