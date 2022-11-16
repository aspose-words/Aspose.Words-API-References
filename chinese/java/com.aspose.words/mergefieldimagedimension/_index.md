---
title: MergeFieldImageDimension
second_title: Aspose.Words for Java API 参考
description: 表示图像尺寸，即
type: docs
weight: 394
url: /zh/java/com.aspose.words/mergefieldimagedimension/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class MergeFieldImageDimension implements Cloneable
```

表示在邮件合并过程中使用的图像尺寸（即宽度或高度）。

要了解更多信息，请访问**Working with Fields**文档文章。

要指示在邮件合并期间应以其原始尺寸插入图像，您应该为[getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)财产。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [MergeFieldImageDimension(double value)](#MergeFieldImageDimension-double-) | 使用给定的点值创建图像尺寸实例。 |
| [MergeFieldImageDimension(double value, int unit)](#MergeFieldImageDimension-double-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getUnit()](#getUnit--) | 那个单位。 |
| [getValue()](#getValue--) | 价值。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setUnit(int value)](#setUnit-int-) | 那个单位。 |
| [setValue(double value)](#setValue-double-) | 价值。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### MergeFieldImageDimension(double value) {#MergeFieldImageDimension-double-}
```
public MergeFieldImageDimension(double value)
```


使用给定的点值创建图像尺寸实例。您应该使用负值表示应应用相应图像尺寸的原始值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 价值。 |

### MergeFieldImageDimension(double value, int unit) {#MergeFieldImageDimension-double-int-}
```
public MergeFieldImageDimension(double value, int unit)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |
| unit | int |  |

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
### getUnit() {#getUnit--}
```
public int getUnit()
```


那个单位。

**退货：**
int - 相应的 int 值。返回值是其中之一[MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit)常数。
### getValue() {#getValue--}
```
public double getValue()
```


价值。您应该使用负值表示应应用相应图像尺寸的原始值。

**退货：**
double - 相应的双精度值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setUnit(int value) {#setUnit-int-}
```
public void setUnit(int value)
```


那个单位。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit)常数。 |

### setValue(double value) {#setValue-double-}
```
public void setValue(double value)
```


价值。您应该使用负值表示应应用相应图像尺寸的原始值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

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
