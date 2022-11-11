---
title: VbaReference类型
second_title: Aspose.Words for Java API 参考
description:允许指定对象的类型。
type: docs
weight: 599
url: /zh/java/com.aspose.words/vbareferencetype/
---

**遗产:**
java.lang.Object
```
public class VbaReference类型
```

允许指定类型[VbaReference](../../com.aspose.words/vbareference)目的。
## 字段

| 字段 | 描述 |
| --- | --- |
| [CONTROL](#CONTROL) | 指定一个旋转类型库引用类型。 |
| [ORIGINAL](#ORIGINAL) | 指定原始自动化类型库引用类型。 |
| [PROJECT](#PROJECT) | 指定了外部 VBA 项目引用类型。 |
| [REGISTERED](#REGISTERED) | 指定自动化类型库引用类型。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String vbaReference类型Name)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int vbaReference类型)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int vbaReference类型)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CONTROL {#CONTROL}
```
public static int CONTROL
```


指定一个旋转类型库引用类型。该类型对应于 2.3.4.2.2.3 REFERENCECONTROL 的记录[MS-OVBA]：https://docs.microsoft.com/en-us/openspecs/office\_文件\_formats/ms-ovba/d64485fa-8562-4726-9c5e-11e8f01a81c0

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


指定原始自动化类型库引用类型。此类型对应于 2.3.4.2.2.4 REFERENCEORIGINAL 记录[MS-OVBA]：https://docs.microsoft.com/en-us/openspecs/office\_文件\_formats/ms-ovba/3ba66994-8c7a-4634-b2da-f9331ace6686

### PROJECT {#PROJECT}
```
public static int PROJECT
```


指定了外部 VBA 项目引用类型。该类型对应 2.3.4.2.2.6 REFERENCEPROJECT 的记录[MS-OVBA]：https://docs.microsoft.com/en-us/openspecs/office\_文件\_formats/ms-ovba/08280eb0-d628-495c-867f-5985ed020142

### REGISTERED {#REGISTERED}
```
public static int REGISTERED
```


指定自动化类型库引用类型。该类型对应于 2.3.4.2.2.5 REFERENCEREGISTERED 的记录[MS-OVBA]：https://docs.microsoft.com/en-us/openspecs/office\_文件\_formats/ms-ovba/6c39388e-96f5-4b93-b90a-ae625a063fcf

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
### fromName(String vbaReference类型Name) {#fromName-java.lang.String-}
```
public static int fromName(String vbaReference类型Name)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| vbaReference类型Name | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int vbaReference类型) {#getName-int-}
```
public static String getName(int vbaReference类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| vbaReference类型 | int |  |

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
### toString(int vbaReference类型) {#toString-int-}
```
public static String toString(int vbaReference类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| vbaReference类型 | int |  |

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
