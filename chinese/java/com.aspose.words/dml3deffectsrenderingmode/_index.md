---
title: Dml3DEffectsRenderingMode
second_title: Aspose.Words for Java API 参考
description:指定如何渲染 3D 形状效果。
type: docs
weight: 116
url: /zh/java/com.aspose.words/dml3deffectsrenderingmode/
---

**遗产:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

指定如何渲染 3D 形状效果。
## 字段

| 字段 | 描述 |
| --- | --- |
| [ADVANCED](#ADVANCED) | 渲染扩展的特殊效果列表，包括高级 3D 效果，例如斜面、照明和材质。 |
| [BASIC](#BASIC) | 轻量级且稳定的渲染，基于内部引擎，但在使用此模式时不显示高级效果，如照明、材质和其他附加效果。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


渲染扩展的特殊效果列表，包括高级 3D 效果，例如斜面、照明和材质。当前的实现使用 OpenGL。使用前请确保您的系统上安装了 OpenGL 库版本 1.1 或更高版本。这个模式还在开发中，可能有些东西不支持，推荐使用[BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC)如果渲染结果不可接受，则为模式。有关详细信息，请参阅文档。

### BASIC {#BASIC}
```
public static int BASIC
```


轻量级且稳定的渲染，基于内部引擎，但在使用此模式时不显示高级效果，如照明、材质和其他附加效果。有关详细信息，请参阅文档。

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
### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int dml3DEffectsRenderingMode) {#getName-int-}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

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
### toString(int dml3DEffectsRenderingMode) {#toString-int-}
```
public static String toString(int dml3DEffectsRenderingMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

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
