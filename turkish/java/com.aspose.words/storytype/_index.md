---
title: "StoryType"
linktitle: "StoryType"
second_title: "Aspose.Words Java için"
description: "Bir Word belgesinin metni Java'da hikayeler içinde depolanır."
type: docs
weight: 634
url: /tr/java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

Bir Word belgesinin metni hikayeler içinde depolanır. [StoryType](../../com.aspose.words/storytype/) bir hikayeyi tanımlar.

 **Examples:** 

Bir düğümden tüm şekilleri nasıl kaldıracağınızı gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [COMMENTS](#COMMENTS) | Belge yorumlarını (notları) içerir, [Comment](../../com.aspose.words/comment/) tarafından temsil edilir. |
| [ENDNOTES](#ENDNOTES) | Dipnot metinlerini içerir, [Footnote](../../com.aspose.words/footnote/) tarafından temsil edilir. |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Dipnot devam bildirimi ayırıcı metnini içerir. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Dipnot devam ayırıcı metnini içerir. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Dipnot ayırıcı metnini içerir. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Çift sayfaların altbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir. |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Çift sayfaların üstbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir. |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | İlk sayfanın altbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir. |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | İlk sayfanın üstbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir. |
| [FOOTNOTES](#FOOTNOTES) | Dipnot metnini içerir, [Footnote](../../com.aspose.words/footnote/) tarafından temsil edilir. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Dipnot devam bildirimi ayırıcı metnini içerir. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Dipnot devam ayırıcı metnini içerir. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Dipnot ayırıcı metnini içerir. |
| [MAIN_TEXT](#MAIN-TEXT) | Belgenin ana metnini içerir, [Body](../../com.aspose.words/body/) tarafından temsil edilir. |
| [NONE](#NONE) | Varsayılan değer. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Ana altbilgi metnini içerir. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Ana üstbilgi metnini içerir. |
| [TEXTBOX](#TEXTBOX) | Şekil veya metin kutusu metnini içerir, [Shape](../../com.aspose.words/shape/) tarafından temsil edilir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Belge yorumlarını (notları) içerir, [Comment](../../com.aspose.words/comment/) tarafından temsil edilir.

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Dipnot metinlerini içerir, [Footnote](../../com.aspose.words/footnote/) tarafından temsil edilir.

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Dipnot devam bildirimi ayırıcı metnini içerir.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Dipnot devam ayırıcı metnini içerir.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Dipnot ayırıcı metnini içerir.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Çift sayfaların altbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir.

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Çift sayfaların üstbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir.

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


İlk sayfanın altbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir.

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


İlk sayfanın üstbilgi metnini içerir, [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir.

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Dipnot metnini içerir, [Footnote](../../com.aspose.words/footnote/) tarafından temsil edilir.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Dipnot devam bildirimi ayırıcı metnini içerir.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Dipnot devam ayırıcı metnini içerir.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Dipnot ayırıcı metnini içerir.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Belgenin ana metnini içerir, [Body](../../com.aspose.words/body/) tarafından temsil edilir.

### NONE {#NONE}
```
public static int NONE
```


Varsayılan değer. Belgede böyle bir hikaye yok.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Ana altbilgi metnini içerir. Altbilgi tek ve çift sayfalar için farklı olduğunda, tek sayfaların altbilgi metnini içerir. [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir.

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Ana üstbilgi metnini içerir. Üstbilgi tek ve çift sayfalar için farklı olduğunda, tek sayfaların üstbilgi metnini içerir. [HeaderFooter](../../com.aspose.words/headerfooter/) tarafından temsil edilir.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Şekil veya metin kutusu metnini içerir, [Shape](../../com.aspose.words/shape/) tarafından temsil edilir.

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
