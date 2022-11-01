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
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | Gets the name of the bookmark that marks the portion of the document used to build the index. |
| [getClass()](#getClass--) |  |
| [getCrossReferenceSeparator()](#getCrossReferenceSeparator--) | Gets the character sequence that is used to separate cross references and other entries. |
| [getDisplayResult()](#getDisplayResult--) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd--) | Gets the node that represents the field end. |
| [getEntryType()](#getEntryType--) | Gets an index entry type used to build the index. |
| [getFieldCode()](#getFieldCode--) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat--) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getHeading()](#getHeading--) | Gets a heading that appears at the start of each set of entries for any given letter. |
| [getLanguageId()](#getLanguageId--) | Gets the language ID used to generate the index. |
| [getLetterRange()](#getLetterRange--) | Gets a range of letters to which limit the index. |
| [getLocaleId()](#getLocaleId--) | Gets the LCID of the field. |
| [getNumberOfColumns()](#getNumberOfColumns--) | Gets the number of columns per page used when building the index. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator--) | Gets the character sequence that is used to separate two page numbers in a page number list. |
| [getPageNumberSeparator()](#getPageNumberSeparator--) | Gets the character sequence that is used to separate an index entry and its page number. |
| [getPageRangeSeparator()](#getPageRangeSeparator--) | Gets the character sequence that is used to separate the start and end of a page range. |
| [getResult()](#getResult--) | Gets text that is between the field separator and field end. |
| [getRunSubentriesOnSameLine()](#getRunSubentriesOnSameLine--) | Gets whether run subentries into the same line as the main entry. |
| [getSeparator()](#getSeparator--) | Gets the node that represents the field separator. |
| [getSequenceName()](#getSequenceName--) | Gets the name of a sequence whose number is included with the page number. |
| [getSequenceSeparator()](#getSequenceSeparator--) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [getStart()](#getStart--) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Gets the Microsoft Word field type. |
| [getUseYomi()](#getUseYomi--) | Gets whether to enable the use of yomi text for index entries. |
| [hasPageNumberSeparator()](#hasPageNumberSeparator--) | Gets a value indicating whether a page number separator is overridden through the field's code. |
| [hasSequenceName()](#hasSequenceName--) | Gets a value indicating whether a sequence should be used while the field's result building. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean-) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked--) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean-) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Removes the field from the document. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Sets the name of the bookmark that marks the portion of the document used to build the index. |
| [setCrossReferenceSeparator(String value)](#setCrossReferenceSeparator-java.lang.String-) | Sets the character sequence that is used to separate cross references and other entries. |
| [setEntryType(String value)](#setEntryType-java.lang.String-) | Sets an index entry type used to build the index. |
| [setHeading(String value)](#setHeading-java.lang.String-) | Sets a heading that appears at the start of each set of entries for any given letter. |
| [setLanguageId(String value)](#setLanguageId-java.lang.String-) | Sets the language ID used to generate the index. |
| [setLetterRange(String value)](#setLetterRange-java.lang.String-) | Sets a range of letters to which limit the index. |
| [setLocaleId(int value)](#setLocaleId-int-) | Sets the LCID of the field. |
| [setNumberOfColumns(String value)](#setNumberOfColumns-java.lang.String-) | Sets the number of columns per page used when building the index. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String-) | Sets the character sequence that is used to separate two page numbers in a page number list. |
| [setPageNumberSeparator(String value)](#setPageNumberSeparator-java.lang.String-) | Sets the character sequence that is used to separate an index entry and its page number. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String-) | Sets the character sequence that is used to separate the start and end of a page range. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets text that is between the field separator and field end. |
| [setRunSubentriesOnSameLine(boolean value)](#setRunSubentriesOnSameLine-boolean-) | Sets whether run subentries into the same line as the main entry. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String-) | Sets the name of a sequence whose number is included with the page number. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [setUseYomi(boolean value)](#setUseYomi-boolean-) | Sets whether to enable the use of yomi text for index entries. |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | Performs the field unlink. |
| [update()](#update--) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | Performs a field update. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


Gets the name of the bookmark that marks the portion of the document used to build the index.

**Returns:**
java.lang.String - The name of the bookmark that marks the portion of the document used to build the index.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCrossReferenceSeparator() {#getCrossReferenceSeparator--}
```
public String getCrossReferenceSeparator()
```


Gets the character sequence that is used to separate cross references and other entries.

**Returns:**
java.lang.String - The character sequence that is used to separate cross references and other entries.
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result. The [Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) fields.

**Returns:**
java.lang.String - The text that represents the displayed field result.
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend) - The node that represents the field end.
### getEntryType() {#getEntryType--}
```
public String getEntryType()
```


Gets an index entry type used to build the index.

**Returns:**
java.lang.String - An index entry type used to build the index.
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Returns text between field start and field separator (or field end if there is no separator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ True  if child field codes should be included. |

**Returns:**
java.lang.String
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat) - A [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.
### getHeading() {#getHeading--}
```
public String getHeading()
```


Gets a heading that appears at the start of each set of entries for any given letter.

**Returns:**
java.lang.String - A heading that appears at the start of each set of entries for any given letter.
### getLanguageId() {#getLanguageId--}
```
public String getLanguageId()
```


Gets the language ID used to generate the index.

**Returns:**
java.lang.String - The language ID used to generate the index.
### getLetterRange() {#getLetterRange--}
```
public String getLetterRange()
```


Gets a range of letters to which limit the index.

**Returns:**
java.lang.String - A range of letters to which limit the index.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### getNumberOfColumns() {#getNumberOfColumns--}
```
public String getNumberOfColumns()
```


Gets the number of columns per page used when building the index.

**Returns:**
java.lang.String - The number of columns per page used when building the index.
### getPageNumberListSeparator() {#getPageNumberListSeparator--}
```
public String getPageNumberListSeparator()
```


Gets the character sequence that is used to separate two page numbers in a page number list.

**Returns:**
java.lang.String - The character sequence that is used to separate two page numbers in a page number list.
### getPageNumberSeparator() {#getPageNumberSeparator--}
```
public String getPageNumberSeparator()
```


Gets the character sequence that is used to separate an index entry and its page number.

**Returns:**
java.lang.String - The character sequence that is used to separate an index entry and its page number.
### getPageRangeSeparator() {#getPageRangeSeparator--}
```
public String getPageRangeSeparator()
```


Gets the character sequence that is used to separate the start and end of a page range.

**Returns:**
java.lang.String - The character sequence that is used to separate the start and end of a page range.
### getResult() {#getResult--}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getRunSubentriesOnSameLine() {#getRunSubentriesOnSameLine--}
```
public boolean getRunSubentriesOnSameLine()
```


Gets whether run subentries into the same line as the main entry.

**Returns:**
boolean - Whether run subentries into the same line as the main entry.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be null.

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - The node that represents the field separator.
### getSequenceName() {#getSequenceName--}
```
public String getSequenceName()
```


Gets the name of a sequence whose number is included with the page number.

**Returns:**
java.lang.String - The name of a sequence whose number is included with the page number.
### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


Gets the character sequence that is used to separate sequence numbers and page numbers.

**Returns:**
java.lang.String - The character sequence that is used to separate sequence numbers and page numbers.
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart) - The node that represents the start of the field.
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
### getType() {#getType--}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### getUseYomi() {#getUseYomi--}
```
public boolean getUseYomi()
```


Gets whether to enable the use of yomi text for index entries.

**Returns:**
boolean - Whether to enable the use of yomi text for index entries.
### hasPageNumberSeparator() {#hasPageNumberSeparator--}
```
public boolean hasPageNumberSeparator()
```


Gets a value indicating whether a page number separator is overridden through the field's code.

**Returns:**
boolean - A value indicating whether a page number separator is overridden through the field's code.
### hasSequenceName() {#hasSequenceName--}
```
public boolean hasSequenceName()
```


Gets a value indicating whether a sequence should be used while the field's result building.

**Returns:**
boolean - A value indicating whether a sequence should be used while the field's result building.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isDirty() {#isDirty--}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.

**Returns:**
[Node](../../com.aspose.words/node)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


Sets the name of the bookmark that marks the portion of the document used to build the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks the portion of the document used to build the index. |

### setCrossReferenceSeparator(String value) {#setCrossReferenceSeparator-java.lang.String-}
```
public void setCrossReferenceSeparator(String value)
```


Sets the character sequence that is used to separate cross references and other entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate cross references and other entries. |

### setEntryType(String value) {#setEntryType-java.lang.String-}
```
public void setEntryType(String value)
```


Sets an index entry type used to build the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An index entry type used to build the index. |

### setHeading(String value) {#setHeading-java.lang.String-}
```
public void setHeading(String value)
```


Sets a heading that appears at the start of each set of entries for any given letter.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A heading that appears at the start of each set of entries for any given letter. |

### setLanguageId(String value) {#setLanguageId-java.lang.String-}
```
public void setLanguageId(String value)
```


Sets the language ID used to generate the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The language ID used to generate the index. |

### setLetterRange(String value) {#setLetterRange-java.lang.String-}
```
public void setLetterRange(String value)
```


Sets a range of letters to which limit the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A range of letters to which limit the index. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setNumberOfColumns(String value) {#setNumberOfColumns-java.lang.String-}
```
public void setNumberOfColumns(String value)
```


Sets the number of columns per page used when building the index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of columns per page used when building the index. |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String-}
```
public void setPageNumberListSeparator(String value)
```


Sets the character sequence that is used to separate two page numbers in a page number list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate two page numbers in a page number list. |

### setPageNumberSeparator(String value) {#setPageNumberSeparator-java.lang.String-}
```
public void setPageNumberSeparator(String value)
```


Sets the character sequence that is used to separate an index entry and its page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate an index entry and its page number. |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String-}
```
public void setPageRangeSeparator(String value)
```


Sets the character sequence that is used to separate the start and end of a page range.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate the start and end of a page range. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setRunSubentriesOnSameLine(boolean value) {#setRunSubentriesOnSameLine-boolean-}
```
public void setRunSubentriesOnSameLine(boolean value)
```


Sets whether run subentries into the same line as the main entry.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether run subentries into the same line as the main entry. |

### setSequenceName(String value) {#setSequenceName-java.lang.String-}
```
public void setSequenceName(String value)
```


Sets the name of a sequence whose number is included with the page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of a sequence whose number is included with the page number. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


Sets the character sequence that is used to separate sequence numbers and page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate sequence numbers and page numbers. |

### setUseYomi(boolean value) {#setUseYomi-boolean-}
```
public void setUseYomi(boolean value)
```


Sets whether to enable the use of yomi text for index entries.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to enable the use of yomi text for index entries. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### unlink() {#unlink--}
```
public boolean unlink()
```


Performs the field unlink.

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

**Returns:**
boolean - \{ True  if the field has been unlinked, otherwise  false .
### update() {#update--}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


Performs a field update. Throws if the field is being updated already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

