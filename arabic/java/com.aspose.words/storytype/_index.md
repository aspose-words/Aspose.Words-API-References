---
title: "StoryType"
linktitle: "StoryType"
second_title: "Aspose.Words لـ Java"
description: "نص مستند Word يُخزن في القصص في Java."
type: docs
weight: 634
url: /ar/java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

نص مستند Word يُخزن في القصص. [StoryType](../../com.aspose.words/storytype/) يحدد القصة.

 **Examples:** 

يوضح كيفية إزالة جميع الأشكال من عقدة.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [COMMENTS](#COMMENTS) | يحتوي على تعليقات المستند (التعليقات التوضيحية)، ممثلة بـ [Comment](../../com.aspose.words/comment/). |
| [ENDNOTES](#ENDNOTES) | يحتوي على نص الحواشي السفلية، ممثلًا بـ [Footnote](../../com.aspose.words/footnote/). |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | يحتوي على نص فاصل إشعار استمرار الحاشية السفلية. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | يحتوي على نص فاصل استمرار الحاشية السفلية. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | يحتوي على نص فاصل الحاشية السفلية. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | يحتوي على نص تذييل الصفحات الزوجية، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | يحتوي على نص رأس الصفحات الزوجية، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | يحتوي على نص تذييل الصفحة الأولى، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | يحتوي على نص رأس الصفحة الأولى، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FOOTNOTES](#FOOTNOTES) | يحتوي على نص الحاشية السفلية، ممثلًا بـ [Footnote](../../com.aspose.words/footnote/). |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | يحتوي على نص فاصل إشعار استمرار الحاشية السفلية. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | يحتوي على نص فاصل استمرار الحاشية السفلية. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | يحتوي على نص فاصل الحاشية السفلية. |
| [MAIN_TEXT](#MAIN-TEXT) | يحتوي على النص الرئيسي للمستند، ممثلًا بـ [Body](../../com.aspose.words/body/). |
| [NONE](#NONE) | القيمة الافتراضية. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | يحتوي على نص التذييل الأساسي. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | يحتوي على نص الرأس الأساسي. |
| [TEXTBOX](#TEXTBOX) | يحتوي على نص الشكل أو مربع النص، ممثلًا بـ [Shape](../../com.aspose.words/shape/). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


يحتوي على تعليقات المستند (التعليقات التوضيحية)، ممثلة بـ [Comment](../../com.aspose.words/comment/).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


يحتوي على نص الحواشي السفلية، ممثلًا بـ [Footnote](../../com.aspose.words/footnote/).

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


يحتوي على نص فاصل إشعار استمرار الحاشية السفلية.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


يحتوي على نص فاصل استمرار الحاشية السفلية.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


يحتوي على نص فاصل الحاشية السفلية.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


يحتوي على نص تذييل الصفحات الزوجية، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


يحتوي على نص رأس الصفحات الزوجية، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


يحتوي على نص تذييل الصفحة الأولى، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


يحتوي على نص رأس الصفحة الأولى، ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


يحتوي على نص الحاشية السفلية، ممثلًا بـ [Footnote](../../com.aspose.words/footnote/).

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


يحتوي على نص فاصل إشعار استمرار الحاشية السفلية.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


يحتوي على نص فاصل استمرار الحاشية السفلية.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


يحتوي على نص فاصل الحاشية السفلية.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


يحتوي على النص الرئيسي للمستند، ممثلًا بـ [Body](../../com.aspose.words/body/).

### NONE {#NONE}
```
public static int NONE
```


القيمة الافتراضية. لا توجد قصة من هذا النوع في المستند.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


يحتوي على نص التذييل الأساسي. عندما يكون التذييل مختلفًا للصفحات الفردية والزوجية، يحتوي على نص تذييل الصفحات الفردية. ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


يحتوي على نص الرأس الأساسي. عندما يكون الرأس مختلفًا للصفحات الفردية والزوجية، يحتوي على نص رأس الصفحات الفردية. ممثلًا بـ [HeaderFooter](../../com.aspose.words/headerfooter/).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


يحتوي على نص الشكل أو مربع النص، ممثلًا بـ [Shape](../../com.aspose.words/shape/).

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
