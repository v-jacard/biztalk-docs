---
title: "BTAD_SilentMode | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""
ms.service: "biztalk-server"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "BTAD_SilentMode [environment variable], about BTAS_SilentMode"
  - "BTAD_SilentMode [environment variable]"
  - "BTAD_SilentMode [environment variable], warnings"
ms.assetid: 271835cf-1587-44c5-b5af-b4df4e981ab4
caps.latest.revision: 16
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# BTAD_SilentMode
BTAD_SilentMode specifies options for running the script in silent mode.  
  
## Remarks  
 When you specify an option for silent mode, BTS Installer places its value into the BTAD_SilentMode variable.  
  
 The default value of BTAD_SilentMode is 2, which specifies that the script runs in silent mode. The following table describes the possible values for BTAD_SilentMode.  
  
> [!CAUTION]
>  If you start the BizTalk Server user interface from scripts, modal dialog boxes may not be visible or have focus, making them difficult to view and dismiss. The BizTalk databases can become locked and inaccessible while modal dialog boxes are open. For this reason, on production systems, all scripts should run in silent mode.  
  
|Value|Description|  
|-----------|-----------------|  
|0|Does not change the user interface (UI) level.|  
|1|Uses the default UI level.|  
|2|Performs a silent installation (the default).|  
|3|Provides simple progress and error handling.|  
|4|Provides authored UI; suppresses wizards.|  
|0x80|If combined with any above value, Windows Installer displays a modal dialog box if the script has executed successfully or if there has been an error. No dialog box is displayed if the user cancels the operation.|  
|0x40|If combined with the 3 value, Windows Installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.|  
|0x20|If combined with the 3 value, Windows Installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.|  
|0x100|If combined with the 3 value, Windows Installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.|  
  
## See Also  
 [Pre- and Post-processing Script Environment Variables](../core/pre-and-post-processing-script-environment-variables.md)   
 [How Environment Variables Indicate Deployment State](../core/how-environment-variables-indicate-deployment-state.md)