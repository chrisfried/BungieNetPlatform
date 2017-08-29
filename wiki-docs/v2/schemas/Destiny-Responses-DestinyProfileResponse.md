<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
The response for GetDestinyProfile, with components for character and item-level data.

## Schema
* **Type:** Class

## Properties
Name | Type | Description
---- | ---- | -----------
vendorReceipts | [[SingleComponentResponse&lt;DestinyVendorReceiptsComponent&gt;|SingleComponentResponseOfDestinyVendorReceiptsComponent]] | Recent, refundable purchases you have made from vendors.  When will you use it?  Couldn't say... COMPONENT TYPE: VendorReceipts
profileInventory | [[SingleComponentResponse&lt;DestinyInventoryComponent&gt;|SingleComponentResponseOfDestinyInventoryComponent]] | The profile-level inventory of the Destiny Profile. COMPONENT TYPE: ProfileInventories
profileCurrencies | [[SingleComponentResponse&lt;DestinyInventoryComponent&gt;|SingleComponentResponseOfDestinyInventoryComponent]] | The profile-level currencies owned by the Destiny Profile. COMPONENT TYPE: ProfileCurrencies
profile | [[SingleComponentResponse&lt;DestinyProfileComponent&gt;|SingleComponentResponseOfDestinyProfileComponent]] | The basic information about the Destiny Profile (formerly &quot;Account&quot;). COMPONENT TYPE: Profiles
profileKiosks | [[SingleComponentResponse&lt;DestinyKiosksComponent&gt;|SingleComponentResponseOfDestinyKiosksComponent]] | Items available from Kiosks that are available Profile-wide (i.e. across all characters) This component returns information about what Kiosk items are available to you on a *Profile*level.  It is theoretically possible for Kiosks to have items gated by specific Character as well.If you ever have those, you will find them on the characterKiosks property. COMPONENT TYPE: Kiosks
characters | [[DictionaryComponentResponse&lt;int64,DestinyCharacterComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterComponent]] | Basic information about each character, keyed by the CharacterId. COMPONENT TYPE: Characters
characterInventories | [[DictionaryComponentResponse&lt;int64,DestinyInventoryComponent&gt;|DictionaryComponentResponseOfint64AndDestinyInventoryComponent]] | The character-level non-equipped inventory items, keyed by the Character's Id. COMPONENT TYPE: CharacterInventories
characterProgressions | [[DictionaryComponentResponse&lt;int64,DestinyCharacterProgressionComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterProgressionComponent]] | Character-level progression data, keyed by the Character's Id. COMPONENT TYPE: CharacterProgressions
characterRenderData | [[DictionaryComponentResponse&lt;int64,DestinyCharacterRenderComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterRenderComponent]] | Character rendering data - a minimal set of info needed to render a character in 3D - keyed by the Character's Id. COMPONENT TYPE: CharacterRenderData
characterActivities | [[DictionaryComponentResponse&lt;int64,DestinyCharacterActivitiesComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterActivitiesComponent]] | Character activity data - the activities available to this character and its status, keyed by the Character's Id. COMPONENT TYPE: CharacterActivities
characterEquipment | [[DictionaryComponentResponse&lt;int64,DestinyInventoryComponent&gt;|DictionaryComponentResponseOfint64AndDestinyInventoryComponent]] | The character's equipped items, keyed by the Character's Id. COMPONENT TYPE: CharacterEquipment
characterKiosks | [[DictionaryComponentResponse&lt;int64,DestinyKiosksComponent&gt;|DictionaryComponentResponseOfint64AndDestinyKiosksComponent]] | Items available from Kiosks that are available to a specific character as opposed to the account as a whole.It must be combined with data from the profileKiosks property to get a full picture of the character's availableitems to check out of a kiosk. This component returns information about what Kiosk items are available to you on a *Character*level.  Usually, kiosk items will be earned for the entire Profile (all characters) at once.To find those, look in the profileKiosks property. COMPONENT TYPE: Kiosks
itemComponents | [[DestinyItemComponentSet&lt;int64&gt;|DestinyItemComponentSetOfint64]] | Information about instanced items across all returned characters, keyed by the item's instance ID. COMPONENT TYPE: [See inside the DestinyItemComponentSet contract for component types.]

