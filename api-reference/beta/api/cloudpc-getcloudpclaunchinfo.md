---
title: "Get my Cloud PC launch info"
description: "Get the cloudPCLaunchInfo for a calling user's Cloud PC"
author: "AndrewKuSZ"
ms.localizationpriority: medium
ms.prod: "cloud-pc"
doc_type: apiPageType
---

# Get my Cloud PC launch info
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the [cloudPCLaunchInfo](../resources/cloudpclaunchinfo.md) for a calling user's Cloud PC

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|CloudPC.Read.All, CloudPC.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /me/cloudPCs/{cloudPCId}/getCloudPcLaunchInfo
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [cloudPcLaunchInfo](../resources/intune-cloudpclaunchinfo.md) in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "cloudpcthis.getcloudpclaunchinfo"
}
-->
``` http
GET https://graph.microsoft.com/beta/me/cloudPCs/{cloudPCId}/getCloudPcLaunchInfo
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.cloudPcLaunchInfo"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://canary.graph.microsoft.com/testprodbetatsku_iws/$metadata#microsoft.graph.cloudPcLaunchInfo",
  "cloudPcId": "a20d556d-85f7-88cc-bb9c-08d9902bb7bb",
  "cloudPcLaunchUrl": "https://rdweb-r0.wvdselfhost.microsoft.com/api/arm/weblaunch/tenants/662009bc-7732-4f6f-8726-25883518b33e/resources/662009bc-7732-4f6f-8726-25883518b33e"
}
```

