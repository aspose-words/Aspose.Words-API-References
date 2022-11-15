---
title: HeightRule
second_title: Aspose.Words for Java API 参考
description: 指定确定对象高度的规则。
type: docs
weight: 319
url: /zh/java/com.aspose.words/heightrule/
---

**遗产:**
java.lang.Object
```
public class HeightRule
```

指定确定对象高度的规则。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | 高度将至少是指定的高度（以磅为单位）。 |
| [AUTO](#AUTO) | 高度将自动增加以容纳对象内的所有文本。 |
| [EXACTLY](#EXACTLY) | 高度以磅为单位精确指定。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String heightRuleName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int heightRule)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int heightRule)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


高度将至少是指定的高度（以磅为单位）。如果需要，它将增长以容纳对象内的所有文本。

### AUTO {#AUTO}
```
public static int AUTO
```


高度将自动增加以容纳对象内的所有文本。

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


高度以磅为单位精确指定。请注意，如果文本无法容纳在此高度的对象内，它将被截断。

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
### fromName(String heightRuleName) {#fromName-java.lang.String-}
```
public static int fromName(String heightRuleName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int heightRule) {#getName-int-}
```
public static String getName(int heightRule)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| heightRule | int |  |

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
### toString(int heightRule) {#toString-int-}
```
public static String toString(int heightRule)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| heightRule | int |  |

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
