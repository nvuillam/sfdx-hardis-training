# Branches & Orgs

## Branches & Orgs strategy

```mermaid
flowchart LR

    subgraph GitBranches [Git Branches]
        direction TB
        featureBranch1["feature1"]:::gitFeature
        featureBranch2["feature2"]:::gitFeature
        integrationBranch["integration"]:::gitMajor
        uatBranch["uat"]:::gitMajor
        hotfixBranch3["hotfix3"]:::gitFeature
        hotfixBranch4["hotfix4"]:::gitFeature
        preprodBranch["preprod"]:::gitMajor
        mainBranch["main"]:::gitMain
    end

    subgraph SalesforceOrgs [Salesforce Major Orgs]
        direction TB
        mainOrg(["<b>Production Org</b>"]):::salesforceProd
        preprodOrg(["<b>Preprod Org</b>"]):::salesforceMajor
        uatOrg(["<b>Uat Org</b>"]):::salesforceMajor
        integrationOrg(["<b>Integration Org</b>"]):::salesforceMajor
    end

    subgraph SalesforceDevOrgsintegration [Salesforce Dev Orgs]
        direction TB
        feature1Org(["Dev Feature1"]):::salesforceDev
        feature2Org(["Dev Feature2"]):::salesforceDev
    end

    subgraph SalesforceDevOrgspreprod [Salesforce Dev Orgs]
        direction TB
        hotfix3Org(["Dev Hotfix3"]):::salesforceDev
        hotfix4Org(["Dev Hotfix4"]):::salesforceDev
    end

    featureBranch1 ==>|"Merge"| integrationBranch
    featureBranch2 ==>|"Merge"| integrationBranch
    hotfixBranch3 ==>|"Merge"| preprodBranch
    hotfixBranch4 ==>|"Merge"| preprodBranch
    integrationBranch ==>|"Merge"| uatBranch
    preprodBranch ==>|"Merge"| mainBranch
    uatBranch ==>|"Merge"| preprodBranch

    mainBranch -. Deploy to Org .-> mainOrg
    preprodBranch -. Deploy to Org .-> preprodOrg
    uatBranch -. Deploy to Org .-> uatOrg
    integrationBranch -. Deploy to Org .-> integrationOrg

    feature1Org <-. Push / Pull .-> featureBranch1
    feature2Org <-. Push / Pull .-> featureBranch2
    hotfix3Org <-. Push / Pull .-> hotfixBranch3
    hotfix4Org <-. Push / Pull .-> hotfixBranch4

    mainBranch ==>|"Retrofit from RUN to BUILD"| integrationBranch

    classDef salesforceDev fill:#9BC3FF,stroke:#2B65D9,stroke-width:2px,color:#000000,font-weight:bold,border-radius:10px;
    classDef salesforceMajor fill:#67B7D1,stroke:#004D66,stroke-width:2px,color:#FFFFFF,font-weight:bold,border-radius:10px;
    classDef salesforceProd fill:#4C98C3,stroke:#003B5A,stroke-width:2px,color:#FFFFFF,font-weight:bold,border-radius:10px;
    classDef gitMajor fill:#FFCA76,stroke:#E65C00,stroke-width:2px,color:#000000,font-weight:bold,border-radius:10px;
    classDef gitMain fill:#F97B8B,stroke:#CC2936,stroke-width:2px,color:#000000,font-weight:bold,border-radius:10px;
    classDef gitFeature fill:#B0DE87,stroke:#2D6A4F,stroke-width:2px,color:#000000,font-weight:bold,border-radius:10px;

    style GitBranches fill:#F4F5F9,color:#000000,stroke:#8B72B2,stroke-width:1px;
    style SalesforceOrgs fill:#F1F7F5,color:#000000,stroke:#468C70,stroke-width:1px;

style SalesforceDevOrgsintegration fill:#EBF6FF,color:#000000,stroke:#0077B5,stroke-width:1px;
style SalesforceDevOrgspreprod fill:#EBF6FF,color:#000000,stroke:#0077B5,stroke-width:1px;
linkStyle 0,1,2,3,4,5,6,15 stroke:#4B0082,stroke-width:4px,color:#4B0082,background-color:transparent;
linkStyle 7,8,9,10 stroke:#4169E1,stroke-width:2px,color:#4169E1,background-color:transparent;
linkStyle 11,12,13,14 stroke:#5F9EA0,stroke-width:2px,color:#5F9EA0,background-color:transparent;
```

| Git branch | Salesforce Org | Deployment Username |
| :--------- | :------------- | :------------------ |
| main | https://login.salesforce.com | veurtio+demo.73193ee31bf8@agentforce.com |
| preprod | https://login.salesforce.com | veurtio.dd9da51447c4@agentforce.com |
| uat | https://test.salesforce.com | test-y0vnmsc9mzwr@example.com |
| integration | https://test.salesforce.com | test-m276mvg5vkjy@example.com |

___

_Documentation generated from branch features/US-054-project-documentation with [sfdx-hardis](https://sfdx-hardis.cloudity.com) by [Cloudity](https://cloudity.com?ref=sfdxhardis) command [`sf hardis:doc:project2markdown`](https://sfdx-hardis.cloudity.com/hardis/doc/project2markdown/)_

[![SFDX-Hardis is provided by Cloudity](https://raw.githubusercontent.com/hardisgroupcom/sfdx-hardis/refs/heads/main/docs/assets/images/cloudity-banner.png)](https://cloudity.com?ref=sfdxhardis)
