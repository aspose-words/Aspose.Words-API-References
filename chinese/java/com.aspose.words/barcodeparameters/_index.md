---
title: BarcodeParameters
second_title: Aspose.Words for Java API 参考
description: 用于传递给 BarcodeGenerator 的条形码参数的容器类。
type: docs
weight: 26
url: /zh/java/com.aspose.words/barcodeparameters/
---

**遗产：**
java.lang.Object
```
public class BarcodeParameters
```

用于传递给 BarcodeGenerator 的条形码参数的容器类。

要了解更多信息，请访问**Working with Fields**文档文章。

参数集根据 DISPLAYBARCODE 字段选项。请参阅确切的列表[ ][Link 1]


[Link 1]: https://msdn.microsoft.com/en-us/library/hh745901%28v=office.12%29.aspx
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAddStartStopChar()](#getAddStartStopChar--) | 是否为条码类型 NW7 和 CODE39 添加起始/终止字符。 |
| [getBackgroundColor()](#getBackgroundColor--) | 条形码背景颜色（0x000000 - 0xFFFFFF） |
| [getBarcodeType()](#getBarcodeType--) | 条形码类型。 |
| [getBarcodeValue()](#getBarcodeValue--) | 要编码的数据。 |
| [getCaseCodeStyle()](#getCaseCodeStyle--) | 条形码类型 ITF14 的案例代码样式。 |
| [getClass()](#getClass--) |  |
| [getDisplayText()](#getDisplayText--) | 是否与图像一起显示条形码数据（文本）。 |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel--) | QR 码纠错级别。 |
| [getFacingIdentificationMark()](#getFacingIdentificationMark--) | 表面识别标记 (FIM) 的类型。 |
| [getFixCheckDigit()](#getFixCheckDigit--) | 是否修复校验位\\u2019s 无效。 |
| [getForegroundColor()](#getForegroundColor--) | 条码前景色（0x000000 - 0xFFFFFF） |
| [getPosCodeStyle()](#getPosCodeStyle--) | 销售点条码样式（条码类型 UPCA|UPCE|EAN13|EAN8). |
| [getPostalAddress()](#getPostalAddress--) | 条形码邮政地址。 |
| [getScalingFactor()](#getScalingFactor--) | 符号的比例因子。 |
| [getSymbolHeight()](#getSymbolHeight--) | 条码图像高度（缇 - 1/1440 英寸） |
| [getSymbolRotation()](#getSymbolRotation--) | 条形码符号的旋转。 |
| [hashCode()](#hashCode--) |  |
| [isBookmark()](#isBookmark--) | 无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是书签的名称。 |
| [isBookmark(boolean value)](#isBookmark-boolean-) | 无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是书签的名称。 |
| [isUSPostalAddress()](#isUSPostalAddress--) | 无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是美国 |
| [isUSPostalAddress(boolean value)](#isUSPostalAddress-boolean-) | 无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是美国 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean-) | 是否为条码类型 NW7 和 CODE39 添加起始/终止字符。 |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String-) | 条形码背景颜色（0x000000 - 0xFFFFFF） |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String-) | 条形码类型。 |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String-) | 要编码的数据。 |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String-) | 条形码类型 ITF14 的案例代码样式。 |
| [setDisplayText(boolean value)](#setDisplayText-boolean-) | 是否与图像一起显示条形码数据（文本）。 |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String-) | QR 码纠错级别。 |
| [setFacingIdentificationMark(String value)](#setFacingIdentificationMark-java.lang.String-) | 表面识别标记 (FIM) 的类型。 |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean-) | 是否修复校验位\\u2019s 无效。 |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String-) | 条码前景色（0x000000 - 0xFFFFFF） |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String-) | 销售点条码样式（条码类型 UPCA|UPCE|EAN13|EAN8). |
| [setPostalAddress(String value)](#setPostalAddress-java.lang.String-) | 条形码邮政地址。 |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String-) | 符号的比例因子。 |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String-) | 条码图像高度（缇 - 1/1440 英寸） |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String-) | 条形码符号的旋转。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getAddStartStopChar() {#getAddStartStopChar--}
```
public boolean getAddStartStopChar()
```


是否为条码类型 NW7 和 CODE39 添加起始/终止字符。

**退货：**
boolean - 相应的布尔值。
### getBackgroundColor() {#getBackgroundColor--}
```
public String getBackgroundColor()
```


条形码背景颜色（0x000000 - 0xFFFFFF）

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getBarcodeType() {#getBarcodeType--}
```
public String getBarcodeType()
```


条形码类型。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getBarcodeValue() {#getBarcodeValue--}
```
public String getBarcodeValue()
```


要编码的数据。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getCaseCodeStyle() {#getCaseCodeStyle--}
```
public String getCaseCodeStyle()
```


条形码类型 ITF14 的案例代码样式。有效值为[性病|EXT|ADD]

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDisplayText() {#getDisplayText--}
```
public boolean getDisplayText()
```


是否与图像一起显示条形码数据（文本）。

**退货：**
boolean - 相应的布尔值。
### getErrorCorrectionLevel() {#getErrorCorrectionLevel--}
```
public String getErrorCorrectionLevel()
```


QR 码纠错级别。有效值为[0, 3]。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getFacingIdentificationMark() {#getFacingIdentificationMark--}
```
public String getFacingIdentificationMark()
```


表面识别标记 (FIM) 的类型。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getFixCheckDigit() {#getFixCheckDigit--}
```
public boolean getFixCheckDigit()
```


是否修复校验位\\u2019s 无效。

**退货：**
boolean - 相应的布尔值。
### getForegroundColor() {#getForegroundColor--}
```
public String getForegroundColor()
```


条码前景色（0x000000 - 0xFFFFFF）

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getPosCodeStyle() {#getPosCodeStyle--}
```
public String getPosCodeStyle()
```


销售点条码样式（条码类型 UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getPostalAddress() {#getPostalAddress--}
```
public String getPostalAddress()
```


条形码邮政地址。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getScalingFactor() {#getScalingFactor--}
```
public String getScalingFactor()
```


符号的比例因子。该值为整数百分比，有效值为[10, 1000]。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getSymbolHeight() {#getSymbolHeight--}
```
public String getSymbolHeight()
```


条码图像高度（缇 - 1/1440 英寸）

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getSymbolRotation() {#getSymbolRotation--}
```
public String getSymbolRotation()
```


条形码符号的旋转。有效值为[0, 3]。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isBookmark() {#isBookmark--}
```
public boolean isBookmark()
```


无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是书签的名称。

**退货：**
boolean - 相应的布尔值。
### isBookmark(boolean value) {#isBookmark-boolean-}
```
public void isBookmark(boolean value)
```


无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是书签的名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### isUSPostalAddress() {#isUSPostalAddress--}
```
public boolean isUSPostalAddress()
```


无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是美国邮政地址。

**退货：**
boolean - 相应的布尔值。
### isUSPostalAddress(boolean value) {#isUSPostalAddress-boolean-}
```
public void isUSPostalAddress(boolean value)
```


无论[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-)是美国邮政地址。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean-}
```
public void setAddStartStopChar(boolean value)
```


是否为条码类型 NW7 和 CODE39 添加起始/终止字符。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String-}
```
public void setBackgroundColor(String value)
```


条形码背景颜色（0x000000 - 0xFFFFFF）

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String-}
```
public void setBarcodeType(String value)
```


条形码类型。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String-}
```
public void setBarcodeValue(String value)
```


要编码的数据。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String-}
```
public void setCaseCodeStyle(String value)
```


条形码类型 ITF14 的案例代码样式。有效值为[性病|EXT|ADD]

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setDisplayText(boolean value) {#setDisplayText-boolean-}
```
public void setDisplayText(boolean value)
```


是否与图像一起显示条形码数据（文本）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String-}
```
public void setErrorCorrectionLevel(String value)
```


QR 码纠错级别。有效值为[0, 3]。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setFacingIdentificationMark(String value) {#setFacingIdentificationMark-java.lang.String-}
```
public void setFacingIdentificationMark(String value)
```


表面识别标记 (FIM) 的类型。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean-}
```
public void setFixCheckDigit(boolean value)
```


是否修复校验位\\u2019s 无效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String-}
```
public void setForegroundColor(String value)
```


条码前景色（0x000000 - 0xFFFFFF）

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String-}
```
public void setPosCodeStyle(String value)
```


销售点条码样式（条码类型 UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setPostalAddress(String value) {#setPostalAddress-java.lang.String-}
```
public void setPostalAddress(String value)
```


条形码邮政地址。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String-}
```
public void setScalingFactor(String value)
```


符号的比例因子。该值为整数百分比，有效值为[10, 1000]。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String-}
```
public void setSymbolHeight(String value)
```


条码图像高度（缇 - 1/1440 英寸）

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String-}
```
public void setSymbolRotation(String value)
```


条形码符号的旋转。有效值为[0, 3]。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
