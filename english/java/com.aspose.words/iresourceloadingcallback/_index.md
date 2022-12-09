---
title: IResourceLoadingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to control how Aspose.Words loads external resource when importing a document and inserting images using .
type: docs
weight: 660
url: /java/com.aspose.words/iresourceloadingcallback/
---
```
public interface IResourceLoadingCallback
```

Implement this interface if you want to control how Aspose.Words loads external resource when importing a document and inserting images using [DocumentBuilder](../../com.aspose.words/documentbuilder).
## Methods

| Method | Description |
| --- | --- |
| [resourceLoading(ResourceLoadingArgs args)](#resourceLoading-com.aspose.words.ResourceLoadingArgs) | Called when Aspose.Words loads any external resource. |
### resourceLoading(ResourceLoadingArgs args) {#resourceLoading-com.aspose.words.ResourceLoadingArgs}
```
public abstract int resourceLoading(ResourceLoadingArgs args)
```


Called when Aspose.Words loads any external resource.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [ResourceLoadingArgs](../../com.aspose.words/resourceloadingargs) |  |

**Returns:**
int
