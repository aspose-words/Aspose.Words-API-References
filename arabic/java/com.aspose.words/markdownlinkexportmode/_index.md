---
title: "MarkdownLinkExportMode"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تصدير الروابط إلى Markdown في Java."
type: docs
weight: 452
url: /ar/java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

يحدد كيفية تصدير الروابط إلى Markdown.

 **Examples:** 

يوضح كيفية كتابة الروابط إلى ملف .md.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertShape(ShapeType.BALLOON, 100.0, 100.0);

 // Image will be written as reference:
 // ![ref1]
 //
 // [ref1]: aw_ref.001.png
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.REFERENCE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

 // Image will be written as inline:
 // ![](../aw_inline.001.png)
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.INLINE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | اكتشاف وضع التصدير تلقائيًا لكل رابط. |
| [INLINE](#INLINE) | تصدير جميع الروابط ككتل مضمنة. |
| [REFERENCE](#REFERENCE) | تصدير جميع الروابط ككتل مرجعية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String markdownLinkExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownLinkExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownLinkExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


اكتشاف وضع التصدير تلقائيًا لكل رابط.

### INLINE {#INLINE}
```
public static int INLINE
```


تصدير جميع الروابط ككتل مضمنة.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


تصدير جميع الروابط ككتل مرجعية.

### length {#length}
```
public static int length
```


### fromName(String markdownLinkExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownLinkExportModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownLinkExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownLinkExportMode) {#getName-int}
```
public static String getName(int markdownLinkExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownLinkExportMode) {#toString-int}
```
public static String toString(int markdownLinkExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
