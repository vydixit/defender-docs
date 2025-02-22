---
title: BehaviorInfo table in the advanced hunting schema
description: Learn about alert generation events in the BehaviorInfo table of the advanced hunting schema
search.appverid: met150
ms.service: defender-xdr
ms.subservice: adv-hunting
f1.keywords: 
  - NOCSH
ms.author: maccruz
author: schmurky
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: 
- m365-security
- tier3
ms.custom: 
- cx-ti
- cx-ah
ms.topic: reference
ms.date: 12/29/2023
---

# BehaviorInfo (Preview)

[!INCLUDE [Microsoft Defender XDR rebranding](../includes/microsoft-defender.md)]


**Applies to:**
- Microsoft Defender XDR




The `BehaviorInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about alerts from Microsoft Defender for Cloud Apps. Use this reference to construct queries that return information from this table.

> [!IMPORTANT]
> The `BehaviorInfo` table is in preview and is not available for GCC. The information here may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here. Have feedback to share? Fill out our [feedback form](https://forms.office.com/r/x0mX5hBkGu).

Behaviors are a type of data in Microsoft Defender XDR based on one or more raw events. Behaviors provide contextual insight into events and can, but not necessarily, indicate malicious activity. [Read more about behaviors](/defender-cloud-apps/behaviors)

For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).

| Column name | Data type | Description |
|-------------|-----------|-------------|
| `Timestamp` | `datetime` | Date and time when the record was generated |
| `BehaviorId` | `string` | Unique identifier for the behavior|
| `ActionType` | `string` | Type of behavior |
| `Description` | `string` | Description of the behavior |
| `Categories` | `string` | Type of threat indicator or  breach activity identified by the behavior|
| `AttackTechniques` | `string` | MITRE ATT&CK techniques associated with the activity that triggered the behavior |
| `ServiceSource` | `string` | Product or service that identified the behavior |
| `DetectionSource` | `string` | Detection technology or sensor that identified the notable component or activity |
| `DataSources` | `string` | Products or services that provided information for the behavior |
| `DeviceId` | `string` | Unique identifier for the device in the service |
| `AccountUpn` | `string` | User principal name (UPN) of the account |
| `AccountObjectId` | `string` | Unique identifier for the account in Microsoft Entra ID |
| `StartTime` | `datetime` | Date and time of the first activity related to the behavior|
| `EndTime` | `datetime` | Date and time of the last activity related to the behavior|
| `AdditionalFields` | `string` | Additional information about the behavior|



## Related topics
- [Advanced hunting overview](advanced-hunting-overview.md)
- [Learn the query language](advanced-hunting-query-language.md)
- [Use shared queries](advanced-hunting-shared-queries.md)
- [Hunt across devices, emails, apps, and identities](advanced-hunting-query-emails-devices.md)
- [Understand the schema](advanced-hunting-schema-tables.md)
- [Apply query best practices](advanced-hunting-best-practices.md)
[!INCLUDE [Microsoft Defender XDR rebranding](../includes/defender-m3d-techcommunity.md)]
