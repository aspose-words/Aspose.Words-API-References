---
title: "MarkdownListExportMode"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تصدير القوائم إلى Markdown في Java."
type: docs
weight: 453
url: /ar/java/com.aspose.words/markdownlistexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownListExportMode
```

يحدد كيفية تصدير القوائم إلى Markdown.

 **Examples:** 

يوضح كيفية كتابة عناصر القائمة إلى مستند markdown.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [MARKDOWN_SYNTAX](#MARKDOWN-SYNTAX) | تصدير عناصر القائمة المتوافقة مع صيغة Markdown. |
| [PLAIN_TEXT](#PLAIN-TEXT) | تصدير عناصر القائمة كنص عادي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String markdownListExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownListExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownListExportMode)](#toString-int) |  |
### MARKDOWN_SYNTAX {#MARKDOWN-SYNTAX}
```
public static int MARKDOWN_SYNTAX
```


تصدير عناصر القائمة المتوافقة مع صيغة Markdown.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


تصدير عناصر القائمة كنص عادي.

### length {#length}
```
public static int length
```


### fromName(String markdownListExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownListExportModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownListExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownListExportMode) {#getName-int}
```
public static String getName(int markdownListExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String
