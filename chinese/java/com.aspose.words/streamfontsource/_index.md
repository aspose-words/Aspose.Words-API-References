---
title: StreamFontSource
second_title: Aspose.Words for Java API 参考
description: 用户定义的流字体源的基类。
type: docs
weight: 530
url: /zh/java/com.aspose.words/streamfontsource/
---

**遗产:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public abstract class StreamFontSource extends FontSourceBase
```

用户定义的流字体源的基类。

要了解更多信息，请访问**Working with Fonts**文档文章。

为了使用流字体源，您应该从[StreamFontSource](../../com.aspose.words/streamfontsource)并提供实施[openFontDataStream()](../../com.aspose.words/streamfontsource\#openFontDataStream--)方法。

[openFontDataStream()](../../com.aspose.words/streamfontsource\#openFontDataStream--)方法可以多次调用。当 Aspose.Words 扫描提供的字体源以获取可用字体列表时，将首次调用它。如果在文档中使用字体来解析字体数据并将字体数据嵌入到某些输出格式中，则稍后可能会调用它。

[StreamFontSource](../../com.aspose.words/streamfontsource)可能很有用，因为它允许仅在需要时加载字体数据，而不是将其存储在内存中以供[FontSettings](../../com.aspose.words/fontsettings)寿命。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | 返回通过此源可用的字体列表。 |
| [getCacheKey()](#getCacheKey--) | 此源在缓存中的键。 |
| [getCacheKeyInternal()](#getCacheKeyInternal--) |  |
| [getClass()](#getClass--) |  |
| [getFilePath()](#getFilePath--) |  |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | 返回字体源优先级。 |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getSize()](#getSize--) |  |
| [getType()](#getType--) | 返回字体源的类型。 |
| [getWarningCallback()](#getWarningCallback--) | 当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [openFontDataStream()](#openFontDataStream--) | 此方法应按需打开带有字体数据的流。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | 当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。 |
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
### getCacheKey() {#getCacheKey--}
```
public String getCacheKey()
```


此源在缓存中的键。当使用 和 方法保存/加载字体搜索缓存时，此键用于识别缓存项。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getCacheKeyInternal() {#getCacheKeyInternal--}
```
public String getCacheKeyInternal()
```




**退货:**
java.lang.String
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getFilePath() {#getFilePath--}
```
public String getFilePath()
```




**退货:**
java.lang.String
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

当不同字体源中存在具有相同家族名称和样式的字体时，使用此值。在这种情况下，Aspose.Words 从具有更高优先级值的源中选择字体。

默认值为 0。

**退货:**
int - 字体源优先级。
### getPriorityInternal() {#getPriorityInternal--}
```
public int getPriorityInternal()
```




**退货:**
整数
### getSize() {#getSize--}
```
public int getSize()
```




**退货:**
整数
### getType() {#getType--}
```
public int getType()
```


返回字体源的类型。

**退货:**
 int - 字体源的类型。返回值是以下之一[FontSourceType](../../com.aspose.words/fontsourcetype)常数。
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。

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




### openFontDataStream() {#openFontDataStream--}
```
public abstract InputStream openFontDataStream()
```


此方法应按需打开带有字体数据的流。

**退货:**
java.io.InputStream - 字体数据流。读取后将关闭流。无需明确关闭它。
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。

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
