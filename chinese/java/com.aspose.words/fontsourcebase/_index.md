---
title: FontSourceBase
second_title: Aspose.Words for Java API Reference
description: 这是允许用户指定各种字体源的类的抽象基类。
type: docs
weight: 287
url: /zh/java/com.aspose.words/fontsourcebase/
---

**遗产:**
java.lang.Object
```
public abstract class FontSourceBase
```

这是允许用户指定各种字体源的类的抽象基类。

要了解更多信息，请访问**Working with Fonts**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | 返回通过此源可用的字体列表。 |
| [get班级()](#get班级--) |  |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | 返回字体源优先级。 |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [get类型()](#get类型--) | 返回字体源的类型。 |
| [getWarningCallback()](#getWarningCallback--) | 当检测到可能导致格式保真度丢失的问题时，在处理字体源期间调用。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | 当检测到可能导致格式保真度丢失的问题时，在处理字体源期间调用。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getAvailableFonts() {#getAvailableFonts--}
```
public ArrayList getAvailableFonts()
```


返回通过此源可用的字体列表。

**退货:**
java.util.ArrayList
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**退货:**
java.lang.Iterable
### getPriority() {#getPriority--}
```
public int getPriority()
```


返回字体源优先级。

当不同字体源中存在具有相同系列名称和样式的字体时使用此值。在这种情况下，Aspose.Words 从源中选择具有较高优先级值的字体。

默认值为 0。

**退货:**
int - 字体源优先级。
### getPriorityInternal() {#getPriorityInternal--}
```
public int getPriorityInternal()
```




**退货:**
整数
### get类型() {#get类型--}
```
public abstract int get类型()
```


返回字体源的类型。

**退货:**
 int - 字体源的类型。返回值是以下之一[FontSource类型](../../com.aspose.words/fontsourcetype)常数。
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


当检测到可能导致格式保真度丢失的问题时，在处理字体源期间调用。

**退货:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。
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




### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


当检测到可能导致格式保真度丢失的问题时，在处理字体源期间调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。 |

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
