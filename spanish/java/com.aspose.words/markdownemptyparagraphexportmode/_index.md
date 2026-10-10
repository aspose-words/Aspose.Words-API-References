---
title: "MarkdownEmptyParagraphExportMode"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo Aspose.Words exporta párrafos vacíos a Markdown en Java."
type: docs
weight: 450
url: /es/java/com.aspose.words/markdownemptyparagraphexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownEmptyParagraphExportMode
```

Especifica cómo Aspose.Words exporta párrafos vacíos a Markdown.

 **Examples:** 

Muestra cómo exportar párrafos vacíos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("First");
 builder.writeln("\r\n\r\n\r\n");
 builder.writeln("Last");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setEmptyParagraphExportMode(exportMode);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

 String result = FileUtils.readFileToString( new File(getArtifactsDir() + "MarkdownSaveOptions.EmptyParagraphExportMode.md"), StandardCharsets.UTF_8);

 switch (exportMode)
 {
     case MarkdownEmptyParagraphExportMode.NONE:
         Assert.assertEquals("\ufeffFirst\r\n\r\nLast\r\n", result);
         break;
     case MarkdownEmptyParagraphExportMode.EMPTY_LINE:
         Assert.assertEquals("\ufeffFirst\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
         break;
     case MarkdownEmptyParagraphExportMode.MARKDOWN_HARD_LINE_BREAK:
         Assert.assertEquals("\ufeffFirst\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n
\r\n", result);
         break;
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [EMPTY_LINE](#EMPTY-LINE) | Exportar como líneas vacías. |
| [MARKDOWN_HARD_LINE_BREAK](#MARKDOWN-HARD-LINE-BREAK) | Exportar como carácter de salto de línea duro de Markdown '\\'. |
| [NONE](#NONE) | No exportar párrafos vacíos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String markdownEmptyParagraphExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownEmptyParagraphExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownEmptyParagraphExportMode)](#toString-int) |  |
### EMPTY_LINE {#EMPTY-LINE}
```
public static int EMPTY_LINE
```


Exportar como líneas vacías.

 **Remarks:** 

Nota, las líneas vacías no son significativas en Markdown y se perderán al cargar.

### MARKDOWN_HARD_LINE_BREAK {#MARKDOWN-HARD-LINE-BREAK}
```
public static int MARKDOWN_HARD_LINE_BREAK
```


Exportar como carácter de salto de línea duro de Markdown '\\'.

### NONE {#NONE}
```
public static int NONE
```


No exportar párrafos vacíos.

### length {#length}
```
public static int length
```


### fromName(String markdownEmptyParagraphExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownEmptyParagraphExportModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownEmptyParagraphExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownEmptyParagraphExportMode) {#getName-int}
```
public static String getName(int markdownEmptyParagraphExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownEmptyParagraphExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownEmptyParagraphExportMode) {#toString-int}
```
public static String toString(int markdownEmptyParagraphExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markdownEmptyParagraphExportMode | int |  |

**Returns:**
java.lang.String
