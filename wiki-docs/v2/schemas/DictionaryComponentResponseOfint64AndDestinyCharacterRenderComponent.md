<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info

## Schema
* **Type:** Generic

## Properties
Name | Type | Description
---- | ---- | -----------
data | Dictionary&lt;integer:int64,[[DestinyCharacterRenderComponent|Destiny-Entities-Characters-DestinyCharacterRenderComponent]]&gt; | 
privacy | [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum | 

## Example
```javascript
{
    // Type: Dictionary&lt;integer:int64,[[DestinyCharacterRenderComponent|Destiny-Entities-Characters-DestinyCharacterRenderComponent]]&gt;
    "data": {
        "0": {
            // Type: [[DyeReference|Destiny-DyeReference]][]
            "customDyes": [
               // Type: [[DyeReference|Destiny-DyeReference]]
                {
                    // Type: integer:uint32
                    "channelHash": 0,
                    // Type: integer:uint32
                    "dyeHash": 0
                }
            ],
            // Type: [[DestinyCharacterCustomization|Destiny-Character-DestinyCharacterCustomization]]
            "customization": {
                // Type: integer:uint32
                "personality": 0,
                // Type: integer:uint32
                "face": 0,
                // Type: integer:uint32
                "skinColor": 0,
                // Type: integer:uint32
                "lipColor": 0,
                // Type: integer:uint32
                "eyeColor": 0,
                // Type: integer:uint32[]
                "hairColors": [
                   // Type: integer:uint32
                    0
                ],
                // Type: integer:uint32[]
                "featureColors": [
                   // Type: integer:uint32
                    0
                ],
                // Type: integer:uint32
                "decalColor": 0,
                // Type: boolean
                "wearHelmet": false,
                // Type: integer:int32
                "hairIndex": 0,
                // Type: integer:int32
                "featureIndex": 0,
                // Type: integer:int32
                "decalIndex": 0
            },
            // Type: [[DestinyCharacterPeerView|Destiny-Character-DestinyCharacterPeerView]]
            "peerView": {
                // Type: [[DestinyItemPeerView|Destiny-Character-DestinyItemPeerView]][]
                "equipment": [
                   // Type: [[DestinyItemPeerView|Destiny-Character-DestinyItemPeerView]]
                    {
                        // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                        "itemHash": 0,
                        // Type: [[DyeReference|Destiny-DyeReference]][]
                        "dyes": [
                           // Type: [[DyeReference|Destiny-DyeReference]]
                            {
                                // Type: integer:uint32
                                "channelHash": 0,
                                // Type: integer:uint32
                                "dyeHash": 0
                            }
                        ]
                    }
                ]
            }
        }
    },
    // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
    "privacy": 0
}

```

## References
1. https://bungie-net.github.io/multi/schema_DictionaryComponentResponseOfint64AndDestinyCharacterRenderComponent.html#schema_DictionaryComponentResponseOfint64AndDestinyCharacterRenderComponent