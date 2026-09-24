---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo Aspose.Words exporta OfficeMath a Markdown en Java."
type: docs
weight: 455
url: /es/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

Especifica cómo Aspose.Words exporta OfficeMath a Markdown.

 **Examples:** 

Muestra cómo se escribirá OfficeMath en el documento.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

Muestra cómo exportar el objeto OfficeMath como Latex.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

Muestra cómo exportar el objeto OfficeMath como MarkItDown.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [IMAGE](#IMAGE) | Exportar OfficeMath como imagen. |
| [LATEX](#LATEX) | Exportar OfficeMath como LaTeX. |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | Exportar OfficeMath como LaTeX compatible con MarkItDown. |
| [MATH_ML](#MATH-ML) | Exportar OfficeMath como MathML. |
| [TEXT](#TEXT) | Exportar OfficeMath como texto plano. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Exportar OfficeMath como imagen.

### LATEX {#LATEX}
```
public static int LATEX
```


Exportar OfficeMath como LaTeX.

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


Exportar OfficeMath como LaTeX compatible con MarkItDown.

 **Remarks:** 

Por favor, consulte https://github.com/microsoft/markitdown para obtener detalles sobre MarkItDown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Exportar OfficeMath como MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


Exportar OfficeMath como texto plano.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