## Example
```javascript
{
    // Type: [[SingleComponentResponse&lt;DestinyVendorReceiptsComponent&gt;|SingleComponentResponseOfDestinyVendorReceiptsComponent]]
    "vendorReceipts": {
        // Type: [[DestinyVendorReceiptsComponent|Destiny-Entities-Profiles-DestinyVendorReceiptsComponent]]
        "data": {
            // Type: [[DestinyVendorReceipt|Destiny-Vendors-DestinyVendorReceipt]][]
            "receipts": [
               // Type: [[DestinyVendorReceipt|Destiny-Vendors-DestinyVendorReceipt]]
                {
                    // Type: [[DestinyItemQuantity|Destiny-DestinyItemQuantity]][]
                    "currencyPaid": [
                       // Type: [[DestinyItemQuantity|Destiny-DestinyItemQuantity]]
                        {
                            // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                            "itemHash": 0,
                            // Type: integer:int64:nullable
                            "itemInstanceId": 0,
                            // Type: integer:int32
                            "quantity": 0
                        }
                    ],
                    // Type: [[DestinyItemQuantity|Destiny-DestinyItemQuantity]]
                    "itemReceived": {
                        // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                        "itemHash": 0,
                        // Type: integer:int64:nullable
                        "itemInstanceId": 0,
                        // Type: integer:int32
                        "quantity": 0
                    },
                    // Type: integer:uint32
                    "licenseUnlockHash": 0,
                    // Type: integer:int64
                    "purchasedByCharacterId": 0,
                    // Type: [[DestinyVendorItemRefundPolicy|Destiny-DestinyVendorItemRefundPolicy]]:Enum
                    "refundPolicy": 0,
                    // Type: integer:int32
                    "sequenceNumber": 0,
                    // Type: integer:int64
                    "timeToExpiration": 0,
                    // Type: string:date-time
                    "expiresOn": ""
                }
            ]
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[SingleComponentResponse&lt;DestinyInventoryComponent&gt;|SingleComponentResponseOfDestinyInventoryComponent]]
    "profileInventory": {
        // Type: [[DestinyInventoryComponent|Destiny-Entities-Inventory-DestinyInventoryComponent]]
        "data": {
            // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]][]
            "items": [
               // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]]
                {
                    // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                    "itemHash": 0,
                    // Type: integer:int64:nullable
                    "itemInstanceId": 0,
                    // Type: integer:int32
                    "quantity": 0,
                    // Type: [[ItemBindStatus|Destiny-ItemBindStatus]]:Enum
                    "bindStatus": 0,
                    // Type: [[ItemLocation|Destiny-ItemLocation]]:Enum
                    "location": 0,
                    // Type: [[DestinyInventoryBucketDefinition|Destiny-Definitions-DestinyInventoryBucketDefinition]]:ManifestDefinition:integer:uint32
                    "bucketHash": 0,
                    // Type: [[TransferStatuses|Destiny-TransferStatuses]]:Enum
                    "transferStatus": 0,
                    // Type: boolean
                    "lockable": false,
                    // Type: [[ItemState|Destiny-ItemState]]:Enum
                    "state": 0
                }
            ]
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[SingleComponentResponse&lt;DestinyInventoryComponent&gt;|SingleComponentResponseOfDestinyInventoryComponent]]
    "profileCurrencies": {
        // Type: [[DestinyInventoryComponent|Destiny-Entities-Inventory-DestinyInventoryComponent]]
        "data": {
            // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]][]
            "items": [
               // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]]
                {
                    // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                    "itemHash": 0,
                    // Type: integer:int64:nullable
                    "itemInstanceId": 0,
                    // Type: integer:int32
                    "quantity": 0,
                    // Type: [[ItemBindStatus|Destiny-ItemBindStatus]]:Enum
                    "bindStatus": 0,
                    // Type: [[ItemLocation|Destiny-ItemLocation]]:Enum
                    "location": 0,
                    // Type: [[DestinyInventoryBucketDefinition|Destiny-Definitions-DestinyInventoryBucketDefinition]]:ManifestDefinition:integer:uint32
                    "bucketHash": 0,
                    // Type: [[TransferStatuses|Destiny-TransferStatuses]]:Enum
                    "transferStatus": 0,
                    // Type: boolean
                    "lockable": false,
                    // Type: [[ItemState|Destiny-ItemState]]:Enum
                    "state": 0
                }
            ]
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[SingleComponentResponse&lt;DestinyProfileComponent&gt;|SingleComponentResponseOfDestinyProfileComponent]]
    "profile": {
        // Type: [[DestinyProfileComponent|Destiny-Entities-Profiles-DestinyProfileComponent]]
        "data": {
            // Type: [[UserInfoCard|User-UserInfoCard]]
            "userInfo": {
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
            "dateLastPlayed": "",
            // Type: [[DestinyGameVersions|Destiny-DestinyGameVersions]]:Enum
            "versionsOwned": 0,
            // Type: integer:int64[]
            "characterIds": [
               // Type: integer:int64
                0
            ]
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[SingleComponentResponse&lt;DestinyKiosksComponent&gt;|SingleComponentResponseOfDestinyKiosksComponent]]
    "profileKiosks": {
        // Type: [[DestinyKiosksComponent|Destiny-Components-Kiosks-DestinyKiosksComponent]]
        "data": {
            // Type: Dictionary&lt;[[DestinyVendorDefinition|Destiny-Definitions-DestinyVendorDefinition]]:ManifestDefinition:integer:uint32,[[DestinyKioskItem|Destiny-Components-Kiosks-DestinyKioskItem]][]&gt;
            "kioskItems": {
                "0": [
                   // Type: [[DestinyKioskItem|Destiny-Components-Kiosks-DestinyKioskItem]]
                    {
                        // Type: integer:int32
                        "index": 0,
                        // Type: boolean
                        "canAcquire": false,
                        // Type: integer:int32[]
                        "failureIndexes": [
                           // Type: integer:int32
                            0
                        ]
                    }
                ]
            }
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[DictionaryComponentResponse&lt;int64,DestinyCharacterComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterComponent]]
    "characters": {
        // Type: Dictionary&lt;integer:int64,[[DestinyCharacterComponent|Destiny-Entities-Characters-DestinyCharacterComponent]]&gt;
        "data": {
            "0": {
                // Type: integer:int64
                "membershipId": 0,
                // Type: [[BungieMembershipType|BungieMembershipType]]:Enum
                "membershipType": 0,
                // Type: integer:int64
                "characterId": 0,
                // Type: string:date-time
                "dateLastPlayed": "",
                // Type: integer:int64
                "minutesPlayedThisSession": 0,
                // Type: integer:int64
                "minutesPlayedTotal": 0,
                // Type: integer:int32
                "light": 0,
                // Type: Dictionary&lt;integer:uint32,integer:int32&gt;
                "stats": {
                    "0": 0
                },
                // Type: [[DestinyRaceDefinition|Destiny-Definitions-DestinyRaceDefinition]]:ManifestDefinition:integer:uint32
                "raceHash": 0,
                // Type: [[DestinyGenderDefinition|Destiny-Definitions-DestinyGenderDefinition]]:ManifestDefinition:integer:uint32
                "genderHash": 0,
                // Type: [[DestinyClassDefinition|Destiny-Definitions-DestinyClassDefinition]]:ManifestDefinition:integer:uint32
                "classHash": 0,
                // Type: [[DestinyRace|Destiny-DestinyRace]]:Enum
                "raceType": 0,
                // Type: [[DestinyClass|Destiny-DestinyClass]]:Enum
                "classType": 0,
                // Type: [[DestinyGender|Destiny-DestinyGender]]:Enum
                "genderType": 0,
                // Type: string
                "emblemPath": "",
                // Type: string
                "emblemBackgroundPath": "",
                // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                "emblemHash": 0,
                // Type: [[DestinyProgression|Destiny-DestinyProgression]]
                "levelProgression": {
                    // Type: [[DestinyProgressionDefinition|Destiny-Definitions-DestinyProgressionDefinition]]:ManifestDefinition:integer:uint32
                    "progressionHash": 0,
                    // Type: integer:int32
                    "dailyProgress": 0,
                    // Type: integer:int32
                    "dailyLimit": 0,
                    // Type: integer:int32
                    "weeklyProgress": 0,
                    // Type: integer:int32
                    "weeklyLimit": 0,
                    // Type: integer:int32
                    "currentProgress": 0,
                    // Type: integer:int32
                    "level": 0,
                    // Type: integer:int32
                    "levelCap": 0,
                    // Type: integer:int32
                    "stepIndex": 0,
                    // Type: integer:int32
                    "progressToNextLevel": 0,
                    // Type: integer:int32
                    "nextLevelAt": 0
                },
                // Type: integer:int32
                "baseCharacterLevel": 0,
                // Type: number:float
                "percentToNextLevel": 0
            }
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[DictionaryComponentResponse&lt;int64,DestinyInventoryComponent&gt;|DictionaryComponentResponseOfint64AndDestinyInventoryComponent]]
    "characterInventories": {
        // Type: Dictionary&lt;integer:int64,[[DestinyInventoryComponent|Destiny-Entities-Inventory-DestinyInventoryComponent]]&gt;
        "data": {
            "0": {
                // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]][]
                "items": [
                   // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]]
                    {
                        // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                        "itemHash": 0,
                        // Type: integer:int64:nullable
                        "itemInstanceId": 0,
                        // Type: integer:int32
                        "quantity": 0,
                        // Type: [[ItemBindStatus|Destiny-ItemBindStatus]]:Enum
                        "bindStatus": 0,
                        // Type: [[ItemLocation|Destiny-ItemLocation]]:Enum
                        "location": 0,
                        // Type: [[DestinyInventoryBucketDefinition|Destiny-Definitions-DestinyInventoryBucketDefinition]]:ManifestDefinition:integer:uint32
                        "bucketHash": 0,
                        // Type: [[TransferStatuses|Destiny-TransferStatuses]]:Enum
                        "transferStatus": 0,
                        // Type: boolean
                        "lockable": false,
                        // Type: [[ItemState|Destiny-ItemState]]:Enum
                        "state": 0
                    }
                ]
            }
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[DictionaryComponentResponse&lt;int64,DestinyCharacterProgressionComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterProgressionComponent]]
    "characterProgressions": {
        // Type: Dictionary&lt;integer:int64,[[DestinyCharacterProgressionComponent|Destiny-Entities-Characters-DestinyCharacterProgressionComponent]]&gt;
        "data": {
            "0": {
                // Type: Dictionary&lt;[[DestinyProgressionDefinition|Destiny-Definitions-DestinyProgressionDefinition]]:ManifestDefinition:integer:uint32,[[DestinyProgression|Destiny-DestinyProgression]]&gt;
                "progressions": {
                    "0": {
                        // Type: [[DestinyProgressionDefinition|Destiny-Definitions-DestinyProgressionDefinition]]:ManifestDefinition:integer:uint32
                        "progressionHash": 0,
                        // Type: integer:int32
                        "dailyProgress": 0,
                        // Type: integer:int32
                        "dailyLimit": 0,
                        // Type: integer:int32
                        "weeklyProgress": 0,
                        // Type: integer:int32
                        "weeklyLimit": 0,
                        // Type: integer:int32
                        "currentProgress": 0,
                        // Type: integer:int32
                        "level": 0,
                        // Type: integer:int32
                        "levelCap": 0,
                        // Type: integer:int32
                        "stepIndex": 0,
                        // Type: integer:int32
                        "progressToNextLevel": 0,
                        // Type: integer:int32
                        "nextLevelAt": 0
                    }
                },
                // Type: Dictionary&lt;[[DestinyFactionDefinition|Destiny-Definitions-DestinyFactionDefinition]]:ManifestDefinition:integer:uint32,[[DestinyFactionProgression|Destiny-Progression-DestinyFactionProgression]]&gt;
                "factions": {
                    "0": {
                        // Type: [[DestinyFactionDefinition|Destiny-Definitions-DestinyFactionDefinition]]:ManifestDefinition:integer:uint32
                        "factionHash": 0,
                        // Type: [[DestinyProgressionDefinition|Destiny-Definitions-DestinyProgressionDefinition]]:ManifestDefinition:integer:uint32
                        "progressionHash": 0,
                        // Type: integer:int32
                        "dailyProgress": 0,
                        // Type: integer:int32
                        "dailyLimit": 0,
                        // Type: integer:int32
                        "weeklyProgress": 0,
                        // Type: integer:int32
                        "weeklyLimit": 0,
                        // Type: integer:int32
                        "currentProgress": 0,
                        // Type: integer:int32
                        "level": 0,
                        // Type: integer:int32
                        "levelCap": 0,
                        // Type: integer:int32
                        "stepIndex": 0,
                        // Type: integer:int32
                        "progressToNextLevel": 0,
                        // Type: integer:int32
                        "nextLevelAt": 0
                    }
                },
                // Type: Dictionary&lt;[[DestinyMilestoneDefinition|Destiny-Definitions-Milestones-DestinyMilestoneDefinition]]:ManifestDefinition:integer:uint32,[[DestinyMilestone|Destiny-Milestones-DestinyMilestone]]&gt;
                "milestones": {
                    "0": {
                        // Type: [[DestinyMilestoneDefinition|Destiny-Definitions-Milestones-DestinyMilestoneDefinition]]:ManifestDefinition:integer:uint32
                        "milestoneHash": 0,
                        // Type: [[DestinyMilestoneQuest|Destiny-Milestones-DestinyMilestoneQuest]][]
                        "availableQuests": [
                           // Type: [[DestinyMilestoneQuest|Destiny-Milestones-DestinyMilestoneQuest]]
                            {
                                // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                                "questItemHash": 0,
                                // Type: [[DestinyQuestStatus|Destiny-Quests-DestinyQuestStatus]]
                                "status": {
                                    // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                                    "questHash": 0,
                                    // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                                    "stepHash": 0,
                                    // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]][]
                                    "stepObjectives": [
                                       // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]]
                                        {
                                            // Type: [[DestinyObjectiveDefinition|Destiny-Definitions-DestinyObjectiveDefinition]]:ManifestDefinition:integer:uint32
                                            "objectiveHash": 0,
                                            // Type: [[DestinyDestinationDefinition|Destiny-Definitions-DestinyDestinationDefinition]]:ManifestDefinition:integer:uint32:nullable
                                            "destinationHash": 0,
                                            // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32:nullable
                                            "activityHash": 0,
                                            // Type: integer:int32:nullable
                                            "progress": 0,
                                            // Type: boolean
                                            "complete": false
                                        }
                                    ],
                                    // Type: boolean
                                    "tracked": false,
                                    // Type: integer:int64
                                    "itemInstanceId": 0,
                                    // Type: boolean
                                    "completed": false,
                                    // Type: boolean
                                    "redeemed": false,
                                    // Type: boolean
                                    "started": false,
                                    // Type: integer:uint32:nullable
                                    "vendorHash": 0
                                },
                                // Type: [[DestinyMilestoneActivity|Destiny-Milestones-DestinyMilestoneActivity]]
                                "activity": {
                                    // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32
                                    "activityHash": 0,
                                    // Type: [[DestinyActivityModifierDefinition|Destiny-Definitions-ActivityModifiers-DestinyActivityModifierDefinition]]:ManifestDefinition:integer:uint32[]
                                    "modifierHashes": [
                                       // Type: integer:uint32
                                        0
                                    ],
                                    // Type: [[DestinyMilestoneActivityVariant|Destiny-Milestones-DestinyMilestoneActivityVariant]][]
                                    "variants": [
                                       // Type: [[DestinyMilestoneActivityVariant|Destiny-Milestones-DestinyMilestoneActivityVariant]]
                                        {
                                            // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32
                                            "activityHash": 0,
                                            // Type: [[DestinyMilestoneActivityCompletionStatus|Destiny-Milestones-DestinyMilestoneActivityCompletionStatus]]
                                            "completionStatus": {
                                                // Type: boolean
                                                "completed": false,
                                                // Type: [[DestinyMilestoneActivityPhase|Destiny-Milestones-DestinyMilestoneActivityPhase]][]
                                                "phases": [
                                                   // Type: [[DestinyMilestoneActivityPhase|Destiny-Milestones-DestinyMilestoneActivityPhase]]
                                                    {
                                                        // Type: boolean
                                                        "complete": false
                                                    }
                                                ]
                                            }
                                        }
                                    ]
                                },
                                // Type: [[DestinyChallengeStatus|Destiny-Challenges-DestinyChallengeStatus]][]
                                "challenges": [
                                   // Type: [[DestinyChallengeStatus|Destiny-Challenges-DestinyChallengeStatus]]
                                    {
                                        // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]]
                                        "objective": {
                                            // Type: [[DestinyObjectiveDefinition|Destiny-Definitions-DestinyObjectiveDefinition]]:ManifestDefinition:integer:uint32
                                            "objectiveHash": 0,
                                            // Type: [[DestinyDestinationDefinition|Destiny-Definitions-DestinyDestinationDefinition]]:ManifestDefinition:integer:uint32:nullable
                                            "destinationHash": 0,
                                            // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32:nullable
                                            "activityHash": 0,
                                            // Type: integer:int32:nullable
                                            "progress": 0,
                                            // Type: boolean
                                            "complete": false
                                        }
                                    }
                                ]
                            }
                        ],
                        // Type: Dictionary&lt;string,number:float&gt;
                        "values": {
                            "{string}": 0
                        },
                        // Type: [[DestinyVendorDefinition|Destiny-Definitions-DestinyVendorDefinition]]:ManifestDefinition:integer:uint32[]
                        "vendorHashes": [
                           // Type: integer:uint32
                            0
                        ],
                        // Type: [[DestinyMilestoneRewardCategory|Destiny-Milestones-DestinyMilestoneRewardCategory]][]
                        "rewards": [
                           // Type: [[DestinyMilestoneRewardCategory|Destiny-Milestones-DestinyMilestoneRewardCategory]]
                            {
                                // Type: integer:uint32
                                "rewardCategoryHash": 0,
                                // Type: [[DestinyMilestoneRewardEntry|Destiny-Milestones-DestinyMilestoneRewardEntry]][]
                                "entries": [
                                   // Type: [[DestinyMilestoneRewardEntry|Destiny-Milestones-DestinyMilestoneRewardEntry]]
                                    {
                                        // Type: integer:uint32
                                        "rewardEntryHash": 0,
                                        // Type: boolean
                                        "earned": false,
                                        // Type: boolean
                                        "redeemed": false
                                    }
                                ]
                            }
                        ],
                        // Type: string:date-time:nullable
                        "startDate": "",
                        // Type: string:date-time:nullable
                        "endDate": ""
                    }
                },
                // Type: [[DestinyQuestStatus|Destiny-Quests-DestinyQuestStatus]][]
                "quests": [
                   // Type: [[DestinyQuestStatus|Destiny-Quests-DestinyQuestStatus]]
                    {
                        // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                        "questHash": 0,
                        // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                        "stepHash": 0,
                        // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]][]
                        "stepObjectives": [
                           // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]]
                            {
                                // Type: [[DestinyObjectiveDefinition|Destiny-Definitions-DestinyObjectiveDefinition]]:ManifestDefinition:integer:uint32
                                "objectiveHash": 0,
                                // Type: [[DestinyDestinationDefinition|Destiny-Definitions-DestinyDestinationDefinition]]:ManifestDefinition:integer:uint32:nullable
                                "destinationHash": 0,
                                // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32:nullable
                                "activityHash": 0,
                                // Type: integer:int32:nullable
                                "progress": 0,
                                // Type: boolean
                                "complete": false
                            }
                        ],
                        // Type: boolean
                        "tracked": false,
                        // Type: integer:int64
                        "itemInstanceId": 0,
                        // Type: boolean
                        "completed": false,
                        // Type: boolean
                        "redeemed": false,
                        // Type: boolean
                        "started": false,
                        // Type: integer:uint32:nullable
                        "vendorHash": 0
                    }
                ],
                // Type: Dictionary&lt;[[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32,[[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]][]&gt;
                "uninstancedItemObjectives": {
                    "0": [
                       // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]]
                        {
                            // Type: [[DestinyObjectiveDefinition|Destiny-Definitions-DestinyObjectiveDefinition]]:ManifestDefinition:integer:uint32
                            "objectiveHash": 0,
                            // Type: [[DestinyDestinationDefinition|Destiny-Definitions-DestinyDestinationDefinition]]:ManifestDefinition:integer:uint32:nullable
                            "destinationHash": 0,
                            // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32:nullable
                            "activityHash": 0,
                            // Type: integer:int32:nullable
                            "progress": 0,
                            // Type: boolean
                            "complete": false
                        }
                    ]
                }
            }
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[DictionaryComponentResponse&lt;int64,DestinyCharacterRenderComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterRenderComponent]]
    "characterRenderData": {
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
    },
    // Type: [[DictionaryComponentResponse&lt;int64,DestinyCharacterActivitiesComponent&gt;|DictionaryComponentResponseOfint64AndDestinyCharacterActivitiesComponent]]
    "characterActivities": {
        // Type: Dictionary&lt;integer:int64,[[DestinyCharacterActivitiesComponent|Destiny-Entities-Characters-DestinyCharacterActivitiesComponent]]&gt;
        "data": {
            "0": {
                // Type: string:date-time
                "dateActivityStarted": "",
                // Type: [[DestinyActivity|Destiny-DestinyActivity]][]
                "availableActivities": [
                   // Type: [[DestinyActivity|Destiny-DestinyActivity]]
                    {
                        // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32
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
                        "difficultyTier": 0
                    }
                ],
                // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32
                "currentActivityHash": 0,
                // Type: [[DestinyActivityModeDefinition|Destiny-Definitions-DestinyActivityModeDefinition]]:ManifestDefinition:integer:uint32
                "currentActivityModeHash": 0,
                // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32
                "lastCompletedStoryHash": 0
            }
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[DictionaryComponentResponse&lt;int64,DestinyInventoryComponent&gt;|DictionaryComponentResponseOfint64AndDestinyInventoryComponent]]
    "characterEquipment": {
        // Type: Dictionary&lt;integer:int64,[[DestinyInventoryComponent|Destiny-Entities-Inventory-DestinyInventoryComponent]]&gt;
        "data": {
            "0": {
                // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]][]
                "items": [
                   // Type: [[DestinyItemComponent|Destiny-Entities-Items-DestinyItemComponent]]
                    {
                        // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                        "itemHash": 0,
                        // Type: integer:int64:nullable
                        "itemInstanceId": 0,
                        // Type: integer:int32
                        "quantity": 0,
                        // Type: [[ItemBindStatus|Destiny-ItemBindStatus]]:Enum
                        "bindStatus": 0,
                        // Type: [[ItemLocation|Destiny-ItemLocation]]:Enum
                        "location": 0,
                        // Type: [[DestinyInventoryBucketDefinition|Destiny-Definitions-DestinyInventoryBucketDefinition]]:ManifestDefinition:integer:uint32
                        "bucketHash": 0,
                        // Type: [[TransferStatuses|Destiny-TransferStatuses]]:Enum
                        "transferStatus": 0,
                        // Type: boolean
                        "lockable": false,
                        // Type: [[ItemState|Destiny-ItemState]]:Enum
                        "state": 0
                    }
                ]
            }
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[DictionaryComponentResponse&lt;int64,DestinyKiosksComponent&gt;|DictionaryComponentResponseOfint64AndDestinyKiosksComponent]]
    "characterKiosks": {
        // Type: Dictionary&lt;integer:int64,[[DestinyKiosksComponent|Destiny-Components-Kiosks-DestinyKiosksComponent]]&gt;
        "data": {
            "0": {
                // Type: Dictionary&lt;[[DestinyVendorDefinition|Destiny-Definitions-DestinyVendorDefinition]]:ManifestDefinition:integer:uint32,[[DestinyKioskItem|Destiny-Components-Kiosks-DestinyKioskItem]][]&gt;
                "kioskItems": {
                    "0": [
                       // Type: [[DestinyKioskItem|Destiny-Components-Kiosks-DestinyKioskItem]]
                        {
                            // Type: integer:int32
                            "index": 0,
                            // Type: boolean
                            "canAcquire": false,
                            // Type: integer:int32[]
                            "failureIndexes": [
                               // Type: integer:int32
                                0
                            ]
                        }
                    ]
                }
            }
        },
        // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
        "privacy": 0
    },
    // Type: [[DestinyItemComponentSet&lt;int64&gt;|DestinyItemComponentSetOfint64]]
    "itemComponents": {
        // Type: [[DictionaryComponentResponse&lt;int64,DestinyItemInstanceComponent&gt;|DictionaryComponentResponseOfint64AndDestinyItemInstanceComponent]]
        "instances": {
            // Type: Dictionary&lt;integer:int64,[[DestinyItemInstanceComponent|Destiny-Entities-Items-DestinyItemInstanceComponent]]&gt;
            "data": {
                "0": {
                    // Type: [[DamageType|Destiny-DamageType]]:Enum
                    "damageType": 0,
                    // Type: [[DestinyDamageTypeDefinition|Destiny-Definitions-DestinyDamageTypeDefinition]]:ManifestDefinition:integer:uint32:nullable
                    "damageTypeHash": 0,
                    // Type: [[DestinyStat|Destiny-DestinyStat]]
                    "primaryStat": {
                        // Type: [[DestinyStatDefinition|Destiny-Definitions-DestinyStatDefinition]]:ManifestDefinition:integer:uint32
                        "statHash": 0,
                        // Type: integer:int32
                        "value": 0,
                        // Type: integer:int32
                        "maximumValue": 0
                    },
                    // Type: integer:int32
                    "itemLevel": 0,
                    // Type: integer:int32
                    "quality": 0,
                    // Type: boolean
                    "isEquipped": false,
                    // Type: boolean
                    "canEquip": false,
                    // Type: integer:int32
                    "equipRequiredLevel": 0,
                    // Type: [[DestinyUnlockDefinition|Destiny-Definitions-DestinyUnlockDefinition]]:ManifestDefinition:integer:uint32[]
                    "unlockHashesRequiredToEquip": [
                       // Type: integer:uint32
                        0
                    ],
                    // Type: [[EquipFailureReason|Destiny-EquipFailureReason]]:Enum
                    "cannotEquipReason": 0
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        },
        // Type: [[DictionaryComponentResponse&lt;int64,DestinyItemObjectivesComponent&gt;|DictionaryComponentResponseOfint64AndDestinyItemObjectivesComponent]]
        "objectives": {
            // Type: Dictionary&lt;integer:int64,[[DestinyItemObjectivesComponent|Destiny-Entities-Items-DestinyItemObjectivesComponent]]&gt;
            "data": {
                "0": {
                    // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]][]
                    "objectives": [
                       // Type: [[DestinyObjectiveProgress|Destiny-Quests-DestinyObjectiveProgress]]
                        {
                            // Type: [[DestinyObjectiveDefinition|Destiny-Definitions-DestinyObjectiveDefinition]]:ManifestDefinition:integer:uint32
                            "objectiveHash": 0,
                            // Type: [[DestinyDestinationDefinition|Destiny-Definitions-DestinyDestinationDefinition]]:ManifestDefinition:integer:uint32:nullable
                            "destinationHash": 0,
                            // Type: [[DestinyActivityDefinition|Destiny-Definitions-DestinyActivityDefinition]]:ManifestDefinition:integer:uint32:nullable
                            "activityHash": 0,
                            // Type: integer:int32:nullable
                            "progress": 0,
                            // Type: boolean
                            "complete": false
                        }
                    ]
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        },
        // Type: [[DictionaryComponentResponse&lt;int64,DestinyItemPerksComponent&gt;|DictionaryComponentResponseOfint64AndDestinyItemPerksComponent]]
        "perks": {
            // Type: Dictionary&lt;integer:int64,[[DestinyItemPerksComponent|Destiny-Entities-Items-DestinyItemPerksComponent]]&gt;
            "data": {
                "0": {
                    // Type: [[DestinyPerkReference|Destiny-Perks-DestinyPerkReference]][]
                    "perks": [
                       // Type: [[DestinyPerkReference|Destiny-Perks-DestinyPerkReference]]
                        {
                            // Type: [[DestinySandboxPerkDefinition|Destiny-Definitions-DestinySandboxPerkDefinition]]:ManifestDefinition:integer:uint32
                            "perkHash": 0,
                            // Type: string
                            "iconPath": "",
                            // Type: boolean
                            "isActive": false,
                            // Type: boolean
                            "visible": false
                        }
                    ]
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        },
        // Type: [[DictionaryComponentResponse&lt;int64,DestinyItemRenderComponent&gt;|DictionaryComponentResponseOfint64AndDestinyItemRenderComponent]]
        "renderData": {
            // Type: Dictionary&lt;integer:int64,[[DestinyItemRenderComponent|Destiny-Entities-Items-DestinyItemRenderComponent]]&gt;
            "data": {
                "0": {
                    // Type: boolean
                    "useCustomDyes": false,
                    // Type: Dictionary&lt;integer:int32,integer:int32&gt;
                    "artRegions": {
                        "0": 0
                    }
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        },
        // Type: [[DictionaryComponentResponse&lt;int64,DestinyItemStatsComponent&gt;|DictionaryComponentResponseOfint64AndDestinyItemStatsComponent]]
        "stats": {
            // Type: Dictionary&lt;integer:int64,[[DestinyItemStatsComponent|Destiny-Entities-Items-DestinyItemStatsComponent]]&gt;
            "data": {
                "0": {
                    // Type: Dictionary&lt;[[DestinyStatDefinition|Destiny-Definitions-DestinyStatDefinition]]:ManifestDefinition:integer:uint32,[[DestinyStat|Destiny-DestinyStat]]&gt;
                    "stats": {
                        "0": {
                            // Type: [[DestinyStatDefinition|Destiny-Definitions-DestinyStatDefinition]]:ManifestDefinition:integer:uint32
                            "statHash": 0,
                            // Type: integer:int32
                            "value": 0,
                            // Type: integer:int32
                            "maximumValue": 0
                        }
                    }
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        },
        // Type: [[DictionaryComponentResponse&lt;int64,DestinyItemSocketsComponent&gt;|DictionaryComponentResponseOfint64AndDestinyItemSocketsComponent]]
        "sockets": {
            // Type: Dictionary&lt;integer:int64,[[DestinyItemSocketsComponent|Destiny-Entities-Items-DestinyItemSocketsComponent]]&gt;
            "data": {
                "0": {
                    // Type: [[DestinyItemSocketState|Destiny-Entities-Items-DestinyItemSocketState]][]
                    "sockets": [
                       // Type: [[DestinyItemSocketState|Destiny-Entities-Items-DestinyItemSocketState]]
                        {
                            // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32:nullable
                            "plugHash": 0,
                            // Type: boolean
                            "isEnabled": false,
                            // Type: integer:int32[]
                            "enableFailIndexes": [
                               // Type: integer:int32
                                0
                            ],
                            // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32[]
                            "reusablePlugHashes": [
                               // Type: integer:uint32
                                0
                            ]
                        }
                    ]
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        },
        // Type: [[DictionaryComponentResponse&lt;int64,DestinyItemTalentGridComponent&gt;|DictionaryComponentResponseOfint64AndDestinyItemTalentGridComponent]]
        "talentGrids": {
            // Type: Dictionary&lt;integer:int64,[[DestinyItemTalentGridComponent|Destiny-Entities-Items-DestinyItemTalentGridComponent]]&gt;
            "data": {
                "0": {
                    // Type: [[DestinyTalentGridDefinition|Destiny-Definitions-DestinyTalentGridDefinition]]:ManifestDefinition:integer:uint32
                    "talentGridHash": 0,
                    // Type: [[DestinyTalentNode|Destiny-DestinyTalentNode]][]
                    "nodes": [
                       // Type: [[DestinyTalentNode|Destiny-DestinyTalentNode]]
                        {
                            // Type: integer:int32
                            "nodeIndex": 0,
                            // Type: integer:uint32
                            "nodeHash": 0,
                            // Type: [[DestinyTalentNodeState|Destiny-DestinyTalentNodeState]]:Enum
                            "state": 0,
                            // Type: boolean
                            "isActivated": false,
                            // Type: integer:int32
                            "stepIndex": 0,
                            // Type: [[DestinyMaterialRequirement|Destiny-Definitions-DestinyMaterialRequirement]]:Definition[]
                            "materialsToUpgrade": [
                               // Type: [[DestinyMaterialRequirement|Destiny-Definitions-DestinyMaterialRequirement]]:Definition
                                {
                                    // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
                                    "itemHash": 0,
                                    // Type: boolean
                                    "deleteOnAction": false,
                                    // Type: integer:int32
                                    "count": 0,
                                    // Type: boolean
                                    "omitFromRequirements": false
                                }
                            ],
                            // Type: integer:int32
                            "activationGridLevel": 0,
                            // Type: number:float
                            "progressPercent": 0,
                            // Type: boolean
                            "hidden": false,
                            // Type: [[DestinyTalentNodeStatBlock|Destiny-DestinyTalentNodeStatBlock]]
                            "nodeStatsBlock": {
                                // Type: [[DestinyStat|Destiny-DestinyStat]][]
                                "currentStepStats": [
                                   // Type: [[DestinyStat|Destiny-DestinyStat]]
                                    {
                                        // Type: [[DestinyStatDefinition|Destiny-Definitions-DestinyStatDefinition]]:ManifestDefinition:integer:uint32
                                        "statHash": 0,
                                        // Type: integer:int32
                                        "value": 0,
                                        // Type: integer:int32
                                        "maximumValue": 0
                                    }
                                ],
                                // Type: [[DestinyStat|Destiny-DestinyStat]][]
                                "nextStepStats": [
                                   // Type: [[DestinyStat|Destiny-DestinyStat]]
                                    {
                                        // Type: [[DestinyStatDefinition|Destiny-Definitions-DestinyStatDefinition]]:ManifestDefinition:integer:uint32
                                        "statHash": 0,
                                        // Type: integer:int32
                                        "value": 0,
                                        // Type: integer:int32
                                        "maximumValue": 0
                                    }
                                ]
                            }
                        }
                    ],
                    // Type: boolean
                    "isGridComplete": false,
                    // Type: [[DestinyProgression|Destiny-DestinyProgression]]
                    "gridProgression": {
                        // Type: [[DestinyProgressionDefinition|Destiny-Definitions-DestinyProgressionDefinition]]:ManifestDefinition:integer:uint32
                        "progressionHash": 0,
                        // Type: integer:int32
                        "dailyProgress": 0,
                        // Type: integer:int32
                        "dailyLimit": 0,
                        // Type: integer:int32
                        "weeklyProgress": 0,
                        // Type: integer:int32
                        "weeklyLimit": 0,
                        // Type: integer:int32
                        "currentProgress": 0,
                        // Type: integer:int32
                        "level": 0,
                        // Type: integer:int32
                        "levelCap": 0,
                        // Type: integer:int32
                        "stepIndex": 0,
                        // Type: integer:int32
                        "progressToNextLevel": 0,
                        // Type: integer:int32
                        "nextLevelAt": 0
                    }
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        },
        // Type: [[DictionaryComponentResponse&lt;uint32,DestinyItemPlugComponent&gt;|DictionaryComponentResponseOfuint32AndDestinyItemPlugComponent]]
        "plugStates": {
            // Type: Dictionary&lt;integer:uint32,[[DestinyItemPlugComponent|Destiny-Components-Items-DestinyItemPlugComponent]]&gt;
            "data": {
                "0": {
                    // Type: integer:int32[]
                    "insertFailIndexes": [
                       // Type: integer:int32
                        0
                    ],
                    // Type: integer:int32[]
                    "enableFailIndexes": [
                       // Type: integer:int32
                        0
                    ]
                }
            },
            // Type: [[ComponentPrivacySetting|Components-ComponentPrivacySetting]]:Enum
            "privacy": 0
        }
    }
}

```

## References
1. https://bungie-net.github.io/multi/schema_Destiny-Responses-DestinyProfileResponse.html#schema_Destiny-Responses-DestinyProfileResponse