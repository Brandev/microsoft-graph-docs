---
title: "List delegatedAdminCustomers"
description: "Get a list of the delegatedAdminCustomer objects and their properties."
author: "adtangir"
ms.localizationpriority: medium
ms.prod: "partnercustomersvcadmin"
doc_type: apiPageType
---

# List delegatedAdminCustomers
Namespace: microsoft.partner.customerServiceAdministration



Get a list of the [delegatedAdminCustomer](../resources/delegatedadmincustomer.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)| DelegatedAdminRelationship.Read.All, DelegatedAdminRelationship.ReadWrite.All |
|Delegated (personal Microsoft account)| Not Supported. |
|Application| Not Supported. |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /tenantRelationship/delegatedAdminCustomers
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [delegatedAdminCustomer](../resources/delegatedadmincustomer.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_delegatedadmincustomer"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/tenantRelationship/delegatedAdminCustomers
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.partner.customerServiceAdministration.delegatedAdminCustomer)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.partner.customerServiceAdministration.delegatedAdminCustomer",
      "id": "2cf4d9a5-5661-8858-da96-13b707815d8a",
      "tenantId": "String",
      "displayName": "String"
    }
  ]
}
```

