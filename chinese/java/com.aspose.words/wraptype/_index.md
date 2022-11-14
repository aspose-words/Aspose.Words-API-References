---
title: WrapType
second_title: Aspose.Words for Java API 参考
description: 指定文本如何环绕形状或图片。
type: docs
weight: 622
url: /zh/java/com.aspose.words/wraptype/
---

**遗产:**
java.lang.Object
```
public class WrapType
```

指定文本如何环绕形状或图片。
## 字段

| 场地 | 描述 |
| --- | --- |
| [INLINE](#INLINE) | 形状与文本保持在同一图层上并被视为字符。 |
| [NONE](#NONE) | 形状周围没有环绕文字。 |
| [SQUARE](#SQUARE) | 将文本环绕在形状的方形边界框的所有边上。 |
| [THROUGH](#THROUGH) | 与 Tight 相同，但包裹在打开的形状的任何部分内。 |
| [TIGHT](#TIGHT) | 紧紧围绕形状的边缘，而不是围绕边界框。 |
| [TOP_BOTTOM](#TOP-BOTTOM) | 文本停在形状的顶部并在形状下方的线上重新开始。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String wrapTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int wrapType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int wrapType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


形状与文本保持在同一图层上并被视为字符。

### NONE {#NONE}
```
public static int NONE
```


没有文字环绕形状。形状放在文本的后面或前面。

### SQUARE {#SQUARE}
```
public static int SQUARE
```


将文本环绕在形状的方形边界框的所有边上。

### THROUGH {#THROUGH}
```
public static int THROUGH
```


与 Tight 相同，但包裹在打开的形状的任何部分内。

### TIGHT {#TIGHT}
```
public static int TIGHT
```


紧紧围绕形状的边缘，而不是围绕边界框。

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


文本停在形状的顶部并在形状下方的线上重新开始。

### length {#length}
```
public static int length
```


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
### fromName(String wrapTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String wrapTypeName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int wrapType) {#getName-int-}
```
public static String getName(int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| wrapType | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
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




**退货:**
java.lang.String
### toString(int wrapType) {#toString-int-}
```
public static String toString(int wrapType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| wrapType | int |  |

**退货:**
java.lang.String
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
