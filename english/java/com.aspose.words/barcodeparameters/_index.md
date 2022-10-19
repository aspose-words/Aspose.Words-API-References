---
title: BarcodeParameters
second_title: Aspose.Words for Java API Reference
description: Container class for barcode parameters to pass-through to BarcodeGenerator.
type: docs
weight: 26
url: /java/com.aspose.words/barcodeparameters/
---

**Inheritance:**
java.lang.Object
```
public class BarcodeParameters
```

Container class for barcode parameters to pass-through to BarcodeGenerator.

To learn more, visit the **Working with Fields** documentation article.

The set of parameters are according to DISPLAYBARCODE field options. See the exact list at [ ][Link 1]


[Link 1]: https://msdn.microsoft.com/en-us/library/hh745901%28v=office.12%29.aspx
## Methods

| Method | Description |
| --- | --- |
| [getBarcodeType()](#getBarcodeType--) | Bar code type. |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String-) | Bar code type. |
| [getBarcodeValue()](#getBarcodeValue--) | Data to be encoded. |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String-) | Data to be encoded. |
| [getSymbolHeight()](#getSymbolHeight--) | Bar code image height (in twips - 1/1440 inches) |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String-) | Bar code image height (in twips - 1/1440 inches) |
| [getForegroundColor()](#getForegroundColor--) | Bar code foreground color (0x000000 - 0xFFFFFF) |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String-) | Bar code foreground color (0x000000 - 0xFFFFFF) |
| [getBackgroundColor()](#getBackgroundColor--) | Bar code background color (0x000000 - 0xFFFFFF) |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String-) | Bar code background color (0x000000 - 0xFFFFFF) |
| [getSymbolRotation()](#getSymbolRotation--) | Rotation of the barcode symbol. |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String-) | Rotation of the barcode symbol. |
| [getScalingFactor()](#getScalingFactor--) | Scaling factor for the symbol. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String-) | Scaling factor for the symbol. |
| [getPosCodeStyle()](#getPosCodeStyle--) | Style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String-) | Style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). |
| [getCaseCodeStyle()](#getCaseCodeStyle--) | Style of a Case Code for barcode type ITF14. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String-) | Style of a Case Code for barcode type ITF14. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel--) | Error correction level of QR Code. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String-) | Error correction level of QR Code. |
| [getDisplayText()](#getDisplayText--) | Whether to display barcode data (text) along with image. |
| [setDisplayText(boolean value)](#setDisplayText-boolean-) | Whether to display barcode data (text) along with image. |
| [getAddStartStopChar()](#getAddStartStopChar--) | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean-) | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [getFixCheckDigit()](#getFixCheckDigit--) | Whether to fix the check digit if it\\u2019s invalid. |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean-) | Whether to fix the check digit if it\\u2019s invalid. |
| [getPostalAddress()](#getPostalAddress--) | Barcode postal address. |
| [setPostalAddress(String value)](#setPostalAddress-java.lang.String-) | Barcode postal address. |
| [isBookmark()](#isBookmark--) | Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is the name of a bookmark. |
| [isBookmark(boolean value)](#isBookmark-boolean-) | Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is the name of a bookmark. |
| [getFacingIdentificationMark()](#getFacingIdentificationMark--) | Type of a Facing Identification Mark (FIM). |
| [setFacingIdentificationMark(String value)](#setFacingIdentificationMark-java.lang.String-) | Type of a Facing Identification Mark (FIM). |
| [isUSPostalAddress()](#isUSPostalAddress--) | Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is a U.S. |
| [isUSPostalAddress(boolean value)](#isUSPostalAddress-boolean-) | Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is a U.S. |
### getBarcodeType() {#getBarcodeType--}
```
public String getBarcodeType()
```


Bar code type.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setBarcodeType(String value) {#setBarcodeType-java.lang.String-}
```
public void setBarcodeType(String value)
```


Bar code type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getBarcodeValue() {#getBarcodeValue--}
```
public String getBarcodeValue()
```


Data to be encoded.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String-}
```
public void setBarcodeValue(String value)
```


Data to be encoded.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getSymbolHeight() {#getSymbolHeight--}
```
public String getSymbolHeight()
```


Bar code image height (in twips - 1/1440 inches)

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String-}
```
public void setSymbolHeight(String value)
```


Bar code image height (in twips - 1/1440 inches)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getForegroundColor() {#getForegroundColor--}
```
public String getForegroundColor()
```


Bar code foreground color (0x000000 - 0xFFFFFF)

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setForegroundColor(String value) {#setForegroundColor-java.lang.String-}
```
public void setForegroundColor(String value)
```


Bar code foreground color (0x000000 - 0xFFFFFF)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getBackgroundColor() {#getBackgroundColor--}
```
public String getBackgroundColor()
```


Bar code background color (0x000000 - 0xFFFFFF)

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String-}
```
public void setBackgroundColor(String value)
```


Bar code background color (0x000000 - 0xFFFFFF)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getSymbolRotation() {#getSymbolRotation--}
```
public String getSymbolRotation()
```


Rotation of the barcode symbol. Valid values are [0, 3].

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String-}
```
public void setSymbolRotation(String value)
```


Rotation of the barcode symbol. Valid values are [0, 3].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getScalingFactor() {#getScalingFactor--}
```
public String getScalingFactor()
```


Scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000].

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setScalingFactor(String value) {#setScalingFactor-java.lang.String-}
```
public void setScalingFactor(String value)
```


Scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getPosCodeStyle() {#getPosCodeStyle--}
```
public String getPosCodeStyle()
```


Style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String-}
```
public void setPosCodeStyle(String value)
```


Style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getCaseCodeStyle() {#getCaseCodeStyle--}
```
public String getCaseCodeStyle()
```


Style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String-}
```
public void setCaseCodeStyle(String value)
```


Style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getErrorCorrectionLevel() {#getErrorCorrectionLevel--}
```
public String getErrorCorrectionLevel()
```


Error correction level of QR Code. Valid values are [0, 3].

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String-}
```
public void setErrorCorrectionLevel(String value)
```


Error correction level of QR Code. Valid values are [0, 3].

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getDisplayText() {#getDisplayText--}
```
public boolean getDisplayText()
```


Whether to display barcode data (text) along with image.

**Returns:**
boolean - The corresponding  boolean  value.
### setDisplayText(boolean value) {#setDisplayText-boolean-}
```
public void setDisplayText(boolean value)
```


Whether to display barcode data (text) along with image.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAddStartStopChar() {#getAddStartStopChar--}
```
public boolean getAddStartStopChar()
```


Whether to add Start/Stop characters for barcode types NW7 and CODE39.

**Returns:**
boolean - The corresponding  boolean  value.
### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean-}
```
public void setAddStartStopChar(boolean value)
```


Whether to add Start/Stop characters for barcode types NW7 and CODE39.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFixCheckDigit() {#getFixCheckDigit--}
```
public boolean getFixCheckDigit()
```


Whether to fix the check digit if it\\u2019s invalid.

**Returns:**
boolean - The corresponding  boolean  value.
### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean-}
```
public void setFixCheckDigit(boolean value)
```


Whether to fix the check digit if it\\u2019s invalid.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getPostalAddress() {#getPostalAddress--}
```
public String getPostalAddress()
```


Barcode postal address.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setPostalAddress(String value) {#setPostalAddress-java.lang.String-}
```
public void setPostalAddress(String value)
```


Barcode postal address.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### isBookmark() {#isBookmark--}
```
public boolean isBookmark()
```


Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is the name of a bookmark.

**Returns:**
boolean - The corresponding  boolean  value.
### isBookmark(boolean value) {#isBookmark-boolean-}
```
public void isBookmark(boolean value)
```


Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is the name of a bookmark.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFacingIdentificationMark() {#getFacingIdentificationMark--}
```
public String getFacingIdentificationMark()
```


Type of a Facing Identification Mark (FIM).

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setFacingIdentificationMark(String value) {#setFacingIdentificationMark-java.lang.String-}
```
public void setFacingIdentificationMark(String value)
```


Type of a Facing Identification Mark (FIM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### isUSPostalAddress() {#isUSPostalAddress--}
```
public boolean isUSPostalAddress()
```


Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is a U.S. postal address.

**Returns:**
boolean - The corresponding  boolean  value.
### isUSPostalAddress(boolean value) {#isUSPostalAddress-boolean-}
```
public void isUSPostalAddress(boolean value)
```


Whether [getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) is a U.S. postal address.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

