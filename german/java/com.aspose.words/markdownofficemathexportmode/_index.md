---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Aspose.Words OfficeMath in Java nach Markdown exportiert."
type: docs
weight: 455
url: /de/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

Gibt an, wie Aspose.Words OfficeMath nach Markdown exportiert.

 **Examples:** 

Zeigt, wie OfficeMath in das Dokument geschrieben wird.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

Zeigt, wie das OfficeMath‑Objekt als LaTeX exportiert wird.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

Zeigt, wie das OfficeMath‑Objekt als MarkItDown exportiert wird.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [IMAGE](#IMAGE) | Exportiert OfficeMath als Bild. |
| [LATEX](#LATEX) | Exportiere OfficeMath als LaTeX. |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | Exportiert OfficeMath als LaTeX, das mit MarkItDown kompatibel ist. |
| [MATH_ML](#MATH-ML) | Exportiert OfficeMath als MathML. |
| [TEXT](#TEXT) | Exportiere OfficeMath als Klartext. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Exportiert OfficeMath als Bild.

### LATEX {#LATEX}
```
public static int LATEX
```


Exportiere OfficeMath als LaTeX.

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


Exportiert OfficeMath als LaTeX, das mit MarkItDown kompatibel ist.

 **Remarks:** 

Bitte siehe https://github.com/microsoft/markitdown für Details zu MarkItDown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Exportiert OfficeMath als MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


Exportiere OfficeMath als Klartext.

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
