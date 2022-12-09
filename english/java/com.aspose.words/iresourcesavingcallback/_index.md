---
title: IResourceSavingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to control how Aspose.Words saves external resources images fonts and css when saving a document to fixed page HTML or SVG.
type: docs
weight: 661
url: /java/com.aspose.words/iresourcesavingcallback/
---
```
public interface IResourceSavingCallback
```

Implement this interface if you want to control how Aspose.Words saves external resources (images, fonts and css) when saving a document to fixed page HTML or SVG.
## Methods

| Method | Description |
| --- | --- |
| [resourceSaving(ResourceSavingArgs args)](#resourceSaving-com.aspose.words.ResourceSavingArgs) | Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats. |
### resourceSaving(ResourceSavingArgs args) {#resourceSaving-com.aspose.words.ResourceSavingArgs}
```
public abstract void resourceSaving(ResourceSavingArgs args)
```


Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [ResourceSavingArgs](../../com.aspose.words/resourcesavingargs) |  |

