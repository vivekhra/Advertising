---
title: BatchError Data Object - Ad Insight
ms.service: bing-ads-ad-insight-service
ms.topic: article
author: rgaritta
ms.author: v-rgaritta
description: Defines an Ad Insight batch error object that identifies the item within the batch of items in the request message that caused the operation to fail, and describes the reason for the failure.
---
# BatchError Data Object - Ad Insight
Defines an Ad Insight batch error object that identifies the item within the batch of items in the request message that caused the operation to fail, and describes the reason for the failure.

## Syntax
```xml
<xs:complexType name="BatchError" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:sequence>
    <xs:element minOccurs="0" name="Code" type="xs:int" />
    <xs:element minOccurs="0" name="Details" nillable="true" type="xs:string" />
    <xs:element minOccurs="0" name="ErrorCode" nillable="true" type="xs:string" />
    <xs:element minOccurs="0" name="Index" type="xs:int" />
    <xs:element minOccurs="0" name="Message" nillable="true" type="xs:string" />
  </xs:sequence>
</xs:complexType>
```

## <a name="elements"></a>Elements

The [BatchError](batcherror.md) object has the following elements: [Code](#code), [Details](#details), [ErrorCode](#errorcode), [Index](#index), [Message](#message).

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="code"></a>Code|A numeric error code that identifies the error.|**int**|
|<a name="details"></a>Details|A message that provides additional details about the batch error. This string can be empty.|**string**|
|<a name="errorcode"></a>ErrorCode|A symbolic string constant that identifies the error. For example, *UserIsNotAuthorized*.|**string**|
|<a name="index"></a>Index|The zero-based index of the item in the batch of items in the request message that failed.|**int**|
|<a name="message"></a>Message|A message that describes the error.<br/><br/>For more information about troubleshooting and error handling, see [Handling Service Errors and Exceptions](../guides/handle-service-errors-exceptions.md) and [Operation Error Codes](../guides/operation-error-codes.md).|**string**|

## Requirements
Service: [AdInsightService.svc v13](https://adinsight.api.bingads.microsoft.com/Api/Advertiser/AdInsight/v13/AdInsightService.svc)  
Namespace: https\://bingads.microsoft.com/AdInsight/v13  

## Used By
[ApiFaultDetail](apifaultdetail.md)  
[SetAutoApplyOptInStatus](setautoapplyoptinstatus.md)  
[TagRecommendations](tagrecommendations.md)  
