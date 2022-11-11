---
title: VbaReference
second_title: Aspose.Words for Java API Reference
description: 实现对自动化类型库或 VBA 项目的引用。
type: docs
weight: 597
url: /zh/java/com.aspose.words/vbareference/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public abstract class VbaReference implements Cloneable
```

实现对自动化类型库或 VBA 项目的引用。

要了解更多信息，请访问**Working with VBA Macros**文档文章。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [VbaReference()](#VbaReference--) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getLibId()](#getLibId--) | 获取一个包含自动化类型库标识符的字符串值。 |
| [get类型()](#get类型--) | 获取[VbaReference类型](../../com.aspose.words/vbareferencetype)指示 VbaReference 对象表示的引用类型的对象。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### VbaReference() {#VbaReference--}
```
public VbaReference()
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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getLibId() {#getLibId--}
```
public abstract String getLibId()
```


获取一个包含自动化类型库标识符的字符串值。根据引用类型，此属性的值可以是：

 *  在 2.1.1.8 LibidReference 中指定的 LibidReference[MS-OVBA]：https://docs.microsoft.com/en-us/openspecs/office\_文件\_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
 *  在 2.1.1.12 ProjectReference 中指定的 ProjectReference[MS-OVBA]：https://docs.microsoft.com/en-us/openspecs/office\_文件\_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

**退货:**
java.lang.String - 一个包含自动化类型库标识符的字符串值。
### get类型() {#get类型--}
```
public abstract int get类型()
```


获取[VbaReference类型](../../com.aspose.words/vbareferencetype)指示 VbaReference 对象表示的引用类型的对象。

**退货:**
诠释 -\{[VbaReference类型](../../com.aspose.words/vbareferencetype)指示 VbaReference 对象表示的引用类型的对象。返回值是以下之一[VbaReference类型](../../com.aspose.words/vbareferencetype)常数。
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
