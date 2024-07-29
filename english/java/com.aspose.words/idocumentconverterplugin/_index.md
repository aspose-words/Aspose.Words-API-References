---
title: IDocumentConverterPlugin
linktitle: IDocumentConverterPlugin
second_title: Aspose.Words for Java
description: Defines an interface for external converter plugin in Java.
type: docs
weight: 696
url: /java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Defines an interface for external converter plugin.
## Methods

| Method | Description |
| --- | --- |
| [convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.SaveOptions) | Converts pages from document from input stream to array of images. |
### convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.SaveOptions}
```
public abstract InputStream[] convertToImages(InputStream inputStream, SaveOptions saveOptions)
```


Converts pages from document from input stream to array of images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input stream. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |

**Returns:**
java.io.InputStream[] - Array of page images streams.
