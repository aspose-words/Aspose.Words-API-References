---
title: StoryType
linktitle: StoryType
second_title: Aspose.Words for Java
description: Text of a Word document is stored in stories in Java.
type: docs
weight: 577
url: /java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

Text of a Word document is stored in stories. [StoryType](../../com.aspose.words/storytype/) identifies a story.

 **Examples:** 

Shows how to remove all shapes from a node.

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
## Fields

| Field | Description |
| --- | --- |
| [COMMENTS](#COMMENTS) | Contains document comments (annotations), represented by [Comment](../../com.aspose.words/comment/). |
| [ENDNOTES](#ENDNOTES) | Contains endnotes text, represented by [Footnote](../../com.aspose.words/footnote/). |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Contains the text of the endnote continuation notice separator. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Contains the text of the endnote continuation separator. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Contains the text of the endnote separator. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Contains text of the even pages footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Contains text of the even pages header, represented by [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | Contains text of the first page footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | Contains text of the first page header, represented by [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FOOTNOTES](#FOOTNOTES) | Contains footnote text, represented by [Footnote](../../com.aspose.words/footnote/). |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Contains the text of the footnote continuation notice separator. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Contains the text of the footnote continuation separator. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Contains the text of the footnote separator. |
| [MAIN_TEXT](#MAIN-TEXT) | Contains the main text of the document, represented by [Body](../../com.aspose.words/body/). |
| [NONE](#NONE) | Default value. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Contains text of the primary footer. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Contains text of the primary header. |
| [TEXTBOX](#TEXTBOX) | Contains shape or textbox text, represented by [Shape](../../com.aspose.words/shape/). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Contains document comments (annotations), represented by [Comment](../../com.aspose.words/comment/).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Contains endnotes text, represented by [Footnote](../../com.aspose.words/footnote/).

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Contains the text of the endnote continuation notice separator.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Contains the text of the endnote continuation separator.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Contains the text of the endnote separator.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Contains text of the even pages footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter/).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Contains text of the even pages header, represented by [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


Contains text of the first page footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


Contains text of the first page header, represented by [HeaderFooter](../../com.aspose.words/headerfooter/).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Contains footnote text, represented by [Footnote](../../com.aspose.words/footnote/).

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Contains the text of the footnote continuation notice separator.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Contains the text of the footnote continuation separator.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Contains the text of the footnote separator.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Contains the main text of the document, represented by [Body](../../com.aspose.words/body/).

### NONE {#NONE}
```
public static int NONE
```


Default value. There is no such story in the document.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Contains text of the primary footer. When footer is different for odd and even pages, contains text of the odd pages footer. Represented by [HeaderFooter](../../com.aspose.words/headerfooter/).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Contains text of the primary header. When header is different for odd and even pages, contains text of the odd pages header. Represented by [HeaderFooter](../../com.aspose.words/headerfooter/).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Contains shape or textbox text, represented by [Shape](../../com.aspose.words/shape/).

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
