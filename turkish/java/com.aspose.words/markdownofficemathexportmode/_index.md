---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words Java için"
description: "Aspose.Words'in OfficeMath'i Java'da Markdown'e nasıl dışa aktardığını belirtir."
type: docs
weight: 455
url: /tr/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

Aspose.Words'un OfficeMath'ı Markdown'a nasıl dışa aktardığını belirtir.

 **Examples:** 

OfficeMath'in belgeye nasıl yazılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

OfficeMath nesnesinin Latex olarak nasıl dışa aktarılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

OfficeMath nesnesinin MarkItDown olarak nasıl dışa aktarılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [IMAGE](#IMAGE) | OfficeMath'i resim olarak dışa aktar. |
| [LATEX](#LATEX) | OfficeMath'i LaTeX olarak dışa aktar. |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | OfficeMath'i MarkItDown ile uyumlu LaTeX olarak dışa aktar. |
| [MATH_ML](#MATH-ML) | OfficeMath'i MathML olarak dışa aktar. |
| [TEXT](#TEXT) | OfficeMath'i düz metin olarak dışa aktar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


OfficeMath'i resim olarak dışa aktar.

### LATEX {#LATEX}
```
public static int LATEX
```


OfficeMath'i LaTeX olarak dışa aktar.

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


OfficeMath'i MarkItDown ile uyumlu LaTeX olarak dışa aktar.

 **Remarks:** 

MarkItDown hakkında ayrıntılar için https://github.com/microsoft/markitdown adresine bakın.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


OfficeMath'i MathML olarak dışa aktar.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath'i düz metin olarak dışa aktar.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
