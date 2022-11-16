---
title: ContinuousSectionRestart
second_title: Aspose.Words for Java API 参考
description: 表示在重新开始页码的连续部分中计算页码时的不同行为。
type: docs
weight: 93
url: /zh/java/com.aspose.words/continuoussectionrestart/
---

**遗产：**
java.lang.Object
```
public class ContinuousSectionRestart
```

表示在重新开始页码的连续部分中计算页码时的不同行为。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ALWAYS](#ALWAYS) | 无论内容流如何，页码总是重新开始。 |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | 仅当该部分开始的页面上的部分之前没有其他内容时，页码才会重新开始。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int continuousSectionRestart)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int continuousSectionRestart)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


无论内容流如何，页码总是重新开始。除 Word 2016 外，所有 MS Word 版本均展示了此行为。

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


仅当该部分开始的页面上的部分之前没有其他内容时，页码才会重新开始。该行为由 MS Word 2016 演示。

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
### fromName(String continuousSectionRestartName) {#fromName-java.lang.String-}
```
public static int fromName(String continuousSectionRestartName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int continuousSectionRestart) {#getName-int-}
```
public static String getName(int continuousSectionRestart)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| continuousSectionRestart | int |  |

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
### toString(int continuousSectionRestart) {#toString-int-}
```
public static String toString(int continuousSectionRestart)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| continuousSectionRestart | int |  |

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
