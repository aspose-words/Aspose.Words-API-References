---
title: WarningInfo
second_title: Aspose.Words for Java API 参考
description: 包含有关 Aspose.Words 在文档加载或保存期间发出的警告的信息。
type: docs
weight: 604
url: /zh/java/com.aspose.words/warninginfo/
---

**遗产：**
java.lang.Object
```
public class WarningInfo
```

包含有关 Aspose.Words 在文档加载或保存期间发出的警告的信息。

要了解更多信息，请访问**Programming with Documents**文档文章。

您不创建此类的实例。此类的对象由 Aspose.Words 创建并传递给[IWarningCallback.warning(com.aspose.words.WarningInfo)](../../com.aspose.words/iwarningcallback\#warning-com.aspose.words.WarningInfo-)方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDescription()](#getDescription--) | 返回警告的描述。 |
| [getSource()](#getSource--) | 返回警告的来源。 |
| [getWarningType()](#getWarningType--) | 返回警告的类型。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDescription() {#getDescription--}
```
public String getDescription()
```


返回警告的描述。

**退货：**
java.lang.String - 警告的描述。
### getSource() {#getSource--}
```
public int getSource()
```


返回警告的来源。

**退货：**
 int - 警告的来源。返回值是其中之一[WarningSource](../../com.aspose.words/warningsource)常数。
### getWarningType() {#getWarningType--}
```
public int getWarningType()
```


返回警告的类型。

**退货：**
int - 警告的类型。返回值是按位组合[WarningType](../../com.aspose.words/warningtype)常数。
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
