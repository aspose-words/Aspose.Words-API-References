---
title: "MarkdownListExportMode"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Listen in Java nach Markdown exportiert werden."
type: docs
weight: 453
url: /de/java/com.aspose.words/markdownlistexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownListExportMode
```

Gibt an, wie Listen nach Markdown exportiert werden.

 **Examples:** 

Zeigt, wie Listenelemente in das Markdown‑Dokument geschrieben werden.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [MARKDOWN_SYNTAX](#MARKDOWN-SYNTAX) | Exportiere Listenelemente, die mit der Markdown‑Syntax kompatibel sind. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Exportiere Listenelemente als Klartext. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String markdownListExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownListExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownListExportMode)](#toString-int) |  |
### MARKDOWN_SYNTAX {#MARKDOWN-SYNTAX}
```
public static int MARKDOWN_SYNTAX
```


Exportiere Listenelemente, die mit der Markdown‑Syntax kompatibel sind.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Exportiere Listenelemente als Klartext.

### length {#length}
```
public static int length
```


### fromName(String markdownListExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownListExportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownListExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownListExportMode) {#getName-int}
```
public static String getName(int markdownListExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownListExportMode) {#toString-int}
```
public static String toString(int markdownListExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String
