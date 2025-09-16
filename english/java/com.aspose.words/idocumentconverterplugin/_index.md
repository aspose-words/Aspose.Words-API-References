---
title: IDocumentConverterPlugin
linktitle: IDocumentConverterPlugin
second_title: Aspose.Words for Java
description: Defines an interface for external converter plugin in Java.
type: docs
weight: 753
url: /java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Defines an interface for external converter plugin.
## Methods

| Method | Description |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions) | Converts pages from document from input stream to array of images. |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions}
```
public abstract OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)
```


Converts pages from document from input stream to array of images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input stream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | The document load options. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |

**Returns:**
java.io.OutputStream[] - Array of page images streams.
