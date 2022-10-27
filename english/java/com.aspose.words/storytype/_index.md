---
title: StoryType
second_title: Aspose.Words for Java API Reference
description: Text of a Word document is stored in stories.
type: docs
weight: 529
url: /java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

Text of a Word document is stored in stories. **StoryType** identifies a story.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Default value. |
| [MAIN_TEXT](#MAIN-TEXT) | Contains the main text of the document, represented by [Body](../../com.aspose.words/body). |
| [FOOTNOTES](#FOOTNOTES) | Contains footnote text, represented by [Footnote](../../com.aspose.words/footnote). |
| [ENDNOTES](#ENDNOTES) | Contains endnotes text, represented by [Footnote](../../com.aspose.words/footnote). |
| [COMMENTS](#COMMENTS) | Contains document comments (annotations), represented by [Comment](../../com.aspose.words/comment). |
| [TEXTBOX](#TEXTBOX) | Contains shape or textbox text, represented by [Shape](../../com.aspose.words/shape). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Contains text of the even pages header, represented by [HeaderFooter](../../com.aspose.words/headerfooter). |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Contains text of the primary header. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Contains text of the even pages footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter). |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Contains text of the primary footer. |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | Contains text of the first page header, represented by [HeaderFooter](../../com.aspose.words/headerfooter). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | Contains text of the first page footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter). |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Contains the text of the footnote separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Contains the text of the footnote continuation separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Contains the text of the footnote continuation notice separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Contains the text of the endnote separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Contains the text of the endnote continuation separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**. |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Contains the text of the endnote continuation notice separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int storyType)](#getName-int-) |  |
| [toString(int storyType)](#toString-int-) |  |
| [fromName(String storyTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


Default value. There is no such story in the document.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Contains the main text of the document, represented by [Body](../../com.aspose.words/body).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Contains footnote text, represented by [Footnote](../../com.aspose.words/footnote).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Contains endnotes text, represented by [Footnote](../../com.aspose.words/footnote).

### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Contains document comments (annotations), represented by [Comment](../../com.aspose.words/comment).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Contains shape or textbox text, represented by [Shape](../../com.aspose.words/shape).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Contains text of the even pages header, represented by [HeaderFooter](../../com.aspose.words/headerfooter).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Contains text of the primary header. When header is different for odd and even pages, contains text of the odd pages header. Represented by [HeaderFooter](../../com.aspose.words/headerfooter).

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Contains text of the even pages footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter).

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Contains text of the primary footer. When footer is different for odd and even pages, contains text of the odd pages footer. Represented by [HeaderFooter](../../com.aspose.words/headerfooter).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


Contains text of the first page header, represented by [HeaderFooter](../../com.aspose.words/headerfooter).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


Contains text of the first page footer, represented by [HeaderFooter](../../com.aspose.words/headerfooter).

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Contains the text of the footnote separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Contains the text of the footnote continuation separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Contains the text of the footnote continuation notice separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Contains the text of the endnote separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Contains the text of the endnote continuation separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**.

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Contains the text of the endnote continuation notice separator, represented by **T:Aspose.Words.Notes.FootnoteSeparator**.

### length {#length}
```
public static int length
```


### getName(int storyType) {#getName-int-}
```
public static String getName(int storyType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
### toString(int storyType) {#toString-int-}
```
public static String toString(int storyType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
### fromName(String storyTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
