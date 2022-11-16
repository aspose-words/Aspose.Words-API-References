---
title: AxisDisplayUnit
second_title: Aspose.Words for Java API 参考
description: 提供对值轴显示单位的缩放选项的访问。
type: docs
weight: 20
url: /zh/java/com.aspose.words/axisdisplayunit/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class AxisDisplayUnit implements Cloneable
```

提供对值轴显示单位的缩放选项的访问。

要了解更多信息，请访问**Working with Charts**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCustomUnit()](#getCustomUnit--) | 获取用户定义的除数以缩放值轴上的显示单位。 |
| [getDocument()](#getDocument--) | 返回标题持有者所属的文档。 |
| [getTitle()](#getTitle--) |  |
| [getTitleDeleted()](#getTitleDeleted--) |  |
| [getTitlePosition()](#getTitlePosition--) |  |
| [getUnit()](#getUnit--) | 获取显示单位的缩放值作为预定义值之一。 |
| [hashCode()](#hashCode--) |  |
| [isVisible()](#isVisible--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCustomUnit(double value)](#setCustomUnit-double-) | 设置用户定义的除数以缩放值轴上的显示单位。 |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle-) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean-) |  |
| [setUnit(int value)](#setUnit-int-) | 将显示单位的缩放值设置为预定义值之一。 |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getCustomUnit() {#getCustomUnit--}
```
public double getCustomUnit()
```


获取用户定义的除数以缩放值轴上的显示单位。

MS Office 2016 新图表不支持该属性。默认值为 1。

设置此属性会设置[getUnit()](../../com.aspose.words/axisdisplayunit\#getUnit--) / [setUnit(int)](../../com.aspose.words/axisdisplayunit\#setUnit-int-)财产[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM).

**退货：**
double - 用户定义的除数，用于在值轴上缩放显示单位。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


返回标题持有者所属的文档。

**退货：**
[DocumentBase](../../com.aspose.words/documentbase) - 所有权人所属的文件。
### getTitle() {#getTitle--}
```
public ChartTitle getTitle()
```




**退货：**
[ChartTitle](../../com.aspose.words/charttitle)
### getTitleDeleted() {#getTitleDeleted--}
```
public boolean getTitleDeleted()
```




**退货：**
布尔值
### getTitlePosition() {#getTitlePosition--}
```
public int getTitlePosition()
```




**退货：**
整数
### getUnit() {#getUnit--}
```
public int getUnit()
```


获取显示单位的缩放值作为预定义值之一。默认值为[AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit\#NONE).这[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM)和[AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit\#PERCENTAGE)值在某些图表类型中不可用；看[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit)了解更多信息。

**退货：**
 int - 作为预定义值之一的显示单位的缩放值。返回值是其中之一[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isVisible() {#isVisible--}
```
public boolean isVisible()
```




**退货：**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCustomUnit(double value) {#setCustomUnit-double-}
```
public void setCustomUnit(double value)
```


设置用户定义的除数以缩放值轴上的显示单位。

MS Office 2016 新图表不支持该属性。默认值为 1。

设置此属性会设置[getUnit()](../../com.aspose.words/axisdisplayunit\#getUnit--) / [setUnit(int)](../../com.aspose.words/axisdisplayunit\#setUnit-int-)财产[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 用户定义的除数，用于在值轴上缩放显示单位。 |

### setTitle(ChartTitle value) {#setTitle-com.aspose.words.ChartTitle-}
```
public void setTitle(ChartTitle value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [ChartTitle](../../com.aspose.words/charttitle) |  |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean-}
```
public void setTitleDeleted(boolean value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setUnit(int value) {#setUnit-int-}
```
public void setUnit(int value)
```


将显示单位的缩放值设置为预定义值之一。默认值为[AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit\#NONE).这[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM)和[AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit\#PERCENTAGE)值在某些图表类型中不可用；看[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit)了解更多信息。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 显示单元的缩放值作为预定义值之一。该值必须是其中之一[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit)常数。 |

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
