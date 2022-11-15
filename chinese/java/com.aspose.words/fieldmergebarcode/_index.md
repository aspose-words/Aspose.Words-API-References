---
title: FieldMergeBarcode
second_title: Aspose.Words for Java API 参考
description: 实现 MERGEBARCODE 字段。
type: docs
weight: 214
url: /zh/java/com.aspose.words/fieldmergebarcode/
---

**遗产:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldMergeBarcode extends Field
```

实现 MERGEBARCODE 字段。

要了解更多信息，请访问**Working with 字段**文档文章。

邮件合并条形码。
## 方法

| 方法 | 描述 |
| --- | --- |
| [canWorkAsMergeField()](#canWorkAsMergeField--) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAddStartStopChar()](#getAddStartStopChar--) | 获取是否为条码类型 NW7 和 CODE39 添加起始/终止字符。 |
| [getBackgroundColor()](#getBackgroundColor--) | 获取条形码符号的背景色。 |
| [getBarcodeType()](#getBarcodeType--) | 获取条码类型（二维码等） |
| [getBarcodeValue()](#getBarcodeValue--) | 获取条形码值。 |
| [getCaseCodeStyle()](#getCaseCodeStyle--) | 获取条码类型 ITF14 的案例代码的样式。 |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | 获取表示显示的字段结果的文本。 |
| [getDisplayText()](#getDisplayText--) | 获取是否与图像一起显示条形码数据（文本）。 |
| [getEnd()](#getEnd--) | 获取表示字段结束的节点。 |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel--) | 获取二维码的纠错级别。 |
| [getFieldCode()](#getFieldCode--) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [getFixCheckDigit()](#getFixCheckDigit--) | 获取是否修复校验位\\u2019s 无效。 |
| [getForegroundColor()](#getForegroundColor--) | 获取条形码符号的前景色。 |
| [getFormat()](#getFormat--) | 得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。 |
| [getLocaleId()](#getLocaleId--) | 获取字段的 LCID。 |
| [getMergeFieldName()](#getMergeFieldName--) |  |
| [getPosCodeStyle()](#getPosCodeStyle--) | 获取销售点条形码的样式（条形码类型 UPCA|UPCE|EAN13|EAN8). |
| [getResult()](#getResult--) | 获取字段分隔符和字段结尾之间的文本。 |
| [getScalingFactor()](#getScalingFactor--) | 获取符号的比例因子。 |
| [getSeparator()](#getSeparator--) | 获取表示字段分隔符的节点。 |
| [getStart()](#getStart--) | 获取表示字段开始的节点。 |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getSymbolHeight()](#getSymbolHeight--) | 获取符号的高度。 |
| [getSymbolRotation()](#getSymbolRotation--) | 获取条形码符号的旋转。 |
| [getType()](#getType--) | 获取 Microsoft Word 字段类型。 |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [isLocked()](#isLocked--) | 获取字段是否被锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置字段是否被锁定（不应重新计算其结果）。 |
| [isMergeValueRequired()](#isMergeValueRequired--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除字段。 |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean-) | 设置是否为条形码类型 NW7 和 CODE39 添加开始/停止字符。 |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String-) | 设置条形码符号的背景颜色。 |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String-) | 设置条码类型（QR 等） |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String-) | 设置条形码值。 |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String-) | 设置条码类型 ITF14 的案例代码的样式。 |
| [setDisplayText(boolean value)](#setDisplayText-boolean-) | 设置是否与图像一起显示条形码数据（文本）。 |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String-) | 设置二维码的纠错级别。 |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean-) | 设置是否固定校验位，如果它\\u2019s 无效。 |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String-) | 设置条形码符号的前景色。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置字段的 LCID。 |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String-) | 设置销售点条码的样式（条码类型 UPCA|UPCE|EAN13|EAN8). |
| [setResult(String value)](#setResult-java.lang.String-) | 设置字段分隔符和字段结尾之间的文本。 |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String-) | 为符号设置比例因子。 |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String-) | 设置符号的高度。 |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String-) | 设置条形码符号的旋转。 |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | 执行字段取消链接。 |
| [update()](#update--) | 执行字段更新。 |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | 执行字段更新。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### canWorkAsMergeField() {#canWorkAsMergeField--}
```
public boolean canWorkAsMergeField()
```




**退货:**
布尔值
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getAddStartStopChar() {#getAddStartStopChar--}
```
public boolean getAddStartStopChar()
```


获取是否为条码类型 NW7 和 CODE39 添加起始/终止字符。

**退货:**
boolean - 是否为条形码类型 NW7 和 CODE39 添加开始/结束字符。
### getBackgroundColor() {#getBackgroundColor--}
```
public String getBackgroundColor()
```


获取条形码符号的背景色。有效值在范围内[0, 0xFFFFFF]

**退货:**
java.lang.String - 条形码符号的背景色。
### getBarcodeType() {#getBarcodeType--}
```
public String getBarcodeType()
```


获取条码类型（二维码等）

**退货:**
java.lang.String - 条形码类型（二维码等）
### getBarcodeValue() {#getBarcodeValue--}
```
public String getBarcodeValue()
```


获取条形码值。

**退货:**
java.lang.String - 条码值。
### getCaseCodeStyle() {#getCaseCodeStyle--}
```
public String getCaseCodeStyle()
```


获取条形码类型 ITF14 的案例代码样式。有效值为[性病|EXT|ADD]

**退货:**
java.lang.String - 条形码类型 ITF14 的 Case 代码样式。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


获取表示显示的字段结果的文本。这[Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--)必须调用方法才能获得正确的值[FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout)和[FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl)字段。

**退货:**
java.lang.String - 表示显示的字段结果的文本。
### getDisplayText() {#getDisplayText--}
```
public boolean getDisplayText()
```


获取是否与图像一起显示条形码数据（文本）。

**退货:**
boolean - 是否与图像一起显示条形码数据（文本）。
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


获取表示字段结束的节点。

**退货:**
[FieldEnd](../../com.aspose.words/fieldend) - 代表字段结束的节点。
### getErrorCorrectionLevel() {#getErrorCorrectionLevel--}
```
public String getErrorCorrectionLevel()
```


获取二维码纠错级别。有效值为[0, 3]。

**退货:**
java.lang.String - QR 码的纠错级别。
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。包含子字段的字段代码和字段结果。

**退货:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ 如果应包含子域代码，则为真。 |

**退货:**
java.lang.String
### getFixCheckDigit() {#getFixCheckDigit--}
```
public boolean getFixCheckDigit()
```


获取是否修复校验位\\u2019s 无效。

**退货:**
boolean - 是否修复校验位\\u2019s 无效。
### getForegroundColor() {#getForegroundColor--}
```
public String getForegroundColor()
```


获取条形码符号的前景色。有效值在范围内[0, 0xFFFFFF]

**退货:**
java.lang.String - 条形码符号的前景色。
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


得到一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。

**退货:**
[FieldFormat](../../com.aspose.words/fieldformat) - 一个[FieldFormat](../../com.aspose.words/fieldformat)提供对字段格式的类型化访问的对象。
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取字段的 LCID。

**退货:**
int - 字段的 LCID。
### getMergeFieldName() {#getMergeFieldName--}
```
public String getMergeFieldName()
```




**退货:**
java.lang.String
### getPosCodeStyle() {#getPosCodeStyle--}
```
public String getPosCodeStyle()
```


获取销售点条形码的样式（条形码类型 UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**退货:**
java.lang.String - 销售点条码的样式（条码类型 UPCA|UPCE|EAN13|EAN8）。
### getResult() {#getResult--}
```
public String getResult()
```


获取字段分隔符和字段结尾之间的文本。

**退货:**
java.lang.String - 字段分隔符和字段结尾之间的文本。
### getScalingFactor() {#getScalingFactor--}
```
public String getScalingFactor()
```


获取符号的比例因子。该值以整数个百分点表示，有效值为[10, 1000]

**退货:**
java.lang.String - 符号的比例因子。
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


获取表示字段分隔符的节点。可以为空。

**退货:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - 表示字段分隔符的节点。
### getStart() {#getStart--}
```
public FieldStart getStart()
```


获取表示字段开始的节点。

**退货:**
[FieldStart](../../com.aspose.words/fieldstart) - 表示字段开始的节点。
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String |  |

**退货:**
整数
### getSymbolHeight() {#getSymbolHeight--}
```
public String getSymbolHeight()
```


获取符号的高度。单位为 TWIPS（1/1440 英寸）。

**退货:**
java.lang.String - 符号的高度。
### getSymbolRotation() {#getSymbolRotation--}
```
public String getSymbolRotation()
```


获取条形码符号的旋转。有效值为[0, 3]

**退货:**
java.lang.String - 条形码符号的旋转。
### getType() {#getType--}
```
public int getType()
```


获取 Microsoft Word 字段类型。

**退货:**
 int - Microsoft Word 字段类型。返回值是以下之一[FieldType](../../com.aspose.words/fieldtype)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isDirty() {#isDirty--}
```
public boolean isDirty()
```


获取字段的当前结果是否由于对文档进行了其他修改而不再正确（陈旧）。

**退货:**
boolean - 由于对文档进行了其他修改，该字段的当前结果是否不再正确（陈旧）。
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 由于对文档进行了其他修改，该字段的当前结果是否不再正确（陈旧）。 |

### isLocked() {#isLocked--}
```
public boolean isLocked()
```


获取字段是否被锁定（不应重新计算其结果）。

**退货:**
boolean - 字段是否被锁定（不应重新计算其结果）。
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


设置字段是否被锁定（不应重新计算其结果）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 该字段是否被锁定（不应重新计算其结果）。 |

### isMergeValueRequired() {#isMergeValueRequired--}
```
public boolean isMergeValueRequired()
```




**退货:**
布尔值
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


从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个子节点，则返回其父段落。如果该字段已被删除，则返回**null**.

**退货:**
[Node](../../com.aspose.words/node)
### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean-}
```
public void setAddStartStopChar(boolean value)
```


设置是否为条形码类型 NW7 和 CODE39 添加开始/停止字符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否为条码类型 NW7 和 CODE39 添加起始/终止字符。 |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String-}
```
public void setBackgroundColor(String value)
```


设置条形码符号的背景颜色。有效值在范围内[0, 0xFFFFFF]

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条形码符号的背景颜色。 |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String-}
```
public void setBarcodeType(String value)
```


设置条码类型（QR 等）

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条码类型（二维码等） |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String-}
```
public void setBarcodeValue(String value)
```


设置条形码值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条形码值。 |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String-}
```
public void setCaseCodeStyle(String value)
```


为条形码类型 ITF14 设置案例代码的样式。有效值为[性病|EXT|ADD]

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条码类型 ITF14 的案例代码的样式。 |

### setDisplayText(boolean value) {#setDisplayText-boolean-}
```
public void setDisplayText(boolean value)
```


设置是否与图像一起显示条形码数据（文本）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否与图像一起显示条形码数据（文本）。 |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String-}
```
public void setErrorCorrectionLevel(String value)
```


设置二维码的纠错级别。有效值为[0, 3]。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 二维码的纠错级别。 |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean-}
```
public void setFixCheckDigit(boolean value)
```


设置是否固定校验位，如果它\\u2019s 无效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否固定校验位\\u2019s 无效。 |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String-}
```
public void setForegroundColor(String value)
```


设置条形码符号的前景色。有效值在范围内[0, 0xFFFFFF]

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条码符号的前景色。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置字段的 LCID。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字段的 LCID。 |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String-}
```
public void setPosCodeStyle(String value)
```


设置销售点条码的样式（条码类型 UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 销售点条形码的样式（条形码类型 UPCA|UPCE|EAN13|EAN8). |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置字段分隔符和字段结尾之间的文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字段分隔符和字段结尾之间的文本。 |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String-}
```
public void setScalingFactor(String value)
```


设置符号的比例因子。该值以整数个百分点表示，有效值为[10, 1000]

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 符号的比例因子。 |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String-}
```
public void setSymbolHeight(String value)
```


设置符号的高度。单位为 TWIPS（1/1440 英寸）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 符号的高度。 |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String-}
```
public void setSymbolRotation(String value)
```


设置条形码符号的旋转。有效值为[0, 3]

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 条形码符号的旋转。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### unlink() {#unlink--}
```
public boolean unlink()
```


执行字段取消链接。

将字段替换为其最新结果。

某些字段，例如 XE（索引条目）字段和 SEQ（序列）字段，无法取消链接。

**退货:**
布尔值 -\{ 如果该字段已取消链接则为真，否则为假。
### update() {#update--}
```
public void update()
```


执行字段更新。如果该字段已经被更新则抛出。

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


执行字段更新。如果该字段已经被更新则抛出。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ignoreMergeFormat | boolean | 如果为真，则放弃直接字段结果格式，不管 MERGEFORMAT 开关如何，否则执行正常更新。 |

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
