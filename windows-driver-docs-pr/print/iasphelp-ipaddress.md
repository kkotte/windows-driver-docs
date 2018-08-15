---
title: Iasphelp get\_IPAddress method
author: windows-driver-content
description: The IPAddress property enables an ASP Web page to obtain a printer's IP address.
MS-HAID:
- 'webfnc\_f0b5a4c6-50db-48a0-a10d-2a835cac32ac.xml'
- 'print.iasphelp\_ipaddress'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 535ea9fa-fff7-47fd-84ae-f61526f1b622
keywords: ["get_IPAddress method Print Devices", "get_IPAddress method Print Devices , Iasphelp interface", "Iasphelp interface Print Devices , get_IPAddress method"]
topic_type:
- apiref
api_name:
- Iasphelp.get_IPAddress
api_type:
- COM
ms.localizationpriority: medium
---

# Iasphelp::get\_IPAddress method


The **IPAddress** property enables an ASP Web page to obtain a printer's IP address.

Syntax
------

```ManagedCPlusPlus
HRESULT get_IPAddress(
  [out] BSTR *pVal
);
```

Parameters
----------

*pVal* \[out\]  
Caller-supplied pointer to a location to receive a pointer to an IP address string.

Return value
------------

Win32 error codes can also be returned.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Return code</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>S_OK</strong></td>
<td><p>The operation succeeded.</p></td>
</tr>
<tr class="even">
<td><strong>E_HANDLE</strong></td>
<td><p>The <strong>Iasphelp::Open</strong> method has not been called.</p></td>
</tr>
<tr class="odd">
<td><strong>E_OUTOFMEMORY</strong></td>
<td><p>Out of memory.</p></td>
</tr>
</tbody>
</table>

 

## <span id="ddk_iasphelp_ipaddress_gg"></span><span id="DDK_IASPHELP_IPADDRESS_GG"></span>


### <span id="vbscript_example"></span><span id="VBSCRIPT_EXAMPLE"></span>VBScript Example

Remarks
-------

The [**Iasphelp::Open**](iasphelp-open.md) method must be called before the **Iasphelp::IPAddress** property can be queried.

If the printer is not supported by the TCP/IP port monitor, the returned string is empty.

```
    Dim objPrinter, PrinterIP
    strPrinter = Session("MS_printer")
    Set objPrinter = Server.CreateObject ("OlePrn.AspHelp")
    objPrinter.Open strPrinter
    PrinterIP = objPrinter.IPAddress
```

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Target platform</p></td>
<td>Desktop</td>
</tr>
<tr class="even">
<td><p>Version</p></td>
<td><p>Available in Windows 2000 and later versions of the Windows operating systems.</p></td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**Iasphelp::Open**](iasphelp-open.md)

 

 



