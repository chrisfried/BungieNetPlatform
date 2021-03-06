<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
When an inventory item (DestinyInventoryItemDefinition) has Stats (such as Attack Power), the item will refer to a Stat Group. This definition enumerates the properties used to transform the item's &quot;Investment&quot; stats into &quot;Display&quot; stats. See DestinyStatDefinition's documentation for information about the transformation of Stats, and the meaning of an Investment vs. a Display stat. If you don't want to do these calculations on your own, fear not: pulling live data from the BNet endpoints will return display stat values pre-computed and ready for you to use. I highly recommend this approach, saves a lot of time and also accounts for certain stat modifiers that can't easily be accounted for without live data (such as stat modifiers on Talent Grids and Socket Plugs)

## Schema
* **Schema Type:** Manifest Definition
* **Type:** object
* **Mobile Manifest:** StatGroups

## Properties
Name | Type | Description
---- | ---- | -----------
maximumValue | integer:int32 | The maximum possible value that any stat in this group can be transformed into. This is used by stats that *don't* have scaledStats entries below, but that still need to be displayed as a progress bar, in which case this is used as the upper bound for said progress bar. (the lower bound is always 0)
uiPosition | integer:int32 | This apparently indicates the position of the stats in the UI? I've returned it in case anyone can use it, but it's not of any use to us on BNet. Something's being lost in translation with this value.
scaledStats | [[DestinyStatDisplayDefinition|Destiny-Definitions-DestinyStatDisplayDefinition]]:Definition[] | Any stat that requires scaling to be transformed from an &quot;Investment&quot; stat to a &quot;Display&quot; stat will have an entry in this list. For more information on what those types of stats mean and the transformation process, see DestinyStatDefinition. In retrospect, I wouldn't mind if this was a dictionary keyed by the stat hash instead. But I'm going to leave it be because [[After Apple Picking]].
overrides | Dictionary&lt;integer:uint32,[[DestinyStatOverrideDefinition|Destiny-Definitions-DestinyStatOverrideDefinition]]:Definition&gt; | The game has the ability to override, based on the stat group, what the localized text is that is displayed for Stats being shown on the item. Mercifully, no Stat Groups use this feature currently. If they start using them, we'll all need to start using them (and those of you who are more prudent than I am can go ahead and start pre-checking for this.)
hash | integer:uint32 | The unique identifier for this entity. Guaranteed to be unique for the type of entity, but not globally. When entities refer to each other in Destiny content, it is this hash that they are referring to.
index | integer:int32 | The index of the entity as it was found in the investment tables.
redacted | boolean | If this is true, then there is an entity with this identifier/type combination, but BNet is not yet allowed to show it. Sorry!

## Example
```javascript
{
    // Type: integer:int32
    "maximumValue": 0,
    // Type: integer:int32
    "uiPosition": 0,
    // Type: [[DestinyStatDisplayDefinition|Destiny-Definitions-DestinyStatDisplayDefinition]]:Definition[]
    "scaledStats": [
       // Type: [[DestinyStatDisplayDefinition|Destiny-Definitions-DestinyStatDisplayDefinition]]:Definition
        {
            // Type: [[Destiny.Definitions.DestinyStatDefinition|Destiny-Definitions-DestinyStatDefinition]]:integer:uint32
            "statHash": 0,
            // Type: integer:int32
            "maximumValue": 0,
            // Type: boolean
            "displayAsNumeric": false,
            // Type: [[InterpolationPoint|Interpolation-InterpolationPoint]][]
            "displayInterpolation": [
               // Type: [[InterpolationPoint|Interpolation-InterpolationPoint]]
                {
                    // Type: integer:int32
                    "value": 0,
                    // Type: integer:int32
                    "weight": 0
                }
            ]
        }
    ],
    // Type: Dictionary&lt;integer:uint32,[[DestinyStatOverrideDefinition|Destiny-Definitions-DestinyStatOverrideDefinition]]:Definition&gt;
    "overrides": {
        "0": {
            // Type: [[Destiny.Definitions.DestinyStatDefinition|Destiny-Definitions-DestinyStatDefinition]]:integer:uint32
            "statHash": 0,
            // Type: [[DestinyDisplayPropertiesDefinition|Destiny-Definitions-Common-DestinyDisplayPropertiesDefinition]]:Definition
            "displayProperties": {}
        }
    },
    // Type: integer:uint32
    "hash": 0,
    // Type: integer:int32
    "index": 0,
    // Type: boolean
    "redacted": false
}

```

## References
1. https://bungie-net.github.io/multi/schema_Destiny-Definitions-DestinyStatGroupDefinition.html#schema_Destiny-Definitions-DestinyStatGroupDefinition
