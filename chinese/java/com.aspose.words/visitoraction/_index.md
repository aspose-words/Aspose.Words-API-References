---
title: VisitorAction
second_title: Aspose.Words for Java API 参考
description: 允许访问者控制节点的枚举。
type: docs
weight: 603
url: /zh/java/com.aspose.words/visitoraction/
---

**遗产:**
java.lang.Object
```
public class VisitorAction
```

允许访问者控制节点的枚举。
## 字段

| 场地 | 描述 |
| --- | --- |
| [CONTINUE](#CONTINUE) | 访问者请求枚举继续。 |
| [SKIP_THIS_NODE](#SKIP-THIS-NODE) | 访问者请求跳过当前节点并继续枚举。 |
| [STOP](#STOP) | 访问者请求停止枚举节点。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String visitorActionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int visitorAction)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int visitorAction)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CONTINUE {#CONTINUE}
```
public static int CONTINUE
```


访问者请求枚举继续。

### SKIP_THIS_NODE {#SKIP-THIS-NODE}
```
public static int SKIP_THIS_NODE
```


访问者请求跳过当前节点并继续枚举。

### STOP {#STOP}
```
public static int STOP
```


访问者请求停止枚举节点。

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
### fromName(String visitorActionName) {#fromName-java.lang.String-}
```
public static int fromName(String visitorActionName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitorActionName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int visitorAction) {#getName-int-}
```
public static String getName(int visitorAction)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitorAction | int |  |

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
### toString(int visitorAction) {#toString-int-}
```
public static String toString(int visitorAction)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitorAction | int |  |

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
