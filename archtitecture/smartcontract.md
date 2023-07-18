---
order: 84
label: Smart Contract
icon: file-badge
tags: [architecture]
---

# Cbased Contract
The account with the accountname Cbased is the main contract and consists of functions and tables. The order of the parameters is crucial for the integration with the Smart Contract. The developing of the cbased contract is still in process.

## Structs

### activateuser
- **username**: `name`

### addccomment
- **autor**: `name`
- **text**: `string`
- **uploadid**: `uint64`
- **parentcommentid**: `uint64`

### addcomment
- **autor**: `name`
- **text**: `string`
- **uploadid**: `uint64`

### addcooldown
- **autor**: `name`
- **action**: `uint16`

### addtag
- **autor**: `name`
- **uploadid**: `uint64`
- **text**: `string`

### addtruster
- **trustername**: `name`

### addupload
- **autor**: `name`
- **ipfshash**: `string`
- **ipfshash_thumb**: `string`
- **uploadtext**: `string`
- **filetyp**: `string`
- **flag**: `uint8`

### badges
- **badgeid**: `uint64`
- **badgetext**: `string`
- **creationtime**: `time_point`
- **ipfshash**: `string`
- **ipfshash_thumb**: `string`
- **filetyp**: `string`

### banuser
- **username**: `name`

### betruster
- **autor**: `name`
- **applicationtimeinweek**: `uint8`

### claimrewards
- **autor**: `name`
- **symbol**: `string`
- **value**: `uint64`

### comments
- **commentid**: `uint64`
- **parentcommentid**: `uint64`
- **autor**: `name`
- **creationtime**: `time_point`
- **uploadid**: `uint64`
- **commenttext**: `string`
- **token**: `int32`

### configs
- **configid**: `uint64`
- **uintvalue**: `uint64`
- **stringvalue**: `string`

### cooldown
- **cooldownid**: `uint64`
- **user**: `name`
- **action**: `uint16`
- **counter**: `uint16`
- **lastaction**: `time_point`

### delupload
- **uploadid**: `uint64`

### globaltags
- **globaltagid**: `uint64`
- **text**: `string`

### init
- **value**: `uint16`

### remcooldown
- **autor**: `name`
- **action**: `uint16`

### report
- **uploadid**: `uint64`
- **reportername**: `uint64`
- **violatedrule**: `uint8`
- **reporttime**: `time_point`
- **numberoftrusters**: `uint8`
- **outstandingvotes**: `uint8`
- **vote_weight**: `int8`

### reportupload
- **autor**: `name`
- **uploadid**: `uint64`
- **violatedrule**: `uint8`

### reportvote
- **trustername**: `uint64`
- **vote**: `int8`

### tags
- **tagid**: `uint64`
- **text**: `string`
- **autor**: `name`
- **token**: `int32`

### truster
- **trustername**: `uint64`
- **karma**: `uint16`
- **status**: `uint8`
- **election_date**: `time_point`

### trustervote
- **trustername**: `name`
- **uploadid**: `uint64`
- **vote**: `int8`

### uploads
- **uploadid**: `uint64`
- **autor**: `name`
- **creationtime**: `time_point`
- **ipfshash**: `string`
- **ipfshash_filetyp**: `string`
- **ipfshash_thumb**: `string`
- **uploadtext**: `string`
- **flag**: `uint8`
- **token**: `int32`

### userbadge
- **userbadgeid**: `uint64`
- **user**: `name`
- **badgeid**: `uint64`
- **handover**: `time_point`

### userconfig
- **configid**: `uint64`
- **active**: `uint8`
- **last_act_reset**: `time_point`
- **act_token**: `uint16`
- **last_claim_time**: `time_point`

### userfavorite
- **id**: `uint64`
- **uploadid**: `uint64`

### useruploads
- **id**: `uint64`
- **uploadid**: `uint64`

### votecomments
- **votecommentsid**: `uint64`
- **commentsid**: `uint64`
- **autor**: `name`
- **vote**: `int8`

### votetags
- **votetagsid**: `uint64`
- **tagid**: `uint64`
- **autor**: `name`
- **vote**: `int8`

### voteupload
- **autor**: `name`
- **vote**: `int8`
- **uploadid**: `uint64`

### voteuploads
- **uploadid**: `uint64`
- **vote**: `int8`

### withthistag
- **uploadid**: `uint64`

## Actions

### activateuser

### addccomment

### addcomment

### addcooldown

### addtag

### addtruster

### addupload

### banuser

### betruster

### claimrewards

### delupload

### init

### remcooldown

### reportupload

### trustervote

### voteupload

## Tables

### badges

### comments

### configs

### cooldown

### globaltags

### reports

### reportvotes

### tags

### trusters

### uploads

### userbadge

### userconfig

### userfavorite

### useruploads

### votecomments

### votetags

### voteuploads

### withthistag
