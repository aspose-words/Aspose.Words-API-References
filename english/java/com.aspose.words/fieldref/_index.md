---
title: FieldRef
second_title: Aspose.Words for Java API Reference
description: Implements the REF field.
type: docs
weight: 235
url: /java/com.aspose.words/fieldref/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldRef extends Field
```

Implements the REF field.

To learn more, visit the **Working with Fields** documentation article.

Inserts the text or graphics represented by the specified bookmark.
## Methods

| Method | Description |
| --- | --- |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getMergeFieldName()](#getMergeFieldName--) |  |
| [canWorkAsMergeField()](#canWorkAsMergeField--) |  |
| [isMergeValueRequired()](#isMergeValueRequired--) |  |
| [getBookmarkName()](#getBookmarkName--) | Gets the referenced bookmark's name. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Sets the referenced bookmark's name. |
| [getNumberSeparator()](#getNumberSeparator--) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [setNumberSeparator(String value)](#setNumberSeparator-java.lang.String-) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [getIncludeNoteOrComment()](#getIncludeNoteOrComment--) | Gets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text. |
| [setIncludeNoteOrComment(boolean value)](#setIncludeNoteOrComment-boolean-) | Sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text. |
| [getInsertHyperlink()](#getInsertHyperlink--) | Gets whether to create a hyperlink to the bookmarked paragraph. |
| [setInsertHyperlink(boolean value)](#setInsertHyperlink-boolean-) | Sets whether to create a hyperlink to the bookmarked paragraph. |
| [getInsertParagraphNumber()](#getInsertParagraphNumber--) | Gets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [setInsertParagraphNumber(boolean value)](#setInsertParagraphNumber-boolean-) | Sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [getInsertRelativePosition()](#getInsertRelativePosition--) | Gets whether to insert the relative position of the referenced paragraph. |
| [setInsertRelativePosition(boolean value)](#setInsertRelativePosition-boolean-) | Sets whether to insert the relative position of the referenced paragraph. |
| [getInsertParagraphNumberInRelativeContext()](#getInsertParagraphNumberInRelativeContext--) | Gets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [setInsertParagraphNumberInRelativeContext(boolean value)](#setInsertParagraphNumberInRelativeContext-boolean-) | Sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [getSuppressNonDelimiters()](#getSuppressNonDelimiters--) | Gets whether to suppress non-delimiter characters. |
| [setSuppressNonDelimiters(boolean value)](#setSuppressNonDelimiters-boolean-) | Sets whether to suppress non-delimiter characters. |
| [getInsertParagraphNumberInFullContext()](#getInsertParagraphNumberInFullContext--) | Gets whether to insert the paragraph number of the referenced paragraph in full context. |
| [setInsertParagraphNumberInFullContext(boolean value)](#setInsertParagraphNumberInFullContext-boolean-) | Sets whether to insert the paragraph number of the referenced paragraph in full context. |
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getMergeFieldName() {#getMergeFieldName--}
```
public String getMergeFieldName()
```




**Returns:**
java.lang.String
### canWorkAsMergeField() {#canWorkAsMergeField--}
```
public boolean canWorkAsMergeField()
```




**Returns:**
boolean
### isMergeValueRequired() {#isMergeValueRequired--}
```
public boolean isMergeValueRequired()
```




**Returns:**
boolean
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


Gets the referenced bookmark's name.

**Returns:**
java.lang.String - The referenced bookmark's name.
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


Sets the referenced bookmark's name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The referenced bookmark's name. |

### getNumberSeparator() {#getNumberSeparator--}
```
public String getNumberSeparator()
```


Gets the character sequence that is used to separate sequence numbers and page numbers.

**Returns:**
java.lang.String - The character sequence that is used to separate sequence numbers and page numbers.
### setNumberSeparator(String value) {#setNumberSeparator-java.lang.String-}
```
public void setNumberSeparator(String value)
```


Sets the character sequence that is used to separate sequence numbers and page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate sequence numbers and page numbers. |

### getIncludeNoteOrComment() {#getIncludeNoteOrComment--}
```
public boolean getIncludeNoteOrComment()
```


Gets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text.

**Returns:**
boolean - Whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text.
### setIncludeNoteOrComment(boolean value) {#setIncludeNoteOrComment-boolean-}
```
public void setIncludeNoteOrComment(boolean value)
```


Sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text. |

### getInsertHyperlink() {#getInsertHyperlink--}
```
public boolean getInsertHyperlink()
```


Gets whether to create a hyperlink to the bookmarked paragraph.

**Returns:**
boolean - Whether to create a hyperlink to the bookmarked paragraph.
### setInsertHyperlink(boolean value) {#setInsertHyperlink-boolean-}
```
public void setInsertHyperlink(boolean value)
```


Sets whether to create a hyperlink to the bookmarked paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to create a hyperlink to the bookmarked paragraph. |

### getInsertParagraphNumber() {#getInsertParagraphNumber--}
```
public boolean getInsertParagraphNumber()
```


Gets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document.

**Returns:**
boolean - Whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document.
### setInsertParagraphNumber(boolean value) {#setInsertParagraphNumber-boolean-}
```
public void setInsertParagraphNumber(boolean value)
```


Sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |

### getInsertRelativePosition() {#getInsertRelativePosition--}
```
public boolean getInsertRelativePosition()
```


Gets whether to insert the relative position of the referenced paragraph.

**Returns:**
boolean - Whether to insert the relative position of the referenced paragraph.
### setInsertRelativePosition(boolean value) {#setInsertRelativePosition-boolean-}
```
public void setInsertRelativePosition(boolean value)
```


Sets whether to insert the relative position of the referenced paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to insert the relative position of the referenced paragraph. |

### getInsertParagraphNumberInRelativeContext() {#getInsertParagraphNumberInRelativeContext--}
```
public boolean getInsertParagraphNumberInRelativeContext()
```


Gets whether to insert the paragraph number of the referenced paragraph in relative context.

**Returns:**
boolean - Whether to insert the paragraph number of the referenced paragraph in relative context.
### setInsertParagraphNumberInRelativeContext(boolean value) {#setInsertParagraphNumberInRelativeContext-boolean-}
```
public void setInsertParagraphNumberInRelativeContext(boolean value)
```


Sets whether to insert the paragraph number of the referenced paragraph in relative context.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to insert the paragraph number of the referenced paragraph in relative context. |

### getSuppressNonDelimiters() {#getSuppressNonDelimiters--}
```
public boolean getSuppressNonDelimiters()
```


Gets whether to suppress non-delimiter characters.

**Returns:**
boolean - Whether to suppress non-delimiter characters.
### setSuppressNonDelimiters(boolean value) {#setSuppressNonDelimiters-boolean-}
```
public void setSuppressNonDelimiters(boolean value)
```


Sets whether to suppress non-delimiter characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to suppress non-delimiter characters. |

### getInsertParagraphNumberInFullContext() {#getInsertParagraphNumberInFullContext--}
```
public boolean getInsertParagraphNumberInFullContext()
```


Gets whether to insert the paragraph number of the referenced paragraph in full context.

**Returns:**
boolean - Whether to insert the paragraph number of the referenced paragraph in full context.
### setInsertParagraphNumberInFullContext(boolean value) {#setInsertParagraphNumberInFullContext-boolean-}
```
public void setInsertParagraphNumberInFullContext(boolean value)
```


Sets whether to insert the paragraph number of the referenced paragraph in full context.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to insert the paragraph number of the referenced paragraph in full context. |

