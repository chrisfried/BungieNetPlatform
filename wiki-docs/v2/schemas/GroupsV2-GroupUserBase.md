<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info

## Schema
* **Type:** Class

## Properties
Name | Type | Description
---- | ---- | -----------
groupId | integer:int64 | 
destinyUserInfo | [[UserInfoCard|User-UserInfoCard]] | 
bungieNetUserInfo | [[UserInfoCard|User-UserInfoCard]] | 
joinDate | string:date-time | 

## Example
```javascript
{
    // Type: integer:int64
    "groupId": 0,
    // Type: [[UserInfoCard|User-UserInfoCard]]
    "destinyUserInfo": {
        // Type: string
        "supplementalDisplayName": "",
        // Type: string
        "iconPath": "",
        // Type: [[BungieMembershipType|BungieMembershipType]]:Enum
        "membershipType": 0,
        // Type: integer:int64
        "membershipId": 0,
        // Type: string
        "displayName": ""
    },
    // Type: [[UserInfoCard|User-UserInfoCard]]
    "bungieNetUserInfo": {
        // Type: string
        "supplementalDisplayName": "",
        // Type: string
        "iconPath": "",
        // Type: [[BungieMembershipType|BungieMembershipType]]:Enum
        "membershipType": 0,
        // Type: integer:int64
        "membershipId": 0,
        // Type: string
        "displayName": ""
    },
    // Type: string:date-time
    "joinDate": ""
}

```

## References
1. https://bungie-net.github.io/multi/schema_GroupsV2-GroupUserBase.html#schema_GroupsV2-GroupUserBase