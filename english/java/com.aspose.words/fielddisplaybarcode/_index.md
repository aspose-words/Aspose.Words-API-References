---
title: FieldDisplayBarcode
second_title: Aspose.Words for Java API Reference
description: Implements the DISPLAYBARCODE field.
type: docs
weight: 180
url: /java/com.aspose.words/fielddisplaybarcode/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldDisplayBarcode extends Field
```

Implements the DISPLAYBARCODE field.

To learn more, visit the **Working with Fields** documentation article.

Inserts a barcode.
## Methods

| Method | Description |
| --- | --- |
| [getBarcodeValue()](#getBarcodeValue--) | Gets the barcode value. |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String-) | Sets the barcode value. |
| [getBarcodeType()](#getBarcodeType--) | Gets the barcode type (QR, etc.) |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String-) | Sets the barcode type (QR, etc.) |
| [getSymbolHeight()](#getSymbolHeight--) | Gets the height of the symbol. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String-) | Sets the height of the symbol. |
| [getSymbolRotation()](#getSymbolRotation--) | Gets the rotation of the barcode symbol. |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String-) | Sets the rotation of the barcode symbol. |
| [getScalingFactor()](#getScalingFactor--) | Gets a scaling factor for the symbol. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String-) | Sets a scaling factor for the symbol. |
| [getForegroundColor()](#getForegroundColor--) | Gets the foreground color of the barcode symbol. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String-) | Sets the foreground color of the barcode symbol. |
| [getBackgroundColor()](#getBackgroundColor--) | Gets the background color of the barcode symbol. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String-) | Sets the background color of the barcode symbol. |
| [getPosCodeStyle()](#getPosCodeStyle--) | Gets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String-) | Sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [getCaseCodeStyle()](#getCaseCodeStyle--) | Gets the style of a Case Code for barcode type ITF14. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String-) | Sets the style of a Case Code for barcode type ITF14. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel--) | Gets an error correction level of QR Code. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String-) | Sets an error correction level of QR Code. |
| [getDisplayText()](#getDisplayText--) | Gets whether to display barcode data (text) along with image. |
| [setDisplayText(boolean value)](#setDisplayText-boolean-) | Sets whether to display barcode data (text) along with image. |
| [getAddStartStopChar()](#getAddStartStopChar--) | Gets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean-) | Sets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [getFixCheckDigit()](#getFixCheckDigit--) | Gets whether to fix the check digit if it\\u2019s invalid. |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean-) | Sets whether to fix the check digit if it\\u2019s invalid. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
### getBarcodeValue() {#getBarcodeValue--}
```
public String getBarcodeValue()
```


Gets the barcode value.

**Returns:**
java.lang.String - The barcode value.
### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String-}
```
public void setBarcodeValue(String value)
```


Sets the barcode value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The barcode value. |

### getBarcodeType() {#getBarcodeType--}
```
public String getBarcodeType()
```


Gets the barcode type (QR, etc.)

**Returns:**
java.lang.String - The barcode type (QR, etc.)
### setBarcodeType(String value) {#setBarcodeType-java.lang.String-}
```
public void setBarcodeType(String value)
```


Sets the barcode type (QR, etc.)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The barcode type (QR, etc.) |

### getSymbolHeight() {#getSymbolHeight--}
```
public String getSymbolHeight()
```


Gets the height of the symbol. The units are in TWIPS (1/1440 inch).

**Returns:**
java.lang.String - The height of the symbol.
### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String-}
```
public void setSymbolHeight(String value)
```


Sets the height of the symbol. The units are in TWIPS (1/1440 inch).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The height of the symbol. |

### getSymbolRotation() {#getSymbolRotation--}
```
public String getSymbolRotation()
```


Gets the rotation of the barcode symbol. Valid values are [0, 3]

**Returns:**
java.lang.String - The rotation of the barcode symbol.
### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String-}
```
public void setSymbolRotation(String value)
```


Sets the rotation of the barcode symbol. Valid values are [0, 3]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The rotation of the barcode symbol. |

### getScalingFactor() {#getScalingFactor--}
```
public String getScalingFactor()
```


Gets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]

**Returns:**
java.lang.String - A scaling factor for the symbol.
### setScalingFactor(String value) {#setScalingFactor-java.lang.String-}
```
public void setScalingFactor(String value)
```


Sets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A scaling factor for the symbol. |

### getForegroundColor() {#getForegroundColor--}
```
public String getForegroundColor()
```


Gets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Returns:**
java.lang.String - The foreground color of the barcode symbol.
### setForegroundColor(String value) {#setForegroundColor-java.lang.String-}
```
public void setForegroundColor(String value)
```


Sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The foreground color of the barcode symbol. |

### getBackgroundColor() {#getBackgroundColor--}
```
public String getBackgroundColor()
```


Gets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Returns:**
java.lang.String - The background color of the barcode symbol.
### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String-}
```
public void setBackgroundColor(String value)
```


Sets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The background color of the barcode symbol. |

### getPosCodeStyle() {#getPosCodeStyle--}
```
public String getPosCodeStyle()
```


Gets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Returns:**
java.lang.String - The style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8).
### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String-}
```
public void setPosCodeStyle(String value)
```


Sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |

### getCaseCodeStyle() {#getCaseCodeStyle--}
```
public String getCaseCodeStyle()
```


Gets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

**Returns:**
java.lang.String - The style of a Case Code for barcode type ITF14.
### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String-}
```
public void setCaseCodeStyle(String value)
```


Sets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The style of a Case Code for barcode type ITF14. |

### getErrorCorrectionLevel() {#getErrorCorrectionLevel--}
```
public String getErrorCorrectionLevel()
```


Gets an error correction level of QR Code. Valid values are [0, 3].

**Returns:**
java.lang.String - An error correction level of QR Code.
### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String-}
```
public void setErrorCorrectionLevel(String value)
```


Sets an error correction level of QR Code. Valid values are [0, 3].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An error correction level of QR Code. |

### getDisplayText() {#getDisplayText--}
```
public boolean getDisplayText()
```


Gets whether to display barcode data (text) along with image.

**Returns:**
boolean - Whether to display barcode data (text) along with image.
### setDisplayText(boolean value) {#setDisplayText-boolean-}
```
public void setDisplayText(boolean value)
```


Sets whether to display barcode data (text) along with image.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to display barcode data (text) along with image. |

### getAddStartStopChar() {#getAddStartStopChar--}
```
public boolean getAddStartStopChar()
```


Gets whether to add Start/Stop characters for barcode types NW7 and CODE39.

**Returns:**
boolean - Whether to add Start/Stop characters for barcode types NW7 and CODE39.
### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean-}
```
public void setAddStartStopChar(boolean value)
```


Sets whether to add Start/Stop characters for barcode types NW7 and CODE39.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |

### getFixCheckDigit() {#getFixCheckDigit--}
```
public boolean getFixCheckDigit()
```


Gets whether to fix the check digit if it\\u2019s invalid.

**Returns:**
boolean - Whether to fix the check digit if it\\u2019s invalid.
### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean-}
```
public void setFixCheckDigit(boolean value)
```


Sets whether to fix the check digit if it\\u2019s invalid.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to fix the check digit if it\\u2019s invalid. |

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
