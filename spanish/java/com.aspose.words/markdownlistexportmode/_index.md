---
title: "MarkdownListExportMode"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se exportan las listas a Markdown en Java."
type: docs
weight: 453
url: /es/java/com.aspose.words/markdownlistexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownListExportMode
```

Especifica cómo se exportan las listas a Markdown.

 **Examples:** 

Muestra cómo se escribirán los elementos de la lista en el documento markdown.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [MARKDOWN_SYNTAX](#MARKDOWN-SYNTAX) | Exportar elementos de lista compatibles con la sintaxis Markdown. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Exportar elementos de lista como texto sin formato. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String markdownListExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownListExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownListExportMode)](#toString-int) |  |
### MARKDOWN_SYNTAX {#MARKDOWN-SYNTAX}
```
public static int MARKDOWN_SYNTAX
```


Exportar elementos de lista compatibles con la sintaxis Markdown.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Exportar elementos de lista como texto sin formato.

### length {#length}
```
public static int length
```


### fromName(String markdownListExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownListExportModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownListExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownListExportMode) {#getName-int}
```
public static String getName(int markdownListExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String
