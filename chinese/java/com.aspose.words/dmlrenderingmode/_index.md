---
title: DmlRenderingMode
second_title: Aspose.Words for Java API 参考
description: 指定如何将 DrawingML 形状呈现为固定页面格式。
type: docs
weight: 118
url: /zh/java/com.aspose.words/dmlrenderingmode/
---

**遗产：**
java.lang.Object
```
public class DmlRenderingMode
```

指定如何将 DrawingML 形状呈现为固定页面格式。
## 字段

| 场地 | 描述 |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words 忽略 DrawingML 的后备形状并呈现 DrawingML 本身。 |
| [FALLBACK](#FALLBACK) | 如果回退形状可用于 DrawingML，Aspose.Words 渲染回退形状而不是 DrawingML。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int dmlRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int dmlRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words 忽略 DrawingML 的后备形状并呈现 DrawingML 本身。这是默认模式。

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


如果回退形状可用于 DrawingML，Aspose.Words 渲染回退形状而不是 DrawingML。请注意，在使用回退 DML 呈现模式将文档保存为固定页面格式后，AW 文档模型中的 DML 形状将永久替换为其回退对应物。因此，即使 DmlRenderingMode 设置为 DrawingML，再次保存同一个文档将始终使用后备形状。

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
### fromName(String dmlRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String dmlRenderingModeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int dmlRenderingMode) {#getName-int-}
```
public static String getName(int dmlRenderingMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dmlRenderingMode | int |  |

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
### toString(int dmlRenderingMode) {#toString-int-}
```
public static String toString(int dmlRenderingMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dmlRenderingMode | int |  |

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
