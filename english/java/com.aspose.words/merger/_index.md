---
title: Merger
linktitle: Merger
second_title: Aspose.Words for Java
description: Represents a group of methods intended to merge a variety of different types of documents into a single output document in Java.
type: docs
weight: 414
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
## Methods

| Method | Description |
| --- | --- |
| [merge(InputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.InputStream-java.io.InputStream---com.aspose.words.SaveOptions-int) |  |
| [merge(InputStream outputStream, InputStream[] inputStreams, int saveFormat)](#merge-java.io.InputStream-java.io.InputStream---int) |  |
| [merge(InputStream[] inputStreams, int mergeFormatMode)](#merge-java.io.InputStream---int) |  |
| [merge(String outputFile, String[] inputFiles)](#merge-java.lang.String-java.lang.String) | Merges the given input documents into a single output document using specified input and output file names. |
| [merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---int-int) |  |
| [merge(String[] inputFiles, int mergeFormatMode)](#merge-java.lang.String---int) |  |
### merge(InputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.io.InputStream-java.io.InputStream---com.aspose.words.SaveOptions-int}
```
public static void merge(InputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.InputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(InputStream outputStream, InputStream[] inputStreams, int saveFormat) {#merge-java.io.InputStream-java.io.InputStream---int}
```
public static void merge(InputStream outputStream, InputStream[] inputStreams, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.InputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveFormat | int |  |

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
### merge(String outputFile, String[] inputFiles) {#merge-java.lang.String-java.lang.String}
```
public static void merge(String outputFile, String[] inputFiles)
```


Merges the given input documents into a single output document using specified input and output file names.

 **Remarks:** 

By default [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING) is used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | java.lang.String | The output file name. |
| inputFiles | java.lang.String[] | The input file names. |

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
