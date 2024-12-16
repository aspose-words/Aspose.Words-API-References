---
title: Merger
linktitle: Merger
second_title: Aspose.Words for Java
description: Represents a group of methods intended to merge a variety of different types of documents into a single output document in Java.
type: docs
weight: 450
url: /java/com.aspose.words/merger/
---

**Inheritance:**
java.lang.Object
```
public class Merger
```

Represents a group of methods intended to merge a variety of different types of documents into a single output document.

 **Remarks:** 

The specified input and output files or streams, along with the desired merge and save options, are used to merge the given input documents into a single output document.

The merging functionality supports over 35 different file formats.

 **Examples:** 

Shows how to merge documents into a single output document.

```

 //There is a several ways to merge documents:
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.SimpleMerge.docx", new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" });

 OoxmlSaveOptions ooxmlSaveOptions = new OoxmlSaveOptions();
 ooxmlSaveOptions.setPassword("Aspose.Words");
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.SaveOptions.docx", new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" }, ooxmlSaveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.SaveFormat.pdf", new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" }, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 Document doc = Merger.merge(new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" }, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.DocumentInstance.docx");
 
```
## Methods

| Method | Description |
| --- | --- |
| [merge(Document[] inputDocuments, int mergeFormatMode)](#merge-com.aspose.words.Document---int) |  |
| [merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.io.InputStream---com.aspose.words.LoadOptions---int) |  |
| [merge(InputStream[] inputStreams, int mergeFormatMode)](#merge-java.io.InputStream---int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat)](#merge-java.io.OutputStream-java.io.InputStream---int) |  |
| [merge(String outputFile, String[] inputFiles)](#merge-java.lang.String-java.lang.String) | Merges the given input documents into a single output document using specified input and output file names. |
| [merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---int-int) |  |
| [merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.lang.String---com.aspose.words.LoadOptions---int) |  |
| [merge(String[] inputFiles, int mergeFormatMode)](#merge-java.lang.String---int) |  |
### merge(Document[] inputDocuments, int mergeFormatMode) {#merge-com.aspose.words.Document---int}
```
public static Document merge(Document[] inputDocuments, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputDocuments | [Document\[\]](../../com.aspose.words/document/) |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode) {#merge-java.io.InputStream---com.aspose.words.LoadOptions---int}
```
public static Document merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStreams | java.io.InputStream[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(InputStream[] inputStreams, int mergeFormatMode) {#merge-java.io.InputStream---int}
```
public static Document merge(InputStream[] inputStreams, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStreams | java.io.InputStream[] |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int}
```
public static void merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.SaveOptions-int}
```
public static void merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat) {#merge-java.io.OutputStream-java.io.InputStream---int}
```
public static void merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveFormat | int |  |

### merge(String outputFile, String[] inputFiles) {#merge-java.lang.String-java.lang.String}
```
public static void merge(String outputFile, String[] inputFiles)
```


Merges the given input documents into a single output document using specified input and output file names.

 **Remarks:** 

By default [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING) is used.

 **Examples:** 

Shows how to merge documents into a single output document.

```

 //There is a several ways to merge documents:
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.SimpleMerge.docx", new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" });

 OoxmlSaveOptions ooxmlSaveOptions = new OoxmlSaveOptions();
 ooxmlSaveOptions.setPassword("Aspose.Words");
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.SaveOptions.docx", new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" }, ooxmlSaveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.SaveFormat.pdf", new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" }, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 Document doc = Merger.merge(new String[] { getMyDir() + "Big document.docx", getMyDir() + "Tables.docx" }, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.DocumentInstance.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | java.lang.String | The output file name. |
| inputFiles | java.lang.String[] | The input file names. |

### merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int}
```
public static void merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | java.lang.String |  |
| inputFiles | java.lang.String[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---com.aspose.words.SaveOptions-int}
```
public static void merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | java.lang.String |  |
| inputFiles | java.lang.String[] |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---int-int}
```
public static void merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | java.lang.String |  |
| inputFiles | java.lang.String[] |  |
| saveFormat | int |  |
| mergeFormatMode | int |  |

### merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode) {#merge-java.lang.String---com.aspose.words.LoadOptions---int}
```
public static Document merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFiles | java.lang.String[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(String[] inputFiles, int mergeFormatMode) {#merge-java.lang.String---int}
```
public static Document merge(String[] inputFiles, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFiles | java.lang.String[] |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
