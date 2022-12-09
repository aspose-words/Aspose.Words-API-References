---
title: IDocumentLoadingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to have your own custom method called during loading a document.
type: docs
weight: 639
url: /java/com.aspose.words/idocumentloadingcallback/
---
```
public interface IDocumentLoadingCallback
```

Implement this interface if you want to have your own custom method called during loading a document.
## Methods

| Method | Description |
| --- | --- |
| [notify(DocumentLoadingArgs args)](#notify-com.aspose.words.DocumentLoadingArgs) | This is called to notify of document loading progress. |
### notify(DocumentLoadingArgs args) {#notify-com.aspose.words.DocumentLoadingArgs}
```
public abstract void notify(DocumentLoadingArgs args)
```


This is called to notify of document loading progress.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../com.aspose.words/documentloadingargs) | An argument of the event. The primary uses for this interface is to allow application code to obtain progress status and abort loading process.

An exception should be threw from the progress callback for abortion and it should be caught in the consumer code. |

