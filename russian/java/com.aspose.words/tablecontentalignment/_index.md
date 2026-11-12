---
title: "TableContentAlignment"
linktitle: "TableContentAlignment"
second_title: "Aspose.Words для Java"
description: "Позволяет указать выравнивание содержимого таблицы, которое будет использоваться при экспорте в формат Markdown в Java."
type: docs
weight: 659
url: /ru/java/com.aspose.words/tablecontentalignment/
---

**Inheritance:**
java.lang.Object
```
public class TableContentAlignment
```

Позволяет указать выравнивание содержимого таблицы, используемое при экспорте в формат Markdown.

 **Examples:** 

Показывает, как выравнивать содержимое в таблицах.

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
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Выравнивание будет взято из первого абзаца в соответствующей колонке таблицы. |
| [CENTER](#CENTER) | Содержимое таблиц будет выровнено по центру. |
| [LEFT](#LEFT) | Содержимое таблиц будет выровнено влево. |
| [RIGHT](#RIGHT) | Содержимое таблиц будет выровнено вправо. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String tableContentAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableContentAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableContentAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Выравнивание будет взято из первого абзаца в соответствующей колонке таблицы.

### CENTER {#CENTER}
```
public static int CENTER
```


Содержимое таблиц будет выровнено по центру.

### LEFT {#LEFT}
```
public static int LEFT
```


Содержимое таблиц будет выровнено влево.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Содержимое таблиц будет выровнено вправо.

### length {#length}
```
public static int length
```


### fromName(String tableContentAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableContentAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableContentAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableContentAlignment) {#getName-int}
```
public static String getName(int tableContentAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableContentAlignment | int |  |

**Returns:**
java.lang.String
