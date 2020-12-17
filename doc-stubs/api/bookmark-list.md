---
title: "List bookmarks"
description: "Get a list of the bookmark objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List bookmarks
Namespace: microsoft.graph

Get a list of the [bookmark](../resources/bookmark.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /bookmarks
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

If successful, this method returns a `200 OK` response code and a collection of [bookmark](../resources/bookmark.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_bookmark"
}
-->
``` http
GET https://graph.microsoft.com/beta/bookmarks
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.bookmark)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.bookmark",
      "id": "1f25a012-a012-1f25-12a0-251f12a0251f",
      "displayName": "String",
      "description": "String",
      "webUrl": "String",
      "lastModifiedBy": {
        "@odata.type": "microsoft.graph.identitySet"
      },
      "lastModifiedDateTime": "String (timestamp)",
      "categories": [
        "String"
      ],
      "availabilityStartDateTime": "String (timestamp)",
      "availabilityEndDateTime": "String (timestamp)",
      "languageTags": [
        "String"
      ],
      "platforms": [
        "String"
      ],
      "targetedVariations": [
        {
          "@odata.type": "microsoft.graph.searchAdminVariant"
        }
      ],
      "powerAppIds": [
        "String"
      ],
      "keywords": {
        "@odata.type": "microsoft.graph.answerKeyword"
      },
      "state": "String",
      "isSuggested": "Boolean",
      "groupIds": [
        "String"
      ]
    }
  ]
}
```
