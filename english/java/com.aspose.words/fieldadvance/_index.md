---
title: FieldAdvance
second_title: Aspose.Words for Java API Reference
description: Implements the ADVANCE field.
type: docs
weight: 154
url: /java/com.aspose.words/fieldadvance/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldAdvance extends Field
```

Implements the ADVANCE field.

To learn more, visit the **Working with Fields** documentation article.

Moves the starting point at which the text that lexically follows the field is displayed to the right or left, up or down, or to a specific horizontal or vertical position.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Gets the text that represents the displayed field result. |
| [getDownOffset()](#getDownOffset--) | Gets the number of points by which the text that follows the field should be moved down. |
| [getEnd()](#getEnd--) | Gets the node that represents the field end. |
| [getFieldCode()](#getFieldCode--) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat--) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getHorizontalPosition()](#getHorizontalPosition--) | Gets the number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box. |
| [getLeftOffset()](#getLeftOffset--) | Gets the number of points by which the text that follows the field should be moved left. |
| [getLocaleId()](#getLocaleId--) | Gets the LCID of the field. |
| [getResult()](#getResult--) | Gets text that is between the field separator and field end. |
| [getRightOffset()](#getRightOffset--) | Gets the number of points by which the text that follows the field should be moved right. |
| [getSeparator()](#getSeparator--) | Gets the node that represents the field separator. |
| [getStart()](#getStart--) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Gets the Microsoft Word field type. |
| [getUpOffset()](#getUpOffset--) | Gets the number of points by which the text that follows the field should be moved up. |
| [getVerticalPosition()](#getVerticalPosition--) | Gets the number of points by which the text that follows the field should be moved vertically from the top edge of the page. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean-) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked--) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean-) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Removes the field from the document. |
| [setDownOffset(String value)](#setDownOffset-java.lang.String-) | Sets the number of points by which the text that follows the field should be moved down. |
| [setHorizontalPosition(String value)](#setHorizontalPosition-java.lang.String-) | Sets the number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box. |
| [setLeftOffset(String value)](#setLeftOffset-java.lang.String-) | Sets the number of points by which the text that follows the field should be moved left. |
| [setLocaleId(int value)](#setLocaleId-int-) | Sets the LCID of the field. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets text that is between the field separator and field end. |
| [setRightOffset(String value)](#setRightOffset-java.lang.String-) | Sets the number of points by which the text that follows the field should be moved right. |
| [setUpOffset(String value)](#setUpOffset-java.lang.String-) | Sets the number of points by which the text that follows the field should be moved up. |
| [setVerticalPosition(String value)](#setVerticalPosition-java.lang.String-) | Sets the number of points by which the text that follows the field should be moved vertically from the top edge of the page. |
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
### getDownOffset() {#getDownOffset--}
```
public String getDownOffset()
```


Gets the number of points by which the text that follows the field should be moved down.

**Returns:**
java.lang.String - The number of points by which the text that follows the field should be moved down.
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
### getHorizontalPosition() {#getHorizontalPosition--}
```
public String getHorizontalPosition()
```


Gets the number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box.

**Returns:**
java.lang.String - The number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box.
### getLeftOffset() {#getLeftOffset--}
```
public String getLeftOffset()
```


Gets the number of points by which the text that follows the field should be moved left.

**Returns:**
java.lang.String - The number of points by which the text that follows the field should be moved left.
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
### getRightOffset() {#getRightOffset--}
```
public String getRightOffset()
```


Gets the number of points by which the text that follows the field should be moved right.

**Returns:**
java.lang.String - The number of points by which the text that follows the field should be moved right.
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
### getUpOffset() {#getUpOffset--}
```
public String getUpOffset()
```


Gets the number of points by which the text that follows the field should be moved up.

**Returns:**
java.lang.String - The number of points by which the text that follows the field should be moved up.
### getVerticalPosition() {#getVerticalPosition--}
```
public String getVerticalPosition()
```


Gets the number of points by which the text that follows the field should be moved vertically from the top edge of the page.

**Returns:**
java.lang.String - The number of points by which the text that follows the field should be moved vertically from the top edge of the page.
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
### setDownOffset(String value) {#setDownOffset-java.lang.String-}
```
public void setDownOffset(String value)
```


Sets the number of points by which the text that follows the field should be moved down.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of points by which the text that follows the field should be moved down. |

### setHorizontalPosition(String value) {#setHorizontalPosition-java.lang.String-}
```
public void setHorizontalPosition(String value)
```


Sets the number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box. |

### setLeftOffset(String value) {#setLeftOffset-java.lang.String-}
```
public void setLeftOffset(String value)
```


Sets the number of points by which the text that follows the field should be moved left.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of points by which the text that follows the field should be moved left. |

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

### setRightOffset(String value) {#setRightOffset-java.lang.String-}
```
public void setRightOffset(String value)
```


Sets the number of points by which the text that follows the field should be moved right.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of points by which the text that follows the field should be moved right. |

### setUpOffset(String value) {#setUpOffset-java.lang.String-}
```
public void setUpOffset(String value)
```


Sets the number of points by which the text that follows the field should be moved up.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of points by which the text that follows the field should be moved up. |

### setVerticalPosition(String value) {#setVerticalPosition-java.lang.String-}
```
public void setVerticalPosition(String value)
```


Sets the number of points by which the text that follows the field should be moved vertically from the top edge of the page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number of points by which the text that follows the field should be moved vertically from the top edge of the page. |

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

