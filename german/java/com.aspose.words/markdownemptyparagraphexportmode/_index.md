---
title: "MarkdownEmptyParagraphExportMode"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Aspose.Words leere Absätze nach Markdown in Java exportiert."
type: docs
weight: 450
url: /de/java/com.aspose.words/markdownemptyparagraphexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownEmptyParagraphExportMode
```

Gibt an, wie Aspose.Words leere Absätze nach Markdown exportiert.

 **Examples:** 

Zeigt, wie leere Absätze exportiert werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [EMPTY_LINE](#EMPTY-LINE) | Exportiere als leere Zeilen. |
| [MARKDOWN_HARD_LINE_BREAK](#MARKDOWN-HARD-LINE-BREAK) | Exportiere als Markdown HardLineBreak‑Zeichen '\\'. |
| [NONE](#NONE) | Exportiere keine leeren Absätze. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String markdownEmptyParagraphExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownEmptyParagraphExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownEmptyParagraphExportMode)](#toString-int) |  |
### EMPTY_LINE {#EMPTY-LINE}
```
public static int EMPTY_LINE
```


Exportiere als leere Zeilen.

 **Remarks:** 

Hinweis: Leere Zeilen haben in Markdown keine Bedeutung und gehen beim Laden verloren.

### MARKDOWN_HARD_LINE_BREAK {#MARKDOWN-HARD-LINE-BREAK}
```
public static int MARKDOWN_HARD_LINE_BREAK
```


Exportiere als Markdown HardLineBreak‑Zeichen '\\'.

### NONE {#NONE}
```
public static int NONE
```


Exportiere keine leeren Absätze.

### length {#length}
```
public static int length
```


### fromName(String markdownEmptyParagraphExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownEmptyParagraphExportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownEmptyParagraphExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownEmptyParagraphExportMode) {#getName-int}
```
public static String getName(int markdownEmptyParagraphExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markdownEmptyParagraphExportMode | int |  |

**Returns:**
java.lang.String
