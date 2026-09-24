---
title: "TxtOfficeMathExportMode"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words Java için"
description: "Aspose.Words'ün OfficeMath'i Java'da SaveFormat.TEXT formatına nasıl dışa aktardığını belirtir."
type: docs
weight: 694
url: /tr/java/com.aspose.words/txtofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtOfficeMathExportMode
```

Aspose.Words'ün OfficeMath'i [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT) formatına nasıl dışa aktardığını belirtir.

 **Examples:** 

OfficeMath nesnesinin TXT içinde LaTeX olarak nasıl dışa aktarılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 TxtSaveOptions saveOptions = new TxtSaveOptions();
 saveOptions.setOfficeMathExportMode(TxtOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [LATEX](#LATEX) | OfficeMath'i LaTeX olarak dışa aktar. |
| [TEXT](#TEXT) | OfficeMath'i düz metin olarak dışa aktar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String txtOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int txtOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtOfficeMathExportMode)](#toString-int) |  |
### LATEX {#LATEX}
```
public static int LATEX
```


OfficeMath'i LaTeX olarak dışa aktar.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath'i düz metin olarak dışa aktar.

### length {#length}
```
public static int length
```


### fromName(String txtOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtOfficeMathExportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtOfficeMathExportMode) {#getName-int}
```
public static String getName(int txtOfficeMathExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
