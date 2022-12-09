---
title: IDocumentPartSavingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to receive notifications and control how Aspose.Words saves document parts when exporting a document to  or  format.
type: docs
weight: 640
url: /java/com.aspose.words/idocumentpartsavingcallback/
---
```
public interface IDocumentPartSavingCallback
```

Implement this interface if you want to receive notifications and control how Aspose.Words saves document parts when exporting a document to [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) or [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) format.
## Methods

| Method | Description |
| --- | --- |
| [documentPartSaving(DocumentPartSavingArgs args)](#documentPartSaving-com.aspose.words.DocumentPartSavingArgs) | Called when Aspose.Words is about to save a document part. |
### documentPartSaving(DocumentPartSavingArgs args) {#documentPartSaving-com.aspose.words.DocumentPartSavingArgs}
```
public abstract void documentPartSaving(DocumentPartSavingArgs args)
```


Called when Aspose.Words is about to save a document part.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs) |  |

