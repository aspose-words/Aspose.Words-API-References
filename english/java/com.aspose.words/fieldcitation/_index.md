---
title: FieldCitation
second_title: Aspose.Words for Java API Reference
description: Implements the CITATION field.
type: docs
weight: 168
url: /java/com.aspose.words/fieldcitation/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldCitation extends Field
```

Implements the CITATION field.

To learn more, visit the **Working with Fields** documentation article.

Inserts the contents of the **Source** element with a specified **Tag** element using a bibliographic style.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAnotherSourceTag()](#getAnotherSourceTag--) | Gets a value that mathes the **Tag** element's value of another source to be included in the citation. |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd--) | Gets the node that represents the field end. |
| [getFieldCode()](#getFieldCode--) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat--) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getFormatLanguageId()](#getFormatLanguageId--) | Gets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document. |
| [getLocaleId()](#getLocaleId--) | Gets the LCID of the field. |
| [getPageNumber()](#getPageNumber--) | Gets a page number associated with the citation. |
| [getPrefix()](#getPrefix--) | Gets a prefix that is prepended to the citation. |
| [getResult()](#getResult--) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator--) | Gets the node that represents the field separator. |
| [getSourceTag()](#getSourceTag--) | Gets a value that mathes the **Tag** element's value of the source to insert. |
| [getStart()](#getStart--) | Gets the node that represents the start of the field. |
| [getSuffix()](#getSuffix--) | Gets a suffix that is appended to the citation. |
| [getSuppressAuthor()](#getSuppressAuthor--) | Gets whether the author information is suppressed from the citation. |
| [getSuppressTitle()](#getSuppressTitle--) | Gets whether the title information is suppressed from the citation. |
| [getSuppressYear()](#getSuppressYear--) | Gets whether the year information is suppressed from the citation. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Gets the Microsoft Word field type. |
| [getVolumeNumber()](#getVolumeNumber--) | Gets a volume number associated with the citation. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean-) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked--) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean-) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Removes the field from the document. |
| [setAnotherSourceTag(String value)](#setAnotherSourceTag-java.lang.String-) | Sets a value that mathes the **Tag** element's value of another source to be included in the citation. |
| [setFormatLanguageId(String value)](#setFormatLanguageId-java.lang.String-) | Sets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document. |
| [setLocaleId(int value)](#setLocaleId-int-) | Sets the LCID of the field. |
| [setPageNumber(String value)](#setPageNumber-java.lang.String-) | Sets a page number associated with the citation. |
| [setPrefix(String value)](#setPrefix-java.lang.String-) | Sets a prefix that is prepended to the citation. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets text that is between the field separator and field end. |
| [setSourceTag(String value)](#setSourceTag-java.lang.String-) | Sets a value that mathes the **Tag** element's value of the source to insert. |
| [setSuffix(String value)](#setSuffix-java.lang.String-) | Sets a suffix that is appended to the citation. |
| [setSuppressAuthor(boolean value)](#setSuppressAuthor-boolean-) | Sets whether the author information is suppressed from the citation. |
| [setSuppressTitle(boolean value)](#setSuppressTitle-boolean-) | Sets whether the title information is suppressed from the citation. |
| [setSuppressYear(boolean value)](#setSuppressYear-boolean-) | Sets whether the year information is suppressed from the citation. |
| [setVolumeNumber(String value)](#setVolumeNumber-java.lang.String-) | Sets a volume number associated with the citation. |
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
### getAnotherSourceTag() {#getAnotherSourceTag--}
```
public String getAnotherSourceTag()
```


Gets a value that mathes the **Tag** element's value of another source to be included in the citation.

**Returns:**
java.lang.String - A value that mathes the **Tag** element's value of another source to be included in the citation.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### getFormatLanguageId() {#getFormatLanguageId--}
```
public String getFormatLanguageId()
```


Gets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document.

**Returns:**
java.lang.String - The language ID that is used in conjunction with the specified bibliographic style to format the citation in the document.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### getPageNumber() {#getPageNumber--}
```
public String getPageNumber()
```


Gets a page number associated with the citation.

**Returns:**
java.lang.String - A page number associated with the citation.
### getPrefix() {#getPrefix--}
```
public String getPrefix()
```


Gets a prefix that is prepended to the citation.

**Returns:**
java.lang.String - A prefix that is prepended to the citation.
### getResult() {#getResult--}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be null.

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - The node that represents the field separator.
### getSourceTag() {#getSourceTag--}
```
public String getSourceTag()
```


Gets a value that mathes the **Tag** element's value of the source to insert.

**Returns:**
java.lang.String - A value that mathes the **Tag** element's value of the source to insert.
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart) - The node that represents the start of the field.
### getSuffix() {#getSuffix--}
```
public String getSuffix()
```


Gets a suffix that is appended to the citation.

**Returns:**
java.lang.String - A suffix that is appended to the citation.
### getSuppressAuthor() {#getSuppressAuthor--}
```
public boolean getSuppressAuthor()
```


Gets whether the author information is suppressed from the citation.

**Returns:**
boolean - Whether the author information is suppressed from the citation.
### getSuppressTitle() {#getSuppressTitle--}
```
public boolean getSuppressTitle()
```


Gets whether the title information is suppressed from the citation.

**Returns:**
boolean - Whether the title information is suppressed from the citation.
### getSuppressYear() {#getSuppressYear--}
```
public boolean getSuppressYear()
```


Gets whether the year information is suppressed from the citation.

**Returns:**
boolean - Whether the year information is suppressed from the citation.
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
### getVolumeNumber() {#getVolumeNumber--}
```
public String getVolumeNumber()
```


Gets a volume number associated with the citation.

**Returns:**
java.lang.String - A volume number associated with the citation.
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
### setAnotherSourceTag(String value) {#setAnotherSourceTag-java.lang.String-}
```
public void setAnotherSourceTag(String value)
```


Sets a value that mathes the **Tag** element's value of another source to be included in the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A value that mathes the **Tag** element's value of another source to be included in the citation. |

### setFormatLanguageId(String value) {#setFormatLanguageId-java.lang.String-}
```
public void setFormatLanguageId(String value)
```


Sets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The language ID that is used in conjunction with the specified bibliographic style to format the citation in the document. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setPageNumber(String value) {#setPageNumber-java.lang.String-}
```
public void setPageNumber(String value)
```


Sets a page number associated with the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A page number associated with the citation. |

### setPrefix(String value) {#setPrefix-java.lang.String-}
```
public void setPrefix(String value)
```


Sets a prefix that is prepended to the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A prefix that is prepended to the citation. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setSourceTag(String value) {#setSourceTag-java.lang.String-}
```
public void setSourceTag(String value)
```


Sets a value that mathes the **Tag** element's value of the source to insert.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A value that mathes the **Tag** element's value of the source to insert. |

### setSuffix(String value) {#setSuffix-java.lang.String-}
```
public void setSuffix(String value)
```


Sets a suffix that is appended to the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A suffix that is appended to the citation. |

### setSuppressAuthor(boolean value) {#setSuppressAuthor-boolean-}
```
public void setSuppressAuthor(boolean value)
```


Sets whether the author information is suppressed from the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the author information is suppressed from the citation. |

### setSuppressTitle(boolean value) {#setSuppressTitle-boolean-}
```
public void setSuppressTitle(boolean value)
```


Sets whether the title information is suppressed from the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the title information is suppressed from the citation. |

### setSuppressYear(boolean value) {#setSuppressYear-boolean-}
```
public void setSuppressYear(boolean value)
```


Sets whether the year information is suppressed from the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the year information is suppressed from the citation. |

### setVolumeNumber(String value) {#setVolumeNumber-java.lang.String-}
```
public void setVolumeNumber(String value)
```


Sets a volume number associated with the citation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A volume number associated with the citation. |

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

