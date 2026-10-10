---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words per Java"
description: "Specifica come Aspose.Words esporta OfficeMath in Markdown in Java."
type: docs
weight: 455
url: /it/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

Specifica come Aspose.Words esporta OfficeMath in Markdown.

 **Examples:** 

Mostra come OfficeMath verrà scritto nel documento.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

Mostra come esportare l'oggetto OfficeMath come Latex.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

Mostra come esportare l'oggetto OfficeMath come MarkItDown.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [IMAGE](#IMAGE) | Esporta OfficeMath come immagine. |
| [LATEX](#LATEX) | Esporta OfficeMath come LaTeX. |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | Esporta OfficeMath come LaTeX compatibile con MarkItDown. |
| [MATH_ML](#MATH-ML) | Esporta OfficeMath come MathML. |
| [TEXT](#TEXT) | Esporta OfficeMath come testo semplice. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Esporta OfficeMath come immagine.

### LATEX {#LATEX}
```
public static int LATEX
```


Esporta OfficeMath come LaTeX.

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


Esporta OfficeMath come LaTeX compatibile con MarkItDown.

 **Remarks:** 

Consulta https://github.com/microsoft/markitdown per i dettagli su MarkItDown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Esporta OfficeMath come MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


Esporta OfficeMath come testo semplice.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
