---
title: IDocumentSavingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to have your own custom method called during saving a document.
type: docs
weight: 643
url: /java/com.aspose.words/idocumentsavingcallback/
---
```
public interface IDocumentSavingCallback
```

Implement this interface if you want to have your own custom method called during saving a document.
## Methods

| Method | Description |
| --- | --- |
| [notify(DocumentSavingArgs args)](#notify-com.aspose.words.DocumentSavingArgs) | This is called to notify of document saving progress. |
### notify(DocumentSavingArgs args) {#notify-com.aspose.words.DocumentSavingArgs}
```
public abstract void notify(DocumentSavingArgs args)
```


This is called to notify of document saving progress.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [DocumentSavingArgs](../../com.aspose.words/documentsavingargs) | An argument of the event. The primary uses for this interface is to allow application code to obtain progress status and abort saving process.

An exception should be threw from the progress callback for abortion and it should be caught in the consumer code. |

