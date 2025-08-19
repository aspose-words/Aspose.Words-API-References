---
title: MarkdownOfficeMathExportMode
linktitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words for Java
description: Specifies how Aspose.Words exports OfficeMath to Markdown in Java.
type: docs
weight: 450
url: /java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

Specifies how Aspose.Words exports OfficeMath to Markdown.

 **Examples:** 

Shows how OfficeMath will be written to the document.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [IMAGE](#IMAGE) | Export OfficeMath as image. |
| [MATH_ML](#MATH-ML) | Export OfficeMath as MathML. |
| [TEXT](#TEXT) | Export OfficeMath as plain text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Export OfficeMath as image.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Export OfficeMath as MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


Export OfficeMath as plain text.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownOfficeMathExportMode) {#toString-int}
```
public static String toString(int markdownOfficeMathExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
