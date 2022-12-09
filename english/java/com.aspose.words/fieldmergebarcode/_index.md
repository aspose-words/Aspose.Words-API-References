---
title: FieldMergeBarcode
second_title: Aspose.Words for Java API Reference
description: Implements the MERGEBARCODE field.
type: docs
weight: 215
url: /java/com.aspose.words/fieldmergebarcode/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldMergeBarcode extends Field
```

Implements the MERGEBARCODE field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

Mail merge a barcode.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [canWorkAsMergeField()](#canWorkAsMergeField) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAddStartStopChar()](#getAddStartStopChar) | Gets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [getBackgroundColor()](#getBackgroundColor) | Gets the background color of the barcode symbol. |
| [getBarcodeType()](#getBarcodeType) | Gets the barcode type (QR, etc.) |
| [getBarcodeValue()](#getBarcodeValue) | Gets the barcode value. |
| [getCaseCodeStyle()](#getCaseCodeStyle) | Gets the style of a Case Code for barcode type ITF14. |
| [getClass()](#getClass) |  |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getDisplayText()](#getDisplayText) | Gets whether to display barcode data (text) along with image. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel) | Gets an error correction level of QR Code. |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFixCheckDigit()](#getFixCheckDigit) | Gets whether to fix the check digit if it\\u2019s invalid. |
| [getForegroundColor()](#getForegroundColor) | Gets the foreground color of the barcode symbol. |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getMergeFieldName()](#getMergeFieldName) |  |
| [getPosCodeStyle()](#getPosCodeStyle) | Gets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getScalingFactor()](#getScalingFactor) | Gets a scaling factor for the symbol. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getSymbolHeight()](#getSymbolHeight) | Gets the height of the symbol. |
| [getSymbolRotation()](#getSymbolRotation) | Gets the rotation of the barcode symbol. |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [hashCode()](#hashCode) |  |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [isMergeValueRequired()](#isMergeValueRequired) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the field from the document. |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean) | Sets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String) | Sets the background color of the barcode symbol. |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String) | Sets the barcode type (QR, etc.) |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String) | Sets the barcode value. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String) | Sets the style of a Case Code for barcode type ITF14. |
| [setDisplayText(boolean value)](#setDisplayText-boolean) | Sets whether to display barcode data (text) along with image. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String) | Sets an error correction level of QR Code. |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean) | Sets whether to fix the check digit if it\\u2019s invalid. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String) | Sets the foreground color of the barcode symbol. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String) | Sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String) | Sets a scaling factor for the symbol. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String) | Sets the height of the symbol. |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String) | Sets the rotation of the barcode symbol. |
| [toString()](#toString) |  |
| [unlink()](#unlink) | Performs the field unlink. |
| [update()](#update) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Performs a field update. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### canWorkAsMergeField() {#canWorkAsMergeField}
```
public boolean canWorkAsMergeField()
```




**Returns:**
boolean
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
### getAddStartStopChar() {#getAddStartStopChar}
```
public boolean getAddStartStopChar()
```


Gets whether to add Start/Stop characters for barcode types NW7 and CODE39.

**Returns:**
boolean - Whether to add Start/Stop characters for barcode types NW7 and CODE39.
### getBackgroundColor() {#getBackgroundColor}
```
public String getBackgroundColor()
```


Gets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Returns:**
java.lang.String - The background color of the barcode symbol.
### getBarcodeType() {#getBarcodeType}
```
public String getBarcodeType()
```


Gets the barcode type (QR, etc.)

**Returns:**
java.lang.String - The barcode type (QR, etc.)
### getBarcodeValue() {#getBarcodeValue}
```
public String getBarcodeValue()
```


Gets the barcode value.

**Returns:**
java.lang.String - The barcode value.
### getCaseCodeStyle() {#getCaseCodeStyle}
```
public String getCaseCodeStyle()
```


Gets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

**Returns:**
java.lang.String - The style of a Case Code for barcode type ITF14.
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


Gets the text that represents the displayed field result. The [Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) fields.

**Returns:**
java.lang.String - The text that represents the displayed field result.
### getDisplayText() {#getDisplayText}
```
public boolean getDisplayText()
```


Gets whether to display barcode data (text) along with image.

**Returns:**
boolean - Whether to display barcode data (text) along with image.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend) - The node that represents the field end.
### getErrorCorrectionLevel() {#getErrorCorrectionLevel}
```
public String getErrorCorrectionLevel()
```


Gets an error correction level of QR Code. Valid values are [0, 3].

**Returns:**
java.lang.String - An error correction level of QR Code.
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
### getFixCheckDigit() {#getFixCheckDigit}
```
public boolean getFixCheckDigit()
```


Gets whether to fix the check digit if it\\u2019s invalid.

**Returns:**
boolean - Whether to fix the check digit if it\\u2019s invalid.
### getForegroundColor() {#getForegroundColor}
```
public String getForegroundColor()
```


Gets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Returns:**
java.lang.String - The foreground color of the barcode symbol.
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat) - A [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### getMergeFieldName() {#getMergeFieldName}
```
public String getMergeFieldName()
```




**Returns:**
java.lang.String
### getPosCodeStyle() {#getPosCodeStyle}
```
public String getPosCodeStyle()
```


Gets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Returns:**
java.lang.String - The style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8).
### getResult() {#getResult}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getScalingFactor() {#getScalingFactor}
```
public String getScalingFactor()
```


Gets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]

**Returns:**
java.lang.String - A scaling factor for the symbol.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be  null .

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - The node that represents the field separator.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart) - The node that represents the start of the field.
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
### getSymbolHeight() {#getSymbolHeight}
```
public String getSymbolHeight()
```


Gets the height of the symbol. The units are in TWIPS (1/1440 inch).

**Returns:**
java.lang.String - The height of the symbol.
### getSymbolRotation() {#getSymbolRotation}
```
public String getSymbolRotation()
```


Gets the rotation of the barcode symbol. Valid values are [0, 3]

**Returns:**
java.lang.String - The rotation of the barcode symbol.
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
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

### isMergeValueRequired() {#isMergeValueRequired}
```
public boolean isMergeValueRequired()
```




**Returns:**
boolean
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
[Node](../../com.aspose.words/node)
### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean}
```
public void setAddStartStopChar(boolean value)
```


Sets whether to add Start/Stop characters for barcode types NW7 and CODE39.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String}
```
public void setBackgroundColor(String value)
```


Sets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The background color of the barcode symbol. |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String}
```
public void setBarcodeType(String value)
```


Sets the barcode type (QR, etc.)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The barcode type (QR, etc.) |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String}
```
public void setBarcodeValue(String value)
```


Sets the barcode value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The barcode value. |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String}
```
public void setCaseCodeStyle(String value)
```


Sets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The style of a Case Code for barcode type ITF14. |

### setDisplayText(boolean value) {#setDisplayText-boolean}
```
public void setDisplayText(boolean value)
```


Sets whether to display barcode data (text) along with image.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to display barcode data (text) along with image. |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String}
```
public void setErrorCorrectionLevel(String value)
```


Sets an error correction level of QR Code. Valid values are [0, 3].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An error correction level of QR Code. |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean}
```
public void setFixCheckDigit(boolean value)
```


Sets whether to fix the check digit if it\\u2019s invalid.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to fix the check digit if it\\u2019s invalid. |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String}
```
public void setForegroundColor(String value)
```


Sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The foreground color of the barcode symbol. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String}
```
public void setPosCodeStyle(String value)
```


Sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String}
```
public void setScalingFactor(String value)
```


Sets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A scaling factor for the symbol. |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String}
```
public void setSymbolHeight(String value)
```


Sets the height of the symbol. The units are in TWIPS (1/1440 inch).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The height of the symbol. |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String}
```
public void setSymbolRotation(String value)
```


Sets the rotation of the barcode symbol. Valid values are [0, 3]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The rotation of the barcode symbol. |

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

