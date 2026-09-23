---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment Aspose.Words exporte OfficeMath vers Markdown en Java."
type: docs
weight: 455
url: /fr/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

Spécifie comment Aspose.Words exporte OfficeMath vers Markdown.

 **Examples:** 

Montre comment OfficeMath sera écrit dans le document.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

Montre comment exporter l'objet OfficeMath au format Latex.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

Montre comment exporter l'objet OfficeMath au format MarkItDown.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [IMAGE](#IMAGE) | Exporter OfficeMath en tant qu'image. |
| [LATEX](#LATEX) | Exporter OfficeMath en LaTeX. |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | Exporter OfficeMath en LaTeX compatible avec MarkItDown. |
| [MATH_ML](#MATH-ML) | Exporter OfficeMath en MathML. |
| [TEXT](#TEXT) | Exporter OfficeMath en texte brut. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Exporter OfficeMath en tant qu'image.

### LATEX {#LATEX}
```
public static int LATEX
```


Exporter OfficeMath en LaTeX.

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


Exporter OfficeMath en LaTeX compatible avec MarkItDown.

 **Remarks:** 

Veuillez consulter https://github.com/microsoft/markitdown pour plus de détails sur MarkItDown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Exporter OfficeMath en MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


Exporter OfficeMath en texte brut.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
