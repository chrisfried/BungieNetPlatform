<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
Unbans the requested member, allowing them to re-apply for membership.

* **URI:** [[/GroupV2/{groupId}/Members/{membershipType}/{membershipId}/Unban/|https://www.bungie.net/Platform/GroupV2/{groupId}/Members/{membershipType}/{membershipId}/Unban/]]
* **Basepath:** https://www.bungie.net/Platform
* **Method:** POST
* **Service:** [[GroupV2|Endpoints#GroupV2]]
* **Permissions:** AdminGroups
* **Officially Supported:** Yes

## Parameters
### Path Parameters
Name | Schema | Required | Description
---- | ------ | -------- | -----------
groupId | integer:int64 | Yes | 
membershipId | integer:int64 | Yes | Membership ID of the member to unban from the group
membershipType | [[BungieMembershipType|BungieMembershipType]]:Enum | Yes | Membership type of the provided membership ID.

### Query String Parameters
None

## Example
### Request
POST https://www.bungie.net/Platform/GroupV2/{groupId}/Members/{membershipType}/{membershipId}/Unban/

### Response
PlatformErrorCode: 200
```javascript
{
    // Type: integer:int32
    "Response": 0,
    // Type: [[PlatformErrorCodes|Exceptions-PlatformErrorCodes]]:Enum
    "ErrorCode": 0,
    // Type: integer:int32
    "ThrottleSeconds": 0,
    // Type: string
    "ErrorStatus": "",
    // Type: string
    "Message": "",
    // Type: Dictionary&lt;string,string&gt;
    "MessageData": {
        "{string}": ""
    },
    // Type: object
}

```

## References
1. https://bungie-net.github.io/multi/operation_post_GroupV2-UnbanMember.html#operation_post_GroupV2-UnbanMember
