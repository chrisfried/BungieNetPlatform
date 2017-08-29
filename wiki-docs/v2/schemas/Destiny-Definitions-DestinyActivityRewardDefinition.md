<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
Activities can refer to one or more sets of tooltip-friendly reward data.  These are the definitionsfor those tooltip friendly rewards.

## Schema
* **Type:** Definition

## Properties
Name | Type | Description
---- | ---- | -----------
rewardText | string | The header for the reward set, if any.
rewardItems | [[DestinyItemQuantity|Destiny-DestinyItemQuantity]][] | The &quot;Items provided&quot; in the reward.  This is almost always a pointer to a DestinyInventoryItemDefintionfor an item that you can't actually earn in-game, but that has name/description/icon information forthe vague concept of the rewards you will receive.  This is because the actual reward generation isnon-deterministic and extremely complicated, so the best the game can do is tell you what you'll getin vague terms.  And so too shall we. Interesting trivia: you actually *do* earn these items when you complete the activity.  They go into a single-slotbucket on your profile, which is how you see the pop-ups of these rewards when you complete an activity that matchthese &quot;dummy&quot; items.  You can even see them if you look at the last one you earned in yourprofile-level inventory through the BNet API!  Who said reading documentation is a waste of time?

## Example
```javascript
{
    // Type: string
    "rewardText": "",
    // Type: [[DestinyItemQuantity|Destiny-DestinyItemQuantity]][]
    "rewardItems": [
       // Type: [[DestinyItemQuantity|Destiny-DestinyItemQuantity]]
        {
            // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
            "itemHash": 0,
            // Type: integer:int64:nullable
            "itemInstanceId": 0,
            // Type: integer:int32
            "quantity": 0
        }
    ]
}

```

## References
1. https://bungie-net.github.io/multi/schema_Destiny-Definitions-DestinyActivityRewardDefinition.html#schema_Destiny-Definitions-DestinyActivityRewardDefinition