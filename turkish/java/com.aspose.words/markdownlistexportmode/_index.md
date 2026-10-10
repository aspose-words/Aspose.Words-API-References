---
title: "MarkdownListExportMode"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words Java için"
description: "Java'da listelerin Markdown'a nasıl dışa aktarılacağını belirtir."
type: docs
weight: 453
url: /tr/java/com.aspose.words/markdownlistexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownListExportMode
```

Listelerin Markdown'a nasıl dışa aktarıldığını belirtir.

 **Examples:** 

Liste öğelerinin markdown belgesine nasıl yazılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [MARKDOWN_SYNTAX](#MARKDOWN-SYNTAX) | Markdown sözdizimiyle uyumlu liste öğelerini dışa aktar. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Liste öğelerini düz metin olarak dışa aktar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String markdownListExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownListExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownListExportMode)](#toString-int) |  |
### MARKDOWN_SYNTAX {#MARKDOWN-SYNTAX}
```
public static int MARKDOWN_SYNTAX
```


Markdown sözdizimiyle uyumlu liste öğelerini dışa aktar.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Liste öğelerini düz metin olarak dışa aktar.

### length {#length}
```
public static int length
```


### fromName(String markdownListExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownListExportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownListExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownListExportMode) {#getName-int}
```
public static String getName(int markdownListExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String
