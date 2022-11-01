---
title: FieldFileSize
second_title: Aspose.Words for Java API Reference
description: Implements the FILESIZE field.
type: docs
weight: 188
url: /java/com.aspose.words/fieldfilesize/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldFileSize extends Field
```

Implements the FILESIZE field.

To learn more, visit the **Working with Fields** documentation article.

Retrieves the size of the current document's file or 0 if the size cannot be determined.

In the current implementation, uses the [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) property to retrieve the file name used to determine the file size.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd--) | Gets the node that represents the field end. |
| [getFieldCode()](#getFieldCode--) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat--) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId--) | Gets the LCID of the field. |
| [getResult()](#getResult--) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator--) | Gets the node that represents the field separator. |
| [getStart()](#getStart--) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Gets the Microsoft Word field type. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean-) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isInKilobytes()](#isInKilobytes--) | Gets whether to display the file size in kilobytes. |
| [isInKilobytes(boolean value)](#isInKilobytes-boolean-) | Sets whether to display the file size in kilobytes. |
| [isInMegabytes()](#isInMegabytes--) | Gets whether to display the file size in megabytes. |
| [isInMegabytes(boolean value)](#isInMegabytes-boolean-) | Sets whether to display the file size in megabytes. |
| [isLocked()](#isLocked--) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean-) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Removes the field from the document. |
| [setLocaleId(int value)](#setLocaleId-int-) | Sets the LCID of the field. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets text that is between the field separator and field end. |
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
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
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

### isInKilobytes() {#isInKilobytes--}
```
public boolean isInKilobytes()
```


Gets whether to display the file size in kilobytes.

**Returns:**
boolean - Whether to display the file size in kilobytes.
### isInKilobytes(boolean value) {#isInKilobytes-boolean-}
```
public void isInKilobytes(boolean value)
```


Sets whether to display the file size in kilobytes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to display the file size in kilobytes. |

### isInMegabytes() {#isInMegabytes--}
```
public boolean isInMegabytes()
```


Gets whether to display the file size in megabytes.

**Returns:**
boolean - Whether to display the file size in megabytes.
### isInMegabytes(boolean value) {#isInMegabytes-boolean-}
```
public void isInMegabytes(boolean value)
```


Sets whether to display the file size in megabytes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to display the file size in megabytes. |

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
### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

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

