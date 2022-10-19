---
title: ResourceLoadingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the  method.
type: docs
weight: 480
url: /java/com.aspose.words/resourceloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingArgs
```

Provides data for the [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) method.
## Methods

| Method | Description |
| --- | --- |
| [getResourceType()](#getResourceType--) | Type of resource. |
| [getUri()](#getUri--) | URI of the resource which is used for downloading if [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) returns [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT). |
| [setUri(String value)](#setUri-java.lang.String-) | URI of the resource which is used for downloading if [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) returns [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT). |
| [getOriginalUri()](#getOriginalUri--) | Original URI of the resource as specified in imported document. |
| [setData(byte[] data)](#setData-byte---) | Sets user provided data of the resource which is used if [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) returns [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction\#USER-PROVIDED). |
### getResourceType() {#getResourceType--}
```
public int getResourceType()
```


Type of resource.

**Returns:**
int - The corresponding  int  value. The returned value is one of [ResourceType](../../com.aspose.words/resourcetype) constants.
### getUri() {#getUri--}
```
public String getUri()
```


URI of the resource which is used for downloading if [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) returns [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT).

Initially it's set to absolute URI of the resource, but user can redefine it to any value.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setUri(String value) {#setUri-java.lang.String-}
```
public void setUri(String value)
```


URI of the resource which is used for downloading if [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) returns [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT).

Initially it's set to absolute URI of the resource, but user can redefine it to any value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getOriginalUri() {#getOriginalUri--}
```
public String getOriginalUri()
```


Original URI of the resource as specified in imported document.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setData(byte[] data) {#setData-byte---}
```
public void setData(byte[] data)
```


Sets user provided data of the resource which is used if [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) returns [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction\#USER-PROVIDED).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| data | byte[] |  |

