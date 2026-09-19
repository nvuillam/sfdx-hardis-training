# Flows

| Object | Name | Type | Description | Status |
| :----  | :-------- | :--: | :---------- | :----- |
| Installation__c | [Installation_Assign_Crew](Installation_Assign_Crew.md) [🕒](Installation_Assign_Crew-history.md) | Record Before Save | When a planner puts a crew on a planned installation that already has a date, the installation moves to Scheduled on its own. A crew larger than the installation cap is brought back down to the cap: too many people on a small roof is a safety problem. | Active |
| Installation__c | [Installation_Close_Check](Installation_Close_Check.md) [🕒](Installation_Close_Check-history.md) | Record Before Save | An installation cannot be closed while its handover checklist has an item not done. | Active |
| Installation__c | [Installation_Crew_Warning](Installation_Crew_Warning.md) | Record After Save | Warns the planner when the crew assigned to an installation is too small for the panels it needs. | Active |

_Documentation generated from branch features/US-054-project-documentation with [sfdx-hardis](https://sfdx-hardis.cloudity.com) by [Cloudity](https://cloudity.com?ref=sfdxhardis) command [`sf hardis:doc:project2markdown`](https://sfdx-hardis.cloudity.com/hardis/doc/project2markdown/)_

[![SFDX-Hardis is provided by Cloudity](https://raw.githubusercontent.com/hardisgroupcom/sfdx-hardis/refs/heads/main/docs/assets/images/cloudity-banner.png)](https://cloudity.com?ref=sfdxhardis)
