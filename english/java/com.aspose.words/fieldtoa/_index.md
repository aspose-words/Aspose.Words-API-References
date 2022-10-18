---
title: FieldToa
second_title: Aspose.Words for Java API Reference
description: Implements the TOA field.
type: docs
weight: 254
url: /java/com.aspose.words/fieldtoa/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldToa extends Field
```

Implements the TOA field.

To learn more, visit the **Working with Fields** documentation article.

Builds a table of authorities (that is, a list of the references in a legal document, such as references to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the entries specified by TA fields.
## Methods

| Method | Description |
| --- | --- |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getBookmarkName()](#getBookmarkName--) | Gets the name of the bookmark that marks the portion of the document used to build the table. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Sets the name of the bookmark that marks the portion of the document used to build the table. |
| [getEntryCategory()](#getEntryCategory--) | Gets the integral category for entries included in the table. |
| [setEntryCategory(String value)](#setEntryCategory-java.lang.String-) | Sets the integral category for entries included in the table. |
| [getSequenceSeparator()](#getSequenceSeparator--) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [getEntrySeparator()](#getEntrySeparator--) | Gets the character sequence that is used to separate a table of authorities entry and its page number. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String-) | Sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [getRemoveEntryFormatting()](#getRemoveEntryFormatting--) | Gets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [setRemoveEntryFormatting(boolean value)](#setRemoveEntryFormatting-boolean-) | Sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [getPageRangeSeparator()](#getPageRangeSeparator--) | Gets the character sequence that is used to separate the start and end of a page range. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String-) | Sets the character sequence that is used to separate the start and end of a page range. |
| [getUseHeading()](#getUseHeading--) | Gets whether to include the category heading for the entries in a table of authorities. |
| [setUseHeading(boolean value)](#setUseHeading-boolean-) | Sets whether to include the category heading for the entries in a table of authorities. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator--) | Gets the character sequence that is used to separate two page numbers in a page number list. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String-) | Sets the character sequence that is used to separate two page numbers in a page number list. |
| [getUsePassim()](#getUsePassim--) | Gets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |
| [setUsePassim(boolean value)](#setUsePassim-boolean-) | Sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |
| [getSequenceName()](#getSequenceName--) | Gets the name of a sequence whose number is included with the page number. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String-) | Sets the name of a sequence whose number is included with the page number. |
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
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


Gets the name of the bookmark that marks the portion of the document used to build the table.

**Returns:**
java.lang.String - The name of the bookmark that marks the portion of the document used to build the table.
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


Sets the name of the bookmark that marks the portion of the document used to build the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks the portion of the document used to build the table. |

### getEntryCategory() {#getEntryCategory--}
```
public String getEntryCategory()
```


Gets the integral category for entries included in the table.

**Returns:**
java.lang.String - The integral category for entries included in the table.
### setEntryCategory(String value) {#setEntryCategory-java.lang.String-}
```
public void setEntryCategory(String value)
```


Sets the integral category for entries included in the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The integral category for entries included in the table. |

### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


Gets the character sequence that is used to separate sequence numbers and page numbers.

**Returns:**
java.lang.String - The character sequence that is used to separate sequence numbers and page numbers.
### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


Sets the character sequence that is used to separate sequence numbers and page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate sequence numbers and page numbers. |

### getEntrySeparator() {#getEntrySeparator--}
```
public String getEntrySeparator()
```


Gets the character sequence that is used to separate a table of authorities entry and its page number.

**Returns:**
java.lang.String - The character sequence that is used to separate a table of authorities entry and its page number.
### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String-}
```
public void setEntrySeparator(String value)
```


Sets the character sequence that is used to separate a table of authorities entry and its page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate a table of authorities entry and its page number. |

### getRemoveEntryFormatting() {#getRemoveEntryFormatting--}
```
public boolean getRemoveEntryFormatting()
```


Gets whether to remove the formatting of the entry text in the document from the entry in the table of authorities.

**Returns:**
boolean - Whether to remove the formatting of the entry text in the document from the entry in the table of authorities.
### setRemoveEntryFormatting(boolean value) {#setRemoveEntryFormatting-boolean-}
```
public void setRemoveEntryFormatting(boolean value)
```


Sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |

### getPageRangeSeparator() {#getPageRangeSeparator--}
```
public String getPageRangeSeparator()
```


Gets the character sequence that is used to separate the start and end of a page range.

**Returns:**
java.lang.String - The character sequence that is used to separate the start and end of a page range.
### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String-}
```
public void setPageRangeSeparator(String value)
```


Sets the character sequence that is used to separate the start and end of a page range.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate the start and end of a page range. |

### getUseHeading() {#getUseHeading--}
```
public boolean getUseHeading()
```


Gets whether to include the category heading for the entries in a table of authorities.

**Returns:**
boolean - Whether to include the category heading for the entries in a table of authorities.
### setUseHeading(boolean value) {#setUseHeading-boolean-}
```
public void setUseHeading(boolean value)
```


Sets whether to include the category heading for the entries in a table of authorities.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to include the category heading for the entries in a table of authorities. |

### getPageNumberListSeparator() {#getPageNumberListSeparator--}
```
public String getPageNumberListSeparator()
```


Gets the character sequence that is used to separate two page numbers in a page number list.

**Returns:**
java.lang.String - The character sequence that is used to separate two page numbers in a page number list.
### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String-}
```
public void setPageNumberListSeparator(String value)
```


Sets the character sequence that is used to separate two page numbers in a page number list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate two page numbers in a page number list. |

### getUsePassim() {#getUsePassim--}
```
public boolean getUsePassim()
```


Gets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.

**Returns:**
boolean - Whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.
### setUsePassim(boolean value) {#setUsePassim-boolean-}
```
public void setUsePassim(boolean value)
```


Sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

### getSequenceName() {#getSequenceName--}
```
public String getSequenceName()
```


Gets the name of a sequence whose number is included with the page number.

**Returns:**
java.lang.String - The name of a sequence whose number is included with the page number.
### setSequenceName(String value) {#setSequenceName-java.lang.String-}
```
public void setSequenceName(String value)
```


Sets the name of a sequence whose number is included with the page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of a sequence whose number is included with the page number. |

