---
title: FieldToa
linktitle: FieldToa
second_title: Aspose.Words for Java API Reference
description: Implements the TOA field in Java.
type: docs
weight: 255
url: /java/com.aspose.words/fieldtoa/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldToa extends Field
```

Implements the TOA field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

Builds a table of authorities (that is, a list of the references in a legal document, such as references to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the entries specified by TA fields.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getBookmarkName()](#getBookmarkName) | Gets the name of the bookmark that marks the portion of the document used to build the table. |
| [getClass()](#getClass) |  |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getEntryCategory()](#getEntryCategory) | Gets the integral category for entries included in the table. |
| [getEntrySeparator()](#getEntrySeparator) | Gets the character sequence that is used to separate a table of authorities entry and its page number. |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator) | Gets the character sequence that is used to separate two page numbers in a page number list. |
| [getPageRangeSeparator()](#getPageRangeSeparator) | Gets the character sequence that is used to separate the start and end of a page range. |
| [getRemoveEntryFormatting()](#getRemoveEntryFormatting) | Gets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getSequenceName()](#getSequenceName) | Gets the name of a sequence whose number is included with the page number. |
| [getSequenceSeparator()](#getSequenceSeparator) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [getUseHeading()](#getUseHeading) | Gets whether to include the category heading for the entries in a table of authorities. |
| [getUsePassim()](#getUsePassim) | Gets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |
| [hashCode()](#hashCode) |  |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the field from the document. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Sets the name of the bookmark that marks the portion of the document used to build the table. |
| [setEntryCategory(String value)](#setEntryCategory-java.lang.String) | Sets the integral category for entries included in the table. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String) | Sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String) | Sets the character sequence that is used to separate two page numbers in a page number list. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String) | Sets the character sequence that is used to separate the start and end of a page range. |
| [setRemoveEntryFormatting(boolean value)](#setRemoveEntryFormatting-boolean) | Sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String) | Sets the name of a sequence whose number is included with the page number. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [setUseHeading(boolean value)](#setUseHeading-boolean) | Sets whether to include the category heading for the entries in a table of authorities. |
| [setUsePassim(boolean value)](#setUsePassim-boolean) | Sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |
| [toString()](#toString) |  |
| [unlink()](#unlink) | Performs the field unlink. |
| [update()](#update) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Performs a field update. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Gets the name of the bookmark that marks the portion of the document used to build the table.

**Returns:**
java.lang.String - The name of the bookmark that marks the portion of the document used to build the table.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result. The [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/) fields.

**Returns:**
java.lang.String - The text that represents the displayed field result.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend/) - The node that represents the field end.
### getEntryCategory() {#getEntryCategory}
```
public String getEntryCategory()
```


Gets the integral category for entries included in the table.

**Returns:**
java.lang.String - The integral category for entries included in the table.
### getEntrySeparator() {#getEntrySeparator}
```
public String getEntrySeparator()
```


Gets the character sequence that is used to separate a table of authorities entry and its page number.

**Returns:**
java.lang.String - The character sequence that is used to separate a table of authorities entry and its page number.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Returns text between field start and field separator (or field end if there is no separator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ true  if child field codes should be included. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat/) - A [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### getPageNumberListSeparator() {#getPageNumberListSeparator}
```
public String getPageNumberListSeparator()
```


Gets the character sequence that is used to separate two page numbers in a page number list.

**Returns:**
java.lang.String - The character sequence that is used to separate two page numbers in a page number list.
### getPageRangeSeparator() {#getPageRangeSeparator}
```
public String getPageRangeSeparator()
```


Gets the character sequence that is used to separate the start and end of a page range.

**Returns:**
java.lang.String - The character sequence that is used to separate the start and end of a page range.
### getRemoveEntryFormatting() {#getRemoveEntryFormatting}
```
public boolean getRemoveEntryFormatting()
```


Gets whether to remove the formatting of the entry text in the document from the entry in the table of authorities.

**Returns:**
boolean - Whether to remove the formatting of the entry text in the document from the entry in the table of authorities.
### getResult() {#getResult}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be  null .

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getSequenceName() {#getSequenceName}
```
public String getSequenceName()
```


Gets the name of a sequence whose number is included with the page number.

**Returns:**
java.lang.String - The name of a sequence whose number is included with the page number.
### getSequenceSeparator() {#getSequenceSeparator}
```
public String getSequenceSeparator()
```


Gets the character sequence that is used to separate sequence numbers and page numbers.

**Returns:**
java.lang.String - The character sequence that is used to separate sequence numbers and page numbers.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype/) constants.
### getUseHeading() {#getUseHeading}
```
public boolean getUseHeading()
```


Gets whether to include the category heading for the entries in a table of authorities.

**Returns:**
boolean - Whether to include the category heading for the entries in a table of authorities.
### getUsePassim() {#getUsePassim}
```
public boolean getUsePassim()
```


Gets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.

**Returns:**
boolean - Whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove() {#remove}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns  null .

**Returns:**
[Node](../../com.aspose.words/node/)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String}
```
public void setBookmarkName(String value)
```


Sets the name of the bookmark that marks the portion of the document used to build the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks the portion of the document used to build the table. |

### setEntryCategory(String value) {#setEntryCategory-java.lang.String}
```
public void setEntryCategory(String value)
```


Sets the integral category for entries included in the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The integral category for entries included in the table. |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String}
```
public void setEntrySeparator(String value)
```


Sets the character sequence that is used to separate a table of authorities entry and its page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate a table of authorities entry and its page number. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String}
```
public void setPageNumberListSeparator(String value)
```


Sets the character sequence that is used to separate two page numbers in a page number list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate two page numbers in a page number list. |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String}
```
public void setPageRangeSeparator(String value)
```


Sets the character sequence that is used to separate the start and end of a page range.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate the start and end of a page range. |

### setRemoveEntryFormatting(boolean value) {#setRemoveEntryFormatting-boolean}
```
public void setRemoveEntryFormatting(boolean value)
```


Sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setSequenceName(String value) {#setSequenceName-java.lang.String}
```
public void setSequenceName(String value)
```


Sets the name of a sequence whose number is included with the page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of a sequence whose number is included with the page number. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


Sets the character sequence that is used to separate sequence numbers and page numbers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate sequence numbers and page numbers. |

### setUseHeading(boolean value) {#setUseHeading-boolean}
```
public void setUseHeading(boolean value)
```


Sets whether to include the category heading for the entries in a table of authorities.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to include the category heading for the entries in a table of authorities. |

### setUsePassim(boolean value) {#setUsePassim-boolean}
```
public void setUsePassim(boolean value)
```


Sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### unlink() {#unlink}
```
public boolean unlink()
```


Performs the field unlink.

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

**Returns:**
boolean - \{ true  if the field has been unlinked, otherwise  false .
### update() {#update}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Performs a field update. Throws if the field is being updated already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

