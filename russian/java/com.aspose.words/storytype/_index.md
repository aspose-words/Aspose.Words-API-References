---
title: "StoryType"
linktitle: "StoryType"
second_title: "Aspose.Words для Java"
description: "Текст документа Word хранится в историях в Java."
type: docs
weight: 634
url: /ru/java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

Текст документа Word хранится в историях. [StoryType](../../com.aspose.words/storytype/) идентифицирует историю.

 **Examples:** 

Показывает, как удалить все фигуры из узла.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a DocumentBuilder to insert a shape. This is an inline shape,
 // which has a parent Paragraph, which is a child node of the first section's Body.
 builder.insertShape(ShapeType.CUBE, 100.0, 100.0);

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 1);

 // We can delete all shapes from the child paragraphs of this Body.
 Assert.assertEquals(doc.getFirstSection().getBody().getStoryType(), StoryType.MAIN_TEXT);
 doc.getFirstSection().getBody().deleteShapes();

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 0);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [COMMENTS](#COMMENTS) | Содержит комментарии документа (аннотации), представленные объектом [Comment](../../com.aspose.words/comment/). |
| [ENDNOTES](#ENDNOTES) | Содержит текст сносок, представленный объектом [Footnote](../../com.aspose.words/footnote/). |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Содержит текст разделителя уведомления о продолжении сноски. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Содержит текст разделителя продолжения сноски. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Содержит текст разделителя сносок. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Содержит текст нижнего колонтитула чётных страниц, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Содержит текст верхнего колонтитула чётных страниц, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | Содержит текст нижнего колонтитула первой страницы, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | Содержит текст верхнего колонтитула первой страницы, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FOOTNOTES](#FOOTNOTES) | Содержит текст сноски, представленного объектом [Footnote](../../com.aspose.words/footnote/). |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Содержит текст разделителя уведомления о продолжении сноски. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Содержит текст разделителя продолжения сноски. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Содержит текст разделителя сноски. |
| [MAIN_TEXT](#MAIN-TEXT) | Содержит основной текст документа, представленного объектом [Body](../../com.aspose.words/body/). |
| [NONE](#NONE) | Значение по умолчанию. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Содержит текст основного нижнего колонтитула. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Содержит текст основного верхнего колонтитула. |
| [TEXTBOX](#TEXTBOX) | Содержит текст фигуры или текстового поля, представленного объектом [Shape](../../com.aspose.words/shape/). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Содержит комментарии документа (аннотации), представленные объектом [Comment](../../com.aspose.words/comment/).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Содержит текст сносок, представленный объектом [Footnote](../../com.aspose.words/footnote/).

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Содержит текст разделителя уведомления о продолжении сноски.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Содержит текст разделителя продолжения сноски.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Содержит текст разделителя сносок.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Содержит текст нижнего колонтитула чётных страниц, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Содержит текст верхнего колонтитула чётных страниц, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


Содержит текст нижнего колонтитула первой страницы, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


Содержит текст верхнего колонтитула первой страницы, представленного объектом [HeaderFooter](../../com.aspose.words/headerfooter/).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Содержит текст сноски, представленного объектом [Footnote](../../com.aspose.words/footnote/).

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Содержит текст разделителя уведомления о продолжении сноски.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Содержит текст разделителя продолжения сноски.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Содержит текст разделителя сноски.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Содержит основной текст документа, представленного объектом [Body](../../com.aspose.words/body/).

### NONE {#NONE}
```
public static int NONE
```


Значение по умолчанию. В документе нет такой истории.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Содержит текст основного нижнего колонтитула. Когда нижний колонтитул отличается для нечётных и чётных страниц, содержит текст нижнего колонтитула нечётных страниц. Представлен объектом [HeaderFooter](../../com.aspose.words/headerfooter/).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Содержит текст основного верхнего колонтитула. Когда верхний колонтитул отличается для нечётных и чётных страниц, содержит текст верхнего колонтитула нечётных страниц. Представлен объектом [HeaderFooter](../../com.aspose.words/headerfooter/).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Содержит текст фигуры или текстового поля, представленного объектом [Shape](../../com.aspose.words/shape/).

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int storyType) {#toString-int}
```
public static String toString(int storyType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
