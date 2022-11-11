---
title: ResourceLoadingAction
second_title: Aspose.Words for Java API 参考
description: 指定资源加载的模式。
type: docs
weight: 479
url: /zh/java/com.aspose.words/resourceloadingaction/
---

**遗产:**
java.lang.Object
```
public class ResourceLoadingAction
```

指定资源加载的模式。

要了解更多信息，请访问**Specify Load Options**文档文章。
## 字段

| 字段 | 描述 |
| --- | --- |
| [DEFAULT](#DEFAULT) | Aspose.Words 会像往常一样加载这个资源。 |
| [SKIP](#SKIP) | Aspose.Words 将跳过此资源的加载。 |
| [USER_PROVIDED](#USER-PROVIDED) |  Aspose.Words 将使用用户提供的字节数组[ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs\#setData-byte---)作为资源数据。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String resourceLoadingActionName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int resourceLoadingAction)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int resourceLoadingAction)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aspose.Words 会像往常一样加载这个资源。

### SKIP {#SKIP}
```
public static int SKIP
```


Aspose.Words 将跳过此资源的加载。对于图像，只会存储没有数据的链接，对于 HTML 格式，CSS 样式表将被忽略。

### USER_PROVIDED {#USER-PROVIDED}
```
public static int USER_PROVIDED
```


 Aspose.Words 将使用用户提供的字节数组[ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs\#setData-byte---)作为资源数据。

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
### fromName(String resourceLoadingActionName) {#fromName-java.lang.String-}
```
public static int fromName(String resourceLoadingActionName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| resourceLoadingActionName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int resourceLoadingAction) {#getName-int-}
```
public static String getName(int resourceLoadingAction)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| resourceLoadingAction | int |  |

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
### toString(int resourceLoadingAction) {#toString-int-}
```
public static String toString(int resourceLoadingAction)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| resourceLoadingAction | int |  |

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
