---
title: "MarkdownEmptyParagraphExportMode"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Aspose.Words Java için"
description: "Aspose.Words'in Java'da boş paragrafları Markdown'a nasıl dışa aktardığını belirtir."
type: docs
weight: 450
url: /tr/java/com.aspose.words/markdownemptyparagraphexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownEmptyParagraphExportMode
```

Aspose.Words'un boş paragrafları Markdown'a nasıl dışa aktardığını belirtir.

 **Examples:** 

Boş paragrafların nasıl dışa aktarılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [EMPTY_LINE](#EMPTY-LINE) | Boş satır olarak dışa aktar. |
| [MARKDOWN_HARD_LINE_BREAK](#MARKDOWN-HARD-LINE-BREAK) | Markdown HardLineBreak karakteri '\\' olarak dışa aktar. |
| [NONE](#NONE) | Boş paragrafları dışa aktarma. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String markdownEmptyParagraphExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownEmptyParagraphExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownEmptyParagraphExportMode)](#toString-int) |  |
### EMPTY_LINE {#EMPTY-LINE}
```
public static int EMPTY_LINE
```


Boş satır olarak dışa aktar.

 **Remarks:** 

Not: Boş satırlar Markdown'da anlamlı değildir ve yükleme sırasında kaybolur.

### MARKDOWN_HARD_LINE_BREAK {#MARKDOWN-HARD-LINE-BREAK}
```
public static int MARKDOWN_HARD_LINE_BREAK
```


Markdown HardLineBreak karakteri '\\' olarak dışa aktar.

### NONE {#NONE}
```
public static int NONE
```


Boş paragrafları dışa aktarma.

### length {#length}
```
public static int length
```


### fromName(String markdownEmptyParagraphExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownEmptyParagraphExportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownEmptyParagraphExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownEmptyParagraphExportMode) {#getName-int}
```
public static String getName(int markdownEmptyParagraphExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownEmptyParagraphExportMode | int |  |

**Returns:**
java.lang.String
