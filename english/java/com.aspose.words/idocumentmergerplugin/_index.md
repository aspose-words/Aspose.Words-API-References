---
title: IDocumentMergerPlugin
linktitle: IDocumentMergerPlugin
second_title: Aspose.Words for Java
description: Defines an interface for external merger plugin that can merge Pdf documents in Java.
type: docs
weight: 661
url: /java/com.aspose.words/idocumentmergerplugin/
---
```
public interface IDocumentMergerPlugin
```

Defines an interface for external merger plugin that can merge Pdf documents.
## Methods

| Method | Description |
| --- | --- |
| [merge(InputStream outputStream, InputStream[] inputStreams)](#merge-java.io.InputStream-java.io.InputStream...) | Merges the given input PDF documents into a single output PDF document using specified input and output streams. |
### merge(InputStream outputStream, InputStream[] inputStreams) {#merge-java.io.InputStream-java.io.InputStream...}
```
public abstract void merge(InputStream outputStream, InputStream[] inputStreams)
```


Merges the given input PDF documents into a single output PDF document using specified input and output streams.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.InputStream | The output stream. |
| inputStreams | java.io.InputStream[] | The input streams. |

