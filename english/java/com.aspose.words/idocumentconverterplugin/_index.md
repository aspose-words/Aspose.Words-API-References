---
title: IDocumentConverterPlugin
linktitle: IDocumentConverterPlugin
second_title: Aspose.Words for Java
description: Defines an interface for external converter plugin in Java.
type: docs
weight: 661
url: /java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Defines an interface for external converter plugin.
## Methods

| Method | Description |
| --- | --- |
| [convert(InputStream inputStream, InputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.InputStream-com.aspose.words.SaveOptions) | Converts document using specified input output streams and save options. |
### convert(InputStream inputStream, InputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-java.io.InputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, InputStream outputStream, SaveOptions saveOptions)
```


Converts document using specified input output streams and save options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input stream. |
| outputStream | java.io.InputStream | The output stream. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |

