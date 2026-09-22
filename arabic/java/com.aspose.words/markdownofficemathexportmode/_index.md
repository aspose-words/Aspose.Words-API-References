---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى Markdown في Java."
type: docs
weight: 455
url: /ar/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى Markdown.

 **Examples:** 

يظهر كيفية كتابة OfficeMath إلى المستند.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

يظهر كيفية تصدير كائن OfficeMath كـ Latex.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

يظهر كيفية تصدير كائن OfficeMath كـ MarkItDown.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [IMAGE](#IMAGE) | تصدير OfficeMath كصورة. |
| [LATEX](#LATEX) | تصدير OfficeMath كـ LaTeX. |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | تصدير OfficeMath كـ LaTeX متوافق مع MarkItDown. |
| [MATH_ML](#MATH-ML) | تصدير OfficeMath كـ MathML. |
| [TEXT](#TEXT) | تصدير OfficeMath كنص عادي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


تصدير OfficeMath كصورة.

### LATEX {#LATEX}
```
public static int LATEX
```


تصدير OfficeMath كـ LaTeX.

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


تصدير OfficeMath كـ LaTeX متوافق مع MarkItDown.

 **Remarks:** 

يرجى الاطلاع على https://github.com/microsoft/markitdown للحصول على تفاصيل حول MarkItDown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


تصدير OfficeMath كـ MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


تصدير OfficeMath كنص عادي.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
