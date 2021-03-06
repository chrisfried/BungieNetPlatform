<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
This component holds activity data for a character. It will tell you about the character's current activity status, as well as activities that are available to the user.

## Schema
* **Schema Type:** Class
* **Type:** object
* **Component Type Dependency:** CharacterActivities

## Properties
Name | Type | Description
---- | ---- | -----------
dateActivityStarted | string:date-time | The last date that the user started playing an activity.
availableActivities | [[DestinyActivity|Destiny-DestinyActivity]][] | The list of activities that the user can play.
currentActivityHash | [[Destiny.Definitions.DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:integer:uint32 | If the user is in an activity, this will be the hash of the Activity being played. Note that you must combine this info with currentActivityModeHash to get a real picture of what the user is doing right now. For instance, PVP &quot;Activities&quot; are just maps: it's the ActivityMode that determines what type of PVP game they're playing.
currentActivityModeHash | [[Destiny.Definitions.DestinyActivityModeDefinition|Destiny-Definitions-DestinyActivityModeDefinition]]:integer:uint32 | If the user is in an activity, this will be the hash of the activity mode being played. Combine with currentActivityHash to give a person a full picture of what they're doing right now.
currentActivityModeType | [[Destiny.Definitions.DestinyActivityModeDefinition|Destiny-Definitions-DestinyActivityModeDefinition]]:integer:int32:nullable | And the current activity's most specific mode type, if it can be found.
currentActivityModeHashes | [[Destiny.Definitions.DestinyActivityModeDefinition|Destiny-Definitions-DestinyActivityModeDefinition]]:integer:uint32[] | If the user is in an activity, this will be the hashes of the DestinyActivityModeDefinition being played. Combine with currentActivityHash to give a person a full picture of what they're doing right now.
currentActivityModeTypes | [[DestinyActivityModeType|Destiny-HistoricalStats-Definitions-DestinyActivityModeType]]:Enum[] | All Activity Modes that apply to the current activity being played, in enum form.
currentPlaylistActivityHash | [[Destiny.Definitions.DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:integer:uint32:nullable | If the user is in a playlist, this is the hash identifier for the playlist that they chose.
lastCompletedStoryHash | [[Destiny.Definitions.DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:integer:uint32 | This will have the activity hash of the last completed story/campaign mission, in case you care about that.

## Example
```javascript
{
    // Type: string:date-time
    "dateActivityStarted": "",
    // Type: [[DestinyActivity|Destiny-DestinyActivity]][]
    "availableActivities": [
       // Type: [[DestinyActivity|Destiny-DestinyActivity]]
        {
            // Type: [[Destiny.Definitions.DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:integer:uint32
            "activityHash": 0,
            // Type: boolean
            "isNew": false,
            // Type: boolean
            "canLead": false,
            // Type: boolean
            "canJoin": false,
            // Type: boolean
            "isCompleted": false,
            // Type: boolean
            "isVisible": false,
            // Type: integer:int32:nullable
            "displayLevel": 0,
            // Type: integer:int32:nullable
            "recommendedLight": 0,
            // Type: [[DestinyActivityDifficultyTier|Destiny-DestinyActivityDifficultyTier]]:Enum
            "difficultyTier": {}
        }
    ],
    // Type: [[Destiny.Definitions.DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:integer:uint32
    "currentActivityHash": 0,
    // Type: [[Destiny.Definitions.DestinyActivityModeDefinition|Destiny-Definitions-DestinyActivityModeDefinition]]:integer:uint32
    "currentActivityModeHash": 0,
    // Type: [[Destiny.Definitions.DestinyActivityModeDefinition|Destiny-Definitions-DestinyActivityModeDefinition]]:integer:int32:nullable
    "currentActivityModeType": 0,
    // Type: [[Destiny.Definitions.DestinyActivityModeDefinition|Destiny-Definitions-DestinyActivityModeDefinition]]:integer:uint32[]
    "currentActivityModeHashes": [
       // Type: integer:uint32
        0
    ],
    // Type: [[DestinyActivityModeType|Destiny-HistoricalStats-Definitions-DestinyActivityModeType]]:Enum[]
    "currentActivityModeTypes": [
       // Type: [[DestinyActivityModeType|Destiny-HistoricalStats-Definitions-DestinyActivityModeType]]:Enum
        0
    ],
    // Type: [[Destiny.Definitions.DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:integer:uint32:nullable
    "currentPlaylistActivityHash": 0,
    // Type: [[Destiny.Definitions.DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:integer:uint32
    "lastCompletedStoryHash": 0
}

```

## References
1. https://bungie-net.github.io/multi/schema_Destiny-Entities-Characters-DestinyCharacterActivitiesComponent.html#schema_Destiny-Entities-Characters-DestinyCharacterActivitiesComponent
