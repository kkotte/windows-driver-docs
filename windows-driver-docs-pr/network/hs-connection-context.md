---
title: HS\_CONNECTION\_CONTEXT structure
author: windows-driver-content
description: The HS\_CONNECTION\_CONTEXT structure contains the information required by the plugin for post connect authentication.
ms.assetid: 22b219fc-691b-4813-a523-a76de037e64d
keywords: 
- HS_CONNECTION_CONTEXT structure Network Drivers Starting with Windows Vista
- PHS_CONNECTION_CONTEXT structure pointer Network Drivers Starting with Windows Vista
ms.author: windowsdriverdev
ms.date: 07/31/2017 
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# HS\_CONNECTION\_CONTEXT structure


The **HS\_CONNECTION\_CONTEXT** structure contains the information required by the plugin for post connect authentication.

Syntax
------

```ManagedCPlusPlus
typedef struct _HS_CONNECTION_CONTEXT {
  HS_MAC_ADDRESS  MacAddress;
  HS_SIM_IDENTITY SIMIdentity;
  WCHAR           pszPhoneNumber[HS_MAX_PHONE_NUMBER_LENGTH+1];
} HS_CONNECTION_CONTEXT, *PHS_CONNECTION_CONTEXT;
```

Members
-------

**MacAddress**  
The [**HS\_MAC\_ADDRESS**](hs-mac-address.md) structure that contains the MAC address.

**SIMIdentity**  
The [**HS\_SIM\_IDENTITY**](hs-sim-identity.md) structure that contains information required for EAP-SIM/AKA authentication.

**pszPhoneNumber**  
Pointer to the phone number.

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Hotspotoffloadplugin.h (include Hotspotoffloadplugin.h)</td>
</tr>
</tbody>
</table>

## See also


[**HS\_MAC\_ADDRESS**](hs-mac-address.md)

[**HS\_SIM\_IDENTITY**](hs-sim-identity.md)

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bnetvista\netvista%5D:%20HS_CONNECTION_CONTEXT%20structure%20%20RELEASE:%20%287/31/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


