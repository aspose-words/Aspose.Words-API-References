---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как Aspose.Words экспортирует OfficeMath в Markdown на Java."
type: docs
weight: 455
url: /ru/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

Указывает, как Aspose.Words экспортирует OfficeMath в Markdown.

 **Examples:** 

Показывает, как OfficeMath будет записан в документ.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

Показывает, как экспортировать объект OfficeMath в формате Latex.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

Показывает, как экспортировать объект OfficeMath в формате MarkItDown.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [IMAGE](#IMAGE) | Экспортировать OfficeMath как изображение. |
| [LATEX](#LATEX) | Экспортировать OfficeMath как LaTeX. |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | Экспортировать OfficeMath как LaTeX, совместимый с MarkItDown. |
| [MATH_ML](#MATH-ML) | Экспортировать OfficeMath как MathML. |
| [TEXT](#TEXT) | Экспортировать OfficeMath как обычный текст. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Экспортировать OfficeMath как изображение.

### LATEX {#LATEX}
```
public static int LATEX
```


Экспортировать OfficeMath как LaTeX.

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


Экспортировать OfficeMath как LaTeX, совместимый с MarkItDown.

 **Remarks:** 

Пожалуйста, см. https://github.com/microsoft/markitdown для получения подробностей о MarkItDown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Экспортировать OfficeMath как MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


Экспортировать OfficeMath как обычный текст.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
