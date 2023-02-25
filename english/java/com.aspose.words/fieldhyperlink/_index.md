---
title: FieldHyperlink
linktitle: FieldHyperlink
second_title: Aspose.Words for Java API Reference
description: Implements the HYPERLINK field in Java.
type: docs
weight: 200
url: /java/com.aspose.words/fieldhyperlink/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldHyperlink extends Field
```

Implements the HYPERLINK field

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

When selected, causes control to jump to the location such as a bookmark or a URL.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAddress()](#getAddress) | Gets a location where this hyperlink jumps. |
| [getClass()](#getClass) |  |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getOpenInNewWindow()](#getOpenInNewWindow) | Gets whether to open the destination site in a new web browser window. |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getScreenTip()](#getScreenTip) | Gets the ScreenTip text for the hyperlink. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getSourceNode()](#getSourceNode) |  |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSubAddress()](#getSubAddress) | Gets a location in the file, such as a bookmark, where this hyperlink jumps. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getTarget()](#getTarget) | Gets the target to which the link should be redirected. |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [hashCode()](#hashCode) |  |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isImageMap()](#isImageMap) | Gets whether to append coordinates to the hyperlink for a server-side image map. |
| [isImageMap(boolean value)](#isImageMap-boolean) | Sets whether to append coordinates to the hyperlink for a server-side image map. |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the field from the document. |
| [setAddress(String value)](#setAddress-java.lang.String) | Sets a location where this hyperlink jumps. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setOpenInNewWindow(boolean value)](#setOpenInNewWindow-boolean) | Sets whether to open the destination site in a new web browser window. |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [setScreenTip(String value)](#setScreenTip-java.lang.String) | Sets the ScreenTip text for the hyperlink. |
| [setSubAddress(String value)](#setSubAddress-java.lang.String) | Sets a location in the file, such as a bookmark, where this hyperlink jumps. |
| [setTarget(String value)](#setTarget-java.lang.String) | Sets the target to which the link should be redirected. |
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
### getAddress() {#getAddress}
```
public String getAddress()
```


Gets a location where this hyperlink jumps.

**Returns:**
java.lang.String - A location where this hyperlink jumps.
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
### getOpenInNewWindow() {#getOpenInNewWindow}
```
public boolean getOpenInNewWindow()
```


Gets whether to open the destination site in a new web browser window.

**Returns:**
boolean - Whether to open the destination site in a new web browser window.
### getResult() {#getResult}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getScreenTip() {#getScreenTip}
```
public String getScreenTip()
```


Gets the ScreenTip text for the hyperlink.

**Returns:**
java.lang.String - The ScreenTip text for the hyperlink.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be  null .

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getSourceNode() {#getSourceNode}
```
public Inline getSourceNode()
```




**Returns:**
[Inline](../../com.aspose.words/inline/)
### getStart() {#getStart}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSubAddress() {#getSubAddress}
```
public String getSubAddress()
```


Gets a location in the file, such as a bookmark, where this hyperlink jumps.

**Returns:**
java.lang.String - A location in the file, such as a bookmark, where this hyperlink jumps.
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
### getTarget() {#getTarget}
```
public String getTarget()
```


Gets the target to which the link should be redirected.

**Returns:**
java.lang.String - The target to which the link should be redirected.
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype/) constants.
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

### isImageMap() {#isImageMap}
```
public boolean isImageMap()
```


Gets whether to append coordinates to the hyperlink for a server-side image map.

**Returns:**
boolean - Whether to append coordinates to the hyperlink for a server-side image map.
### isImageMap(boolean value) {#isImageMap-boolean}
```
public void isImageMap(boolean value)
```


Sets whether to append coordinates to the hyperlink for a server-side image map.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to append coordinates to the hyperlink for a server-side image map. |

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
### setAddress(String value) {#setAddress-java.lang.String}
```
public void setAddress(String value)
```


Sets a location where this hyperlink jumps.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A location where this hyperlink jumps. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setOpenInNewWindow(boolean value) {#setOpenInNewWindow-boolean}
```
public void setOpenInNewWindow(boolean value)
```


Sets whether to open the destination site in a new web browser window.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to open the destination site in a new web browser window. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setScreenTip(String value) {#setScreenTip-java.lang.String}
```
public void setScreenTip(String value)
```


Sets the ScreenTip text for the hyperlink.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The ScreenTip text for the hyperlink. |

### setSubAddress(String value) {#setSubAddress-java.lang.String}
```
public void setSubAddress(String value)
```


Sets a location in the file, such as a bookmark, where this hyperlink jumps.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A location in the file, such as a bookmark, where this hyperlink jumps. |

### setTarget(String value) {#setTarget-java.lang.String}
```
public void setTarget(String value)
```


Sets the target to which the link should be redirected.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The target to which the link should be redirected. |

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

