---
title: FieldIndex
second_title: Aspose.Words for Java API Reference
description: Implements the INDEX field.
type: docs
weight: 206
url: /java/com.aspose.words/fieldindex/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldIndex extends Field
```

Implements the INDEX field.

To learn more, visit the **Working with Fields** documentation article.

Builds an index using the index entries specified by XE fields, and inserts that index at this place in the document.
## Methods

| Method | Description |
| --- | --- |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getBookmarkName()](#getBookmarkName--) | Gets the name of the bookmark that marks the portion of the document used to build the index. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Sets the name of the bookmark that marks the portion of the document used to build the index. |
| [getNumberOfColumns()](#getNumberOfColumns--) | Gets the number of columns per page used when building the index. |
| [setNumberOfColumns(String value)](#setNumberOfColumns-java.lang.String-) | Sets the number of columns per page used when building the index. |
| [getSequenceSeparator()](#getSequenceSeparator--) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [getPageNumberSeparator()](#getPageNumberSeparator--) | Gets the character sequence that is used to separate an index entry and its page number. |
| [setPageNumberSeparator(String value)](#setPageNumberSeparator-java.lang.String-) | Sets the character sequence that is used to separate an index entry and its page number. |
| [hasPageNumberSeparator()](#hasPageNumberSeparator--) | Gets a value indicating whether a page number separator is overridden through the field's code. |
| [getEntryType()](#getEntryType--) | Gets an index entry type used to build the index. |
| [setEntryType(String value)](#setEntryType-java.lang.String-) | Sets an index entry type used to build the index. |
| [getPageRangeSeparator()](#getPageRangeSeparator--) | Gets the character sequence that is used to separate the start and end of a page range. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String-) | Sets the character sequence that is used to separate the start and end of a page range. |
| [getHeading()](#getHeading--) | Gets a heading that appears at the start of each set of entries for any given letter. |
| [setHeading(String value)](#setHeading-java.lang.String-) | Sets a heading that appears at the start of each set of entries for any given letter. |
| [getCrossReferenceSeparator()](#getCrossReferenceSeparator--) | Gets the character sequence that is used to separate cross references and other entries. |
| [setCrossReferenceSeparator(String value)](#setCrossReferenceSeparator-java.lang.String-) | Sets the character sequence that is used to separate cross references and other entries. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator--) | Gets the character sequence that is used to separate two page numbers in a page number list. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String-) | Sets the character sequence that is used to separate two page numbers in a page number list. |
| [getLetterRange()](#getLetterRange--) | Gets a range of letters to which limit the index. |
| [setLetterRange(String value)](#setLetterRange-java.lang.String-) | Sets a range of letters to which limit the index. |
| [getRunSubentriesOnSameLine()](#getRunSubentriesOnSameLine--) | Gets whether run subentries into the same line as the main entry. |
| [setRunSubentriesOnSameLine(boolean value)](#setRunSubentriesOnSameLine-boolean-) | Sets whether run subentries into the same line as the main entry. |
| [getSequenceName()](#getSequenceName--) | Gets the name of a sequence whose number is included with the page number. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String-) | Sets the name of a sequence whose number is included with the page number. |
| [hasSequenceName()](#hasSequenceName--) | Gets a value indicating whether a sequence should be used while the field's result building. |
| [getUseYomi()](#getUseYomi--) | Gets whether to enable the use of yomi text for index entries. |
| [setUseYomi(boolean value)](#setUseYomi-boolean-) | Sets whether to enable the use of yomi text for index entries. |
| [getLanguageId()](#getLanguageId--) | Gets the language ID used to generate the index. |
| [setLanguageId(String value)](#setLanguageId-java.lang.String-) | Sets the language ID used to generate the index. |
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


Gets the name of the bookmark that marks the portion of the document used to build the index.

**Returns:**
java.lang.String - The name of the bookmark that marks the portion of the document used to build the index.
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


Sets the name of the bookmark that marks the portion of the document used to build the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks the portion of the document used to build the index. |

### getNumberOfColumns() {#getNumberOfColumns--}
```
public String getNumberOfColumns()
```


Gets the number of columns per page used when building the index.

**Returns:**
java.lang.String - The number of columns per page used when building the index.
### setNumberOfColumns(String value) {#setNumberOfColumns-java.lang.String-}
```
public void setNumberOfColumns(String value)
```


Sets the number of columns per page used when building the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of columns per page used when building the index. |

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

### getPageNumberSeparator() {#getPageNumberSeparator--}
```
public String getPageNumberSeparator()
```


Gets the character sequence that is used to separate an index entry and its page number.

**Returns:**
java.lang.String - The character sequence that is used to separate an index entry and its page number.
### setPageNumberSeparator(String value) {#setPageNumberSeparator-java.lang.String-}
```
public void setPageNumberSeparator(String value)
```


Sets the character sequence that is used to separate an index entry and its page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate an index entry and its page number. |

### hasPageNumberSeparator() {#hasPageNumberSeparator--}
```
public boolean hasPageNumberSeparator()
```


Gets a value indicating whether a page number separator is overridden through the field's code.

**Returns:**
boolean - A value indicating whether a page number separator is overridden through the field's code.
### getEntryType() {#getEntryType--}
```
public String getEntryType()
```


Gets an index entry type used to build the index.

**Returns:**
java.lang.String - An index entry type used to build the index.
### setEntryType(String value) {#setEntryType-java.lang.String-}
```
public void setEntryType(String value)
```


Sets an index entry type used to build the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An index entry type used to build the index. |

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

### getHeading() {#getHeading--}
```
public String getHeading()
```


Gets a heading that appears at the start of each set of entries for any given letter.

**Returns:**
java.lang.String - A heading that appears at the start of each set of entries for any given letter.
### setHeading(String value) {#setHeading-java.lang.String-}
```
public void setHeading(String value)
```


Sets a heading that appears at the start of each set of entries for any given letter.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A heading that appears at the start of each set of entries for any given letter. |

### getCrossReferenceSeparator() {#getCrossReferenceSeparator--}
```
public String getCrossReferenceSeparator()
```


Gets the character sequence that is used to separate cross references and other entries.

**Returns:**
java.lang.String - The character sequence that is used to separate cross references and other entries.
### setCrossReferenceSeparator(String value) {#setCrossReferenceSeparator-java.lang.String-}
```
public void setCrossReferenceSeparator(String value)
```


Sets the character sequence that is used to separate cross references and other entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate cross references and other entries. |

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

### getLetterRange() {#getLetterRange--}
```
public String getLetterRange()
```


Gets a range of letters to which limit the index.

**Returns:**
java.lang.String - A range of letters to which limit the index.
### setLetterRange(String value) {#setLetterRange-java.lang.String-}
```
public void setLetterRange(String value)
```


Sets a range of letters to which limit the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of letters to which limit the index. |

### getRunSubentriesOnSameLine() {#getRunSubentriesOnSameLine--}
```
public boolean getRunSubentriesOnSameLine()
```


Gets whether run subentries into the same line as the main entry.

**Returns:**
boolean - Whether run subentries into the same line as the main entry.
### setRunSubentriesOnSameLine(boolean value) {#setRunSubentriesOnSameLine-boolean-}
```
public void setRunSubentriesOnSameLine(boolean value)
```


Sets whether run subentries into the same line as the main entry.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether run subentries into the same line as the main entry. |

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

### hasSequenceName() {#hasSequenceName--}
```
public boolean hasSequenceName()
```


Gets a value indicating whether a sequence should be used while the field's result building.

**Returns:**
boolean - A value indicating whether a sequence should be used while the field's result building.
### getUseYomi() {#getUseYomi--}
```
public boolean getUseYomi()
```


Gets whether to enable the use of yomi text for index entries.

**Returns:**
boolean - Whether to enable the use of yomi text for index entries.
### setUseYomi(boolean value) {#setUseYomi-boolean-}
```
public void setUseYomi(boolean value)
```


Sets whether to enable the use of yomi text for index entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to enable the use of yomi text for index entries. |

### getLanguageId() {#getLanguageId--}
```
public String getLanguageId()
```


Gets the language ID used to generate the index.

**Returns:**
java.lang.String - The language ID used to generate the index.
### setLanguageId(String value) {#setLanguageId-java.lang.String-}
```
public void setLanguageId(String value)
```


Sets the language ID used to generate the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The language ID used to generate the index. |

