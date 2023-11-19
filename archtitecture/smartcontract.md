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
  - **parentcommentid** (uint64)
  - **language** (string)

### addcomment
Type: addcomment

  - **autor** (name)
  - **text** (string)
  - **uploadid** (uint64)
  - **language** (string)

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

### addsubscrip
Type: addsubscrip

  - **autor** (name)
  - **follow** (name)

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
  - **language** (string)
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

### delsubscrip
Type: delsubscrip

  - **autor** (name)
  - **unfollow** (name)

### delupload
Type: delupload

  - **uploadid** (uint64)

### init
Type: init


### remcooldown
Type: remcooldown

  - **autor** (name)
  - **action** (uint16)

### reportupload
Type: reportupload

  - **autor** (name)
  - **uploadid** (uint64)
  - **violatedrule** (uint8)

### run
Type: run


### senddm
Type: senddm

  - **from** (name)
  - **to** (name)
  - **message** (string)

### setprofile
Type: setprofile

  - **autor** (name)
  - **profilebio** (string)
  - **profileimageipfs** (string)
  - **profileimagefiletyp** (string)
  - **language** (string)
  - **otherconfigsasjson** (string)

### trustervote
Type: trustervote

  - **trustername** (name)
  - **uploadid** (uint64)
  - **vote** (int8)

### votecomment
Type: votecomment

  - **autor** (name)
  - **vote** (int8)
  - **commentid** (uint64)

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
  - **language** (string)
  - **commenttext** (string)
  - **token** (int32)
  - **up** (uint32)
  - **down** (uint32)

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
  - **numoffavorites** (uint64)
  - **text** (string)

### globcomments
Type: globcomments

  - **commentid** (uint64)
  - **uploadid** (uint64)

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

### stats
Type: stats

  - **id** (uint64)
  - **text** (string)
  - **time** (time_point)
  - **uint64number** (uint64)
  - **int64number** (int64)

### tags
Type: tags

  - **tagid** (uint64)
  - **text** (string)
  - **autor** (name)
  - **token** (int32)

### todelete
Type: todelete

  - **id** (uint64)
  - **timetodelete** (time_point_sec)
  - **uploadid** (uint64)

### trends
Type: trend

  - **trendid** (uint64)
  - **uploadid** (uint64)
  - **creationtime** (time_point)

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
  - **language** (string)
  - **flag** (uint8)
  - **numofcomments** (uint32)
  - **numoffavorites** (uint32)
  - **token** (uint64)
  - **up** (uint32)
  - **down** (uint32)
  - **trendid** (uint64)

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
  - **numofsubscribtions** (uint16)
  - **numoffollowers** (uint16)
  - **profilebio** (string)
  - **profileimageipfs** (string)
  - **profileimagefiletyp** (string)
  - **language** (string)
  - **otherconfigsasjson** (string)

### userfavorite
Type: userfavorite

  - **uploadid** (uint64)
  - **creationtime** (time_point)

### userfavotags
Type: userfavotag

  - **globaltagid** (uint64)

### usersubscrip
Type: usersubscrip

  - **subscriptionid** (uint64)
  - **username** (name)
  - **creationtime** (time_point)

### useruploads
Type: userupload

  - **id** (uint64)
  - **uploadid** (uint64)

### votecomments
Type: votecomments

  - **commentid** (uint64)
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
