---
# required metadata

title: Known issues with deployments using the infrastructure stack
description: This topic lists known issues that you might experience during deployment.
author: sarvanisathish
manager: AnnBe
ms.date: 12/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form:  [Operations AOT form name to tie this topic to]
audience: IT Pro
# ms.devlang: 
ms.reviewer: sericks
ms.search.scope: Operations
# ms.custom: [used by loc for topics migrated from the wiki]
ms.search.region: Global 
# ms.search.industry: 
ms.author: sarvanis
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1

---

# Known issues with deployments using the infrastructure stack

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

This topic explains how to view the known issues that you might experience during deployment on the modern infrastructure stack.

## Lifecycle Services (LCS)

### Features not yet implemented
The following LCS features are not yet implemented in the modern deployment experience. These features have not been deprecated.

| **Feature**             | **Description**  |
------------------------------|---------------------------------------------------------|
| Data movement scenarios | The self-service automation to move database bacpacs and copy databases across environments is not yet implemented. At this time, you will need to log a support ticket to perform these operations. The following self-service feature is planned for a future release: Golden config bacpac move to sandbox environment. |
| Monitoring page         | The LCS page that allows you to monitor the Finance and Operations environment is not yet implemented. |
| Package deployments     | Applying binary, application, and X++ updates is not yet enabled. Currently, you can only update your environment by deleting and redeploying. Slipstreaming is enabled.     |
| LCS tiles experience    | Not yet enabled.  |

### Features not intended to be implemented
The following LCS features are deprecated and will not be implemented in the modern deployment experience.

| **Feature**        | **Description**   |
|--------------------|--------|
| System diagnostics | System diagnostics has been deprecated. All data and functionality provided by system diagnostics today will be available through other features in the product and LCS. |
| Service requests   | Service requests are being replaced with self-service actions. |

### Known issues in this release
Know issues are bugs that will be addressed in upcoming releases. Every 2 weeks there is a new release of LCS.

-   Logs on failures are not yet available through LCS. Currently, you need to log failures as a support incident.

-   LCS integration from a Finance and Operations environment does not work. The features that are not available as a result of this include:

    -   Getting started

    -   Online Help enabled through BPM libraries. Online Help from docs.microsoft.com is available.

    -   Raising support tickets from within Finance and Operations. Cloud-powered support from LCS is enabled.

## Finance and Operations 

### Features not yet implemented

The following features that have infrastructure dependencies are not yet implemented in the modern deployment experience. These features have not been deprecated.

| **Feature**                 | **Description**                                           |
|-----------------------------|-----------------------------------------------------------|
| Retail                      | Retail support is not yet enabled.                        |
| Trace Parser                | Perf tools are not yet supported.                         |
| Reporting – Print to Screen | Only print to PDF is supported at this time.              |
| Export to Word              | Export to Word functionality is not enabled at this time. |

### Features not intended to be implemented
The following features are deprecated and will not be implemented in the modern deployment experience.

| **Feature**  | **Description**                     |
|--------------|-------------------------------------|
| Custom fonts | Custom fonts will not be supported. |

### Known issues in this release
Known issues are listed below. These are bugs that are being worked on actively. Hotfixes will be provided in future releases.

#### Financial reporting

-   **Default reports are not imported by default:** To import the default reports, do the following:

    1.  Launch Report designer by going to **General Ledger \> Inquiries and reports \> Financial reports.**
    2.  Click **New**.
    3.  Go to **Tools \> Import Default Reports**. 
    4.  Reports will load into the web client after a few minutes.

-   **Print to PDF is printing to XPS instead** (due to a print driver access issue).
