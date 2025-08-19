---
title: MergeFormatMode
linktitle: MergeFormatMode
second_title: Aspose.Words for Java
description: Specifies how formatting is merged when combining multiple documents in Java.
type: docs
weight: 459
url: /java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

Specifies how formatting is merged when combining multiple documents.

 **Examples:** 

Shows how to merge documents into a single output document.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Means that the source document will retain its original formatting, such as font styles, sizes, colors, indents, and any other formatting elements applied to its content. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | Preserve the layout of the original documents in the final document. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | Combine the formatting of the merged documents. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Means that the source document will retain its original formatting, such as font styles, sizes, colors, indents, and any other formatting elements applied to its content.

 **Remarks:** 

By using this option, you ensure that the copied content appears as it did in the original source, regardless of the formatting settings of the first document in merge queue.

This option does not have any affect when the input and the output formats are PDF.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


Preserve the layout of the original documents in the final document.

 **Remarks:** 

In general, it looks like you print out the original documents and manually adhere them together using glue.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


Combine the formatting of the merged documents.

 **Remarks:** 

By using this option, Aspose.Words adapts the formatting of the first document to match the structure and appearance of the second document, but keeps some of the original formatting intact. This option is useful when you want to maintain the overall look and feel of the destination document but still retain certain formatting aspects from the original document.

This option does not have any affect when the input and the output formats are PDF.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
