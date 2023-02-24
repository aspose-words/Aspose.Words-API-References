---
title: FieldXE
linktitle: FieldXE
second_title: Aspose.Words for Java API Reference
description: Implements the XE field in Java.
type: docs
weight: 264
url: /java/com.aspose.words/fieldxe/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldXE extends Field
```

Implements the XE field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

Defines the text and page number for an index entry, which is used by an INDEX field.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getEntryType()](#getEntryType) | Gets an index entry type. |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getPageNumberReplacement()](#getPageNumberReplacement) | Gets text used in place of a page number. |
| [getPageRangeBookmarkName()](#getPageRangeBookmarkName) | Gets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getText()](#getText) | Gets the text of the entry. |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [getYomi()](#getYomi) | Gets the yomi (first phonetic character for sorting indexes) for the index entry |
| [hashCode()](#hashCode) |  |
| [isBold()](#isBold) | Gets whether to apply bold formatting to the entry's page number. |
| [isBold(boolean value)](#isBold-boolean) | Sets whether to apply bold formatting to the entry's page number. |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isItalic()](#isItalic) | Gets whether to apply italic formatting to the entry's page number. |
| [isItalic(boolean value)](#isItalic-boolean) | Sets whether to apply italic formatting to the entry's page number. |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the field from the document. |
| [setEntryType(String value)](#setEntryType-java.lang.String) | Sets an index entry type. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setPageNumberReplacement(String value)](#setPageNumberReplacement-java.lang.String) | Sets text used in place of a page number. |
| [setPageRangeBookmarkName(String value)](#setPageRangeBookmarkName-java.lang.String) | Sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [setText(String value)](#setText-java.lang.String) | Sets the text of the entry. |
| [setYomi(String value)](#setYomi-java.lang.String) | Sets the yomi (first phonetic character for sorting indexes) for the index entry |
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
### getEntryType() {#getEntryType}
```
public String getEntryType()
```


Gets an index entry type.

**Returns:**
java.lang.String - An index entry type.
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
### getPageNumberReplacement() {#getPageNumberReplacement}
```
public String getPageNumberReplacement()
```


Gets text used in place of a page number.

**Returns:**
java.lang.String - Text used in place of a page number.
### getPageRangeBookmarkName() {#getPageRangeBookmarkName}
```
public String getPageRangeBookmarkName()
```


Gets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.

**Returns:**
java.lang.String - The name of the bookmark that marks a range of pages that is inserted as the entry's page number.
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
### getText() {#getText}
```
public String getText()
```


Gets the text of the entry.

**Returns:**
java.lang.String - The text of the entry.
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype/) constants.
### getYomi() {#getYomi}
```
public String getYomi()
```


Gets the yomi (first phonetic character for sorting indexes) for the index entry

**Returns:**
java.lang.String - The yomi (first phonetic character for sorting indexes) for the index entry
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isBold() {#isBold}
```
public boolean isBold()
```


Gets whether to apply bold formatting to the entry's page number.

**Returns:**
boolean - Whether to apply bold formatting to the entry's page number.
### isBold(boolean value) {#isBold-boolean}
```
public void isBold(boolean value)
```


Sets whether to apply bold formatting to the entry's page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to apply bold formatting to the entry's page number. |

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

### isItalic() {#isItalic}
```
public boolean isItalic()
```


Gets whether to apply italic formatting to the entry's page number.

**Returns:**
boolean - Whether to apply italic formatting to the entry's page number.
### isItalic(boolean value) {#isItalic-boolean}
```
public void isItalic(boolean value)
```


Sets whether to apply italic formatting to the entry's page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to apply italic formatting to the entry's page number. |

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
### setEntryType(String value) {#setEntryType-java.lang.String}
```
public void setEntryType(String value)
```


Sets an index entry type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An index entry type. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setPageNumberReplacement(String value) {#setPageNumberReplacement-java.lang.String}
```
public void setPageNumberReplacement(String value)
```


Sets text used in place of a page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text used in place of a page number. |

### setPageRangeBookmarkName(String value) {#setPageRangeBookmarkName-java.lang.String}
```
public void setPageRangeBookmarkName(String value)
```


Sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks a range of pages that is inserted as the entry's page number. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Sets the text of the entry.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text of the entry. |

### setYomi(String value) {#setYomi-java.lang.String}
```
public void setYomi(String value)
```


Sets the yomi (first phonetic character for sorting indexes) for the index entry

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The yomi (first phonetic character for sorting indexes) for the index entry |

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

