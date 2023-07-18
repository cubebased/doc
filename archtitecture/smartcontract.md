# Contract Interface Overview

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
Type: `activateuser`
Ricardian Contract: ``

### addccomment
Type: `addccomment`
Ricardian Contract: ``

### addcomment
Type: `addcomment`
Ricardian Contract: ``

### addcooldown
Type: `addcooldown`
Ricardian Contract: ``

### addtag
Type: `addtag`
Ricardian Contract: ``

### addtruster
Type: `addtruster`
Ricardian Contract: ``

### addupload
Type: `addupload`
Ricardian Contract: ``

### banuser
Type: `banuser`
Ricardian Contract: ``

### betruster
Type: `betruster`
Ricardian Contract: ``

### claimrewards
Type: `claimrewards`
Ricardian Contract: ``

### delupload
Type: `delupload`
Ricardian Contract: ``

### init
Type: `init`
Ricardian Contract: ``

### remcooldown
Type: `remcooldown`
Ricardian Contract: ``

### reportupload
Type: `reportupload`
Ricardian Contract: ``

### trustervote
Type: `trustervote`
Ricardian Contract: ``

### voteupload
Type: `voteupload`
Ricardian Contract: ``

## Tables

### badges
Type: `badges`
Index Type: `i64`
Key Names: ``
Key Types: ``

### comments
Type: `comments`
Index Type: `i64`
Key Names: ``
Key Types: ``

### configs
Type: `configs`
Index Type: `i64`
Key Names: ``
Key Types: ``

### cooldown
Type: `cooldown`
Index Type: `i64`
Key Names: ``
Key Types: ``

### globaltags
Type: `globaltags`
Index Type: `i64`
Key Names: ``
Key Types: ``

### reports
Type: `report`
Index Type: `i64`
Key Names: ``
Key Types: ``

### reportvotes
Type: `reportvote`
Index Type: `i64`
Key Names: ``
Key Types: ``

### tags
Type: `tags`
Index Type: `i64`
Key Names: ``
Key Types: ``

### trusters
Type: `truster`
Index Type: `i64`
Key Names: ``
Key Types: ``

### uploads
Type: `uploads`
Index Type: `i64`
Key Names: ``
Key Types: ``

### userbadge
Type: `userbadge`
Index Type: `i64`
Key Names: ``
Key Types: ``

### userconfig
Type: `userconfig`
Index Type: `i64`
Key Names: ``
Key Types: ``

### userfavorite
Type: `userfavorite`
Index Type: `i64`
Key Names: ``
Key Types: ``

### useruploads
Type: `useruploads`
Index Type: `i64`
Key Names: ``
Key Types: ``

### votecomments
Type: `votecomments`
Index Type: `i64`
Key Names: ``
Key Types: ``

### votetags
Type: `votetags`
Index Type: `i64`
Key Names: ``
Key Types: ``

### voteuploads
Type: `voteuploads`
Index Type: `i64`
Key Names: ``
Key Types: ``

### withthistag
Type: `withthistag`
Index Type: `i64`
Key Names: ``
Key Types: ``
