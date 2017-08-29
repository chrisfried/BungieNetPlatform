<span class="wiki-builder">This page was generated with Wiki Builder. Do not change the format!</span>

## Info
Request this component if you want the details about an item being sold in relation to the charactermaking the request: whether the character can buy it,whether they can afford it, and other data related to purchasing the item. Note that if you want instance, stats, etc... data for the item, you'll have to request additional components such asItemInstances, ItemPerks etc... and acquire them from the DestinyVendorResponse's &quot;items&quot; property.

## Schema
* **Type:** Class
* **Component Type Dependency:** VendorSales

## Properties
Name | Type | Description
---- | ---- | -----------
vendorItemIndex | integer:int32 | The index into the DestinyVendorDefinition.itemList property.  Note that this means Vendor data*is* Content Version dependent: make sure you have the latest content before you use Vendor data,or these indexes may mismatch. Most systems avoid this problem, but Vendors is one area where weare unable to reasonably avoid content dependency at the moment.
itemHash | [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32 | The hash of the item being sold, as a quick shortcut for looking up the DestinyInventoryItemDefinitionof the sale item.
saleStatus | [[VendorItemStatus|Destiny-VendorItemStatus]]:Enum | A flag indicating whether the requesting character can buy the item, and if not the reasons why the character can't buy it.
costs | [[DestinyItemQuantity|Destiny-DestinyItemQuantity]][] | A summary of the current costs of the item.
requiredUnlocks | [[DestinyUnlockDefinition|Destiny-Definitions-DestinyUnlockDefinition]]:ManifestDefinition:integer:uint32[] | If you can't buy the item due to a complex character state, these will be hashes forDestinyUnlockDefinitions that you can check to see messages regarding the failure (if the unlockshave human readable information: it is not guaranteed that Unlocks will have human readable strings, andyour application will have to handle that) Prefer using failureIndexes instead.  These are provided for informational purposes, but have largelybeen supplanted by failureIndexes.
unlockStatuses | [[DestinyUnlockStatus|Destiny-DestinyUnlockStatus]][] | If any complex unlock states are checked in determining purchasability, these willbe returned here along with the status of the unlock check. Prefer using failureIndexes instead.  These are provided for informational purposes, but have largelybeen supplanted by failureIndexes.
failureIndexes | integer:int32[] | Indexes in to the &quot;failureStrings&quot; lookup table in DestinyVendorDefinition for the given Vendor.Gives some more reliable failure information for why you can't purchase an item. It is preferred to use these over requiredUnlocks and unlockStatuses: the latter are providedmostly in case someone can do something interesting with it that I didn't anticipate.

## Example
```javascript
{
    // Type: integer:int32
    "vendorItemIndex": 0,
    // Type: [[DestinyInventoryItemDefinition|Destiny-Definitions-DestinyInventoryItemDefinition]]:ManifestDefinition:integer:uint32
    "itemHash": 0,
    // Type: [[VendorItemStatus|Destiny-VendorItemStatus]]:Enum
    "saleStatus": 0,
    // Type: [[DestinyItemQuantity|Destiny-DestinyItemQuantity]][]
    "costs": [
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
    // Type: [[DestinyUnlockDefinition|Destiny-Definitions-DestinyUnlockDefinition]]:ManifestDefinition:integer:uint32[]
    "requiredUnlocks": [
       // Type: integer:uint32
        0
    ],
    // Type: [[DestinyUnlockStatus|Destiny-DestinyUnlockStatus]][]
    "unlockStatuses": [
       // Type: [[DestinyUnlockStatus|Destiny-DestinyUnlockStatus]]
        {
            // Type: [[DestinyUnlockDefinition|Destiny-Definitions-DestinyUnlockDefinition]]:ManifestDefinition:integer:uint32
            "unlockHash": 0,
            // Type: boolean
            "isSet": false
        }
    ],
    // Type: integer:int32[]
    "failureIndexes": [
       // Type: integer:int32
        0
    ]
}

```

## References
1. https://bungie-net.github.io/multi/schema_Destiny-Entities-Vendors-DestinyVendorSaleItemComponent.html#schema_Destiny-Entities-Vendors-DestinyVendorSaleItemComponent