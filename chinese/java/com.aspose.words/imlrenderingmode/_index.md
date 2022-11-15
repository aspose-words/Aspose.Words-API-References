---
title: ImlRenderingMode
second_title: Aspose.Words for Java API 参考
description: 指定墨迹 InkML 对象如何呈现为固定页面格式。
type: docs
weight: 345
url: /zh/java/com.aspose.words/imlrenderingmode/
---

**遗产：**
java.lang.Object
```
public class ImlRenderingMode
```

指定如何将墨迹 (InkML) 对象呈现为固定页面格式。
## 字段

| 场地 | 描述 |
| --- | --- |
| [FALLBACK](#FALLBACK) | 如果后备形状可用于墨水 (InkML) 对象，Aspose.Words 渲染后备形状而不是 InkML。 |
| [INK_ML](#INK-ML) | Aspose.Words 忽略墨水 (InkML) 对象的回退形状并呈现 InkML 本身。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int imlRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int imlRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


如果后备形状可用于墨水 (InkML) 对象，Aspose.Words 渲染后备形状而不是 InkML。请注意，在使用回退呈现模式将文档保存为固定页面格式后，AW 文档模型中的 InkML 对象将永久替换为其回退对应对象。因此，即使 ImlRenderingMode 设置为 InkML，再次保存同一个文档将始终使用回退形状。

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words 忽略墨水 (InkML) 对象的回退形状并呈现 InkML 本身。这是默认模式。

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
### fromName(String imlRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String imlRenderingModeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int imlRenderingMode) {#getName-int-}
```
public static String getName(int imlRenderingMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imlRenderingMode | int |  |

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
### toString(int imlRenderingMode) {#toString-int-}
```
public static String toString(int imlRenderingMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imlRenderingMode | int |  |

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
