<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
Items that can be equipped define this block.  It contains information we need tounderstand how and when the item can be equipped.

## Schema
* **Type:** Definition

## Properties
Name | Type | Description
---- | ---- | -----------
gearsetItemHash | [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32:nullable | If the item is part of a gearset, this is a reference to that gearset item.
uniqueLabel | string | If defined, this is the label used to check if the item has other items ofmatching types already equipped. For instance, when you aren't allowed toequip more than one Exotic Weapon, that's because all exotic weapons haveidentical uniqueLabels and the game checks the to-be-equipped item's uniqueLabelvs. all other already equipped items (other than the item in the slot that'sabout to be occupied).
uniqueLabelHash | integer:uint32 | The hash of that unique label.  Does not point to a specific definition.
equipmentSlotTypeHash | [[DestinyEquipmentSlotDefinition|Destiny-Definitions-DestinyEquipmentSlotDefinition]]:Definition:integer:uint32 | An equipped item *must* be equipped in an Equipment Slot.  This is the hash identifierof the DestinyEquipmentSlotDefinition into which it must be equipped.
attributes | [[EquippingItemBlockAttributes|Destiny-EquippingItemBlockAttributes]]:Enum | These are custom attributes on the equippability of the item. For now, this can only be &quot;equip on acquire&quot;, which would mean that the itemwill be automatically equipped as soon as you pick it up.
displayStrings | string[] | These are strings that represent the possible Game/Account/Character state failure conditionsthat can occur when trying to equip the item.  They match up one-to-one with requiredUnlockExpressions.

## Example
```javascript
{
    // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32:nullable
    "gearsetItemHash": 0,
    // Type: string
    "uniqueLabel": "",
    // Type: integer:uint32
    "uniqueLabelHash": 0,
    // Type: [[DestinyEquipmentSlotDefinition|Destiny-Definitions-DestinyEquipmentSlotDefinition]]:Definition:integer:uint32
    "equipmentSlotTypeHash": 0,
    // Type: [[EquippingItemBlockAttributes|Destiny-EquippingItemBlockAttributes]]:Enum
    "attributes": 0,
    // Type: string[]
    "displayStrings": [
       // Type: string
        ""
    ]
}

```

## References
1. https://bungie-net.github.io/multi/schema_Destiny-Definitions-DestinyEquippingBlockDefinition.html#schema_Destiny-Definitions-DestinyEquippingBlockDefinition