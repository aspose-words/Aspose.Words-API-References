---
title: LineSpacingRule
second_title: Aspose.Words for Java API 参考
description: 指定段落的行距值。
type: docs
weight: 366
url: /zh/java/com.aspose.words/linespacingrule/
---

**遗产：**
java.lang.Object
```
public class LineSpacingRule
```

指定段落的行距值。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | 行间距可以大于或等于，但绝不能小于[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-)财产。 |
| [EXACTLY](#EXACTLY) | 行间距永远不会从中指定的值改变[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-)属性，即使段落中使用了更大的字体。 |
| [MULTIPLE](#MULTIPLE) | 行间距在[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-)属性作为行数。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String lineSpacingRuleName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int lineSpacingRule)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int lineSpacingRule)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


行间距可以大于或等于，但绝不能小于[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-)财产。

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


行间距永远不会从中指定的值改变[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-)属性，即使段落中使用了更大的字体。

### MULTIPLE {#MULTIPLE}
```
public static int MULTIPLE
```


行间距在[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-)属性作为行数。一条线等于 12 个点。

### length {#length}
```
public static int length
```


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
### fromName(String lineSpacingRuleName) {#fromName-java.lang.String-}
```
public static int fromName(String lineSpacingRuleName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| lineSpacingRuleName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int lineSpacingRule) {#getName-int-}
```
public static String getName(int lineSpacingRule)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| lineSpacingRule | int |  |

**退货：**
java.lang.字符串
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货：**
整数[]
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




### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### toString(int lineSpacingRule) {#toString-int-}
```
public static String toString(int lineSpacingRule)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| lineSpacingRule | int |  |

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
