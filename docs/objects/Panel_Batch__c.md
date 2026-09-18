<!-- This file is auto-generated. if you do not want it to be overwritten, set TRUE in the line below -->
<!-- DO_NOT_OVERWRITE_DOC=FALSE -->

# Panel_Batch__c

## Schema

```mermaid
graph TD
Panel_Batch__c["Panel Batch"]:::mainObject
click Panel_Batch__c "../Panel_Batch__c/"
Installation__c["Installation"]:::customObject
click Installation__c "../Installation__c/"

Panel_Batch__c -->|Installation__c| Installation__c

classDef object fill:#D6E9FF,stroke:#0070D2,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObject fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObjectManaged fill:#FFD8B2,stroke:#CC5500,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainObject fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;
linkStyle 0 stroke:#A6A6A6,stroke-width:2px;

```


<!-- Object description -->

## Fields

| Name | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| Arrival_Date__c | Arrival Date | Date | The day the pallet reaches the warehouse. |
| Cost__c | Cost | Currency | What Helios paid for this pallet. Level 2 opens it to the crews. |
| External_Id__c | External Id | Text | Stable key used by the training data loader. Never edit it by hand. |
| Installation__c | Installation | Lookup | The installation this pallet is for. |
| Quantity__c | Quantity | Number | How many panels are on this pallet. |
| Quote_Pdf_Url__c | Quote PDF URL | Url | Where the generated quote PDF for this batch is stored. |
| Serial_Prefix__c | Serial Prefix | Text | First characters of the serial numbers on this pallet. |
















## Related Apex Classes

| Apex Class | Type |
| :----      | :--: | 
| [InstallationScheduler](../apex/InstallationScheduler.md) | Class |
| [InstallationSchedulerTest](../apex/InstallationSchedulerTest.md) | Test |


## Related Lightning Web Components

| Component | Description | Exposed | Targets |
| :-------- | :---------- | :-----: | :------------- |
| [installationTimeline](../lwc/installationTimeline.md) | Shows the panel batches booked for an installation, in arrival order. | ✅ | lightning__RecordPage |










## Related Permission Sets

| Permission Set | User License |
| :----      | :--: | 
| [Helios_Delivery_Crew](../permissionsets/Helios_Delivery_Crew.md) | None |
| [Helios_Delivery_Manager](../permissionsets/Helios_Delivery_Manager.md) | None |


[![SFDX-Hardis is provided by Cloudity](https://raw.githubusercontent.com/hardisgroupcom/sfdx-hardis/refs/heads/main/docs/assets/images/cloudity-banner.png)](https://cloudity.com?ref=sfdxhardis)

_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com), by [Cloudity](https://www.cloudity.com/) & [friends](https://github.com/hardisgroupcom/sfdx-hardis/graphs/contributors)_
