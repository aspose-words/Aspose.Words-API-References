---
title: "TableContentAlignment"
linktitle: "TableContentAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da Markdown formatına dışa aktarılırken tablonun içeriğinin hizalamasını belirtmeye olanak tanır."
type: docs
weight: 659
url: /tr/java/com.aspose.words/tablecontentalignment/
---

**Inheritance:**
java.lang.Object
```
public class TableContentAlignment
```

Tablonun içeriğinin Markdown formatına dışa aktarılırken kullanılacak hizalamasını belirtmeye izin verir.

 **Examples:** 

Tablolardaki içeriklerin nasıl hizalanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Hizalama, ilgili tablo sütunundaki ilk paragraftan alınacaktır. |
| [CENTER](#CENTER) | Tabloların içeriği Ortaya hizalanacaktır. |
| [LEFT](#LEFT) | Tabloların içeriği Sola hizalanacaktır. |
| [RIGHT](#RIGHT) | Tabloların içeriği Sağa hizalanacaktır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String tableContentAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableContentAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableContentAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Hizalama, ilgili tablo sütunundaki ilk paragraftan alınacaktır.

### CENTER {#CENTER}
```
public static int CENTER
```


Tabloların içeriği Ortaya hizalanacaktır.

### LEFT {#LEFT}
```
public static int LEFT
```


Tabloların içeriği Sola hizalanacaktır.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Tabloların içeriği Sağa hizalanacaktır.

### length {#length}
```
public static int length
```


### fromName(String tableContentAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableContentAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableContentAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableContentAlignment) {#getName-int}
```
public static String getName(int tableContentAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableContentAlignment | int |  |

**Returns:**
java.lang.String
