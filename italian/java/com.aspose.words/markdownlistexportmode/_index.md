---
title: "MarkdownListExportMode"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words per Java"
description: "Specifica come le liste vengono esportate in Markdown in Java."
type: docs
weight: 453
url: /it/java/com.aspose.words/markdownlistexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownListExportMode
```

Specifica come le liste vengono esportate in Markdown.

 **Examples:** 

Mostra come gli elementi dell'elenco verranno scritti nel documento markdown.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [MARKDOWN_SYNTAX](#MARKDOWN-SYNTAX) | Esporta gli elementi dell'elenco compatibili con la sintassi Markdown. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Esporta gli elementi dell'elenco come testo semplice. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String markdownListExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownListExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownListExportMode)](#toString-int) |  |
### MARKDOWN_SYNTAX {#MARKDOWN-SYNTAX}
```
public static int MARKDOWN_SYNTAX
```


Esporta gli elementi dell'elenco compatibili con la sintassi Markdown.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Esporta gli elementi dell'elenco come testo semplice.

### length {#length}
```
public static int length
```


### fromName(String markdownListExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownListExportModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownListExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownListExportMode) {#getName-int}
```
public static String getName(int markdownListExportMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String
