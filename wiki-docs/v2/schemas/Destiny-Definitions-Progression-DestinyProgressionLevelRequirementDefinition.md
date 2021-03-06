<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
These are pre-constructed collections of data that can be used to determine the Level Requirement for an item given a Progression to be tested (such as the Character's level). For instance, say a character receives a new Auto Rifle, and that Auto Rifle's DestinyInventoryItemDefinition.quality.progressionLevelRequirementHash property is pointing at one of these DestinyProgressionLevelRequirementDefinitions. Let's pretend also that the progressionHash it is pointing at is the Character Level progression. In that situation, the character's level will be used to interpolate a value in the requirementCurve property. The value picked up from that interpolation will be the required level for the item.

## Schema
* **Schema Type:** Manifest Definition
* **Type:** object
* **Mobile Manifest:** ProgressionLevelRequirements

## Properties
Name | Type | Description
---- | ---- | -----------
requirementCurve | [[InterpolationPointFloat|Interpolation-InterpolationPointFloat]][] | A curve of level requirements, weighted by the related progressions' level. Interpolate against this curve with the character's progression level to determine what the level requirement of the generated item that is using this data will be.
progressionHash | [[Destiny.Definitions.DestinyProgressionDefinition|Destiny-Definitions-DestinyProgressionDefinition]]:integer:uint32 | The progression whose level should be used to determine the level requirement. Look up the DestinyProgressionDefinition with this hash for more information about the progression in question.
hash | integer:uint32 | The unique identifier for this entity. Guaranteed to be unique for the type of entity, but not globally. When entities refer to each other in Destiny content, it is this hash that they are referring to.
index | integer:int32 | The index of the entity as it was found in the investment tables.
redacted | boolean | If this is true, then there is an entity with this identifier/type combination, but BNet is not yet allowed to show it. Sorry!

## Example
```javascript
{
    // Type: [[InterpolationPointFloat|Interpolation-InterpolationPointFloat]][]
    "requirementCurve": [
       // Type: [[InterpolationPointFloat|Interpolation-InterpolationPointFloat]]
        {
            // Type: number:float
            "value": 0,
            // Type: number:float
            "weight": 0
        }
    ],
    // Type: [[Destiny.Definitions.DestinyProgressionDefinition|Destiny-Definitions-DestinyProgressionDefinition]]:integer:uint32
    "progressionHash": 0,
    // Type: integer:uint32
    "hash": 0,
    // Type: integer:int32
    "index": 0,
    // Type: boolean
    "redacted": false
}

```

## References
1. https://bungie-net.github.io/multi/schema_Destiny-Definitions-Progression-DestinyProgressionLevelRequirementDefinition.html#schema_Destiny-Definitions-Progression-DestinyProgressionLevelRequirementDefinition
