---
title: "TableContentAlignment"
linktitle: "TableContentAlignment"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد محاذاة محتوى الجدول لاستخدامها عند التصدير إلى تنسيق Markdown في Java."
type: docs
weight: 659
url: /ar/java/com.aspose.words/tablecontentalignment/
---

**Inheritance:**
java.lang.Object
```
public class TableContentAlignment
```

يسمح بتحديد محاذاة محتوى الجدول لاستخدامها عند التصدير إلى تنسيق Markdown.

 **Examples:** 

يوضح كيفية محاذاة المحتويات في الجداول.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions(); { saveOptions.setTableContentAlignment(tableContentAlignment); }

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

 Document doc = new Document(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 switch (tableContentAlignment)
 {
     case TableContentAlignment.AUTO:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.LEFT:
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.CENTER:
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.RIGHT:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | سيتم أخذ المحاذاة من الفقرة الأولى في العمود المقابل للجدول. |
| [CENTER](#CENTER) | سيتم محاذاة محتوى الجداول إلى الوسط. |
| [LEFT](#LEFT) | سيتم محاذاة محتوى الجداول إلى اليسار. |
| [RIGHT](#RIGHT) | سيتم محاذاة محتوى الجداول إلى اليمين. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String tableContentAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableContentAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableContentAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


سيتم أخذ المحاذاة من الفقرة الأولى في العمود المقابل للجدول.

### CENTER {#CENTER}
```
public static int CENTER
```


سيتم محاذاة محتوى الجداول إلى الوسط.

### LEFT {#LEFT}
```
public static int LEFT
```


سيتم محاذاة محتوى الجداول إلى اليسار.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


سيتم محاذاة محتوى الجداول إلى اليمين.

### length {#length}
```
public static int length
```


### fromName(String tableContentAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableContentAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableContentAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableContentAlignment) {#getName-int}
```
public static String getName(int tableContentAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableContentAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableContentAlignment) {#toString-int}
```
public static String toString(int tableContentAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableContentAlignment | int |  |

**Returns:**
java.lang.String
