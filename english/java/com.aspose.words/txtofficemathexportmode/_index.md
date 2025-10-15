---
title: TxtOfficeMathExportMode
linktitle: TxtOfficeMathExportMode
second_title: Aspose.Words for Java
description: Specifies how Aspose.Words exports OfficeMath to SaveFormat.TEXT in Java.
type: docs
weight: 690
url: /java/com.aspose.words/txtofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtOfficeMathExportMode
```

Specifies how Aspose.Words exports OfficeMath to [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT).

 **Examples:** 

Shows how to export OfficeMath object as Latex in TXT.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 TxtSaveOptions saveOptions = new TxtSaveOptions();
 saveOptions.setOfficeMathExportMode(TxtOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [LATEX](#LATEX) | Export OfficeMath as LaTeX. |
| [TEXT](#TEXT) | Export OfficeMath as plain text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String txtOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int txtOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtOfficeMathExportMode)](#toString-int) |  |
### LATEX {#LATEX}
```
public static int LATEX
```


Export OfficeMath as LaTeX.

### TEXT {#TEXT}
```
public static int TEXT
```


Export OfficeMath as plain text.

### length {#length}
```
public static int length
```


### fromName(String txtOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtOfficeMathExportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtOfficeMathExportMode) {#getName-int}
```
public static String getName(int txtOfficeMathExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtOfficeMathExportMode) {#toString-int}
```
public static String toString(int txtOfficeMathExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
