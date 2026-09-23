---
title: "MarkdownEmptyParagraphExportMode"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Aspose.Words per Java"
description: "Specifica come Aspose.Words esporta i paragrafi vuoti in Markdown in Java."
type: docs
weight: 450
url: /it/java/com.aspose.words/markdownemptyparagraphexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownEmptyParagraphExportMode
```

Specifica come Aspose.Words esporta i paragrafi vuoti in Markdown.

 **Examples:** 

Mostra come esportare i paragrafi vuoti.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [EMPTY_LINE](#EMPTY-LINE) | Esporta come righe vuote. |
| [MARKDOWN_HARD_LINE_BREAK](#MARKDOWN-HARD-LINE-BREAK) | Esporta come carattere Markdown HardLineBreak '\\\\'. |
| [NONE](#NONE) | Non esportare i paragrafi vuoti. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String markdownEmptyParagraphExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownEmptyParagraphExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownEmptyParagraphExportMode)](#toString-int) |  |
### EMPTY_LINE {#EMPTY-LINE}
```
public static int EMPTY_LINE
```


Esporta come righe vuote.

 **Remarks:** 

Nota, le righe vuote non hanno significato in Markdown e verranno perse al caricamento.

### MARKDOWN_HARD_LINE_BREAK {#MARKDOWN-HARD-LINE-BREAK}
```
public static int MARKDOWN_HARD_LINE_BREAK
```


Esporta come carattere Markdown HardLineBreak '\\\\'.

### NONE {#NONE}
```
public static int NONE
```


Non esportare i paragrafi vuoti.

### length {#length}
```
public static int length
```


### fromName(String markdownEmptyParagraphExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownEmptyParagraphExportModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownEmptyParagraphExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownEmptyParagraphExportMode) {#getName-int}
```
public static String getName(int markdownEmptyParagraphExportMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markdownEmptyParagraphExportMode | int |  |

**Returns:**
java.lang.String
