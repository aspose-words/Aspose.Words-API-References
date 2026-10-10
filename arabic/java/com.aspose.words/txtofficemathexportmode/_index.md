---
title: "TxtOfficeMathExportMode"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى SaveFormat.TEXT في Java."
type: docs
weight: 694
url: /ar/java/com.aspose.words/txtofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtOfficeMathExportMode
```

يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT).

 **Examples:** 

يظهر كيفية تصدير كائن OfficeMath كـ Latex في TXT.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 TxtSaveOptions saveOptions = new TxtSaveOptions();
 saveOptions.setOfficeMathExportMode(TxtOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [LATEX](#LATEX) | تصدير OfficeMath كـ LaTeX. |
| [TEXT](#TEXT) | تصدير OfficeMath كنص عادي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String txtOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int txtOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtOfficeMathExportMode)](#toString-int) |  |
### LATEX {#LATEX}
```
public static int LATEX
```


تصدير OfficeMath كـ LaTeX.

### TEXT {#TEXT}
```
public static int TEXT
```


تصدير OfficeMath كنص عادي.

### length {#length}
```
public static int length
```


### fromName(String txtOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtOfficeMathExportModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| txtOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtOfficeMathExportMode) {#getName-int}
```
public static String getName(int txtOfficeMathExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
