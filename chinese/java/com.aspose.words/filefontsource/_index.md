---
title: FileFontSource
second_title: Aspose.Words for Java API 参考
description: 表示存储在文件系统中的单个 TrueType 字体文件。
type: docs
weight: 264
url: /zh/java/com.aspose.words/filefontsource/
---

**遗产：**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class FileFontSource extends FontSourceBase
```

表示存储在文件系统中的单个 TrueType 字体文件。

要了解更多信息，请访问**Working with Fonts**文档文章。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [FileFontSource(String filePath)](#FileFontSource-java.lang.String-) | 克托尔。 |
| [FileFontSource(String filePath, int priority)](#FileFontSource-java.lang.String-int-) | 克托尔。 |
| [FileFontSource(String filePath, int priority, String cacheKey)](#FileFontSource-java.lang.String-int-java.lang.String-) | 克托尔。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | 返回通过此源可用的字体列表。 |
| [getCacheKey()](#getCacheKey--) | 此源在缓存中的键。 |
| [getClass()](#getClass--) |  |
| [getFilePath()](#getFilePath--) | 字体文件的路径。 |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | 返回字体源优先级。 |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getType()](#getType--) | 返回字体源的类型。 |
| [getWarningCallback()](#getWarningCallback--) | 当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | 当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FileFontSource(String filePath) {#FileFontSource-java.lang.String-}
```
public FileFontSource(String filePath)
```


克托尔。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| filePath | java.lang.String | 字体文件的路径。 |

### FileFontSource(String filePath, int priority) {#FileFontSource-java.lang.String-int-}
```
public FileFontSource(String filePath, int priority)
```


克托尔。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| filePath | java.lang.String | 字体文件的路径。 |
| priority | int | 字体来源优先。见[FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--)属性描述以获取更多信息。 |

### FileFontSource(String filePath, int priority, String cacheKey) {#FileFontSource-java.lang.String-int-java.lang.String-}
```
public FileFontSource(String filePath, int priority, String cacheKey)
```


克托尔。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| filePath | java.lang.String | 字体文件的路径。 |
| priority | int | 字体来源优先。见[FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--)属性描述以获取更多信息。 |
| cacheKey | java.lang.String | 此源在缓存中的键。看[getCacheKey()](../../com.aspose.words/filefontsource\#getCacheKey--)属性描述以获取更多信息。 |

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
### getAvailableFonts() {#getAvailableFonts--}
```
public ArrayList getAvailableFonts()
```


返回通过此源可用的字体列表。

**退货：**
java.util.ArrayList
### getCacheKey() {#getCacheKey--}
```
public String getCacheKey()
```


此源在缓存中的键。

当使用 和 方法保存/加载字体搜索缓存时，此键用于识别缓存项。

如果未指定密钥，则[getFilePath()](../../com.aspose.words/filefontsource\#getFilePath--)将用作密钥。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getFilePath() {#getFilePath--}
```
public String getFilePath()
```


字体文件的路径。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**退货：**
java.lang.Iterable
### getPriority() {#getPriority--}
```
public int getPriority()
```


返回字体源优先级。

当不同字体源中存在具有相同家族名称和样式的字体时，使用此值。在这种情况下，Aspose.Words 从具有更高优先级值的源中选择字体。

默认值为 0。

**退货：**
int - 字体源优先级。
### getPriorityInternal() {#getPriorityInternal--}
```
public int getPriorityInternal()
```




**退货：**
整数
### getType() {#getType--}
```
public int getType()
```


返回字体源的类型。

**退货：**
 int - 字体源的类型。返回值是其中之一[FontSourceType](../../com.aspose.words/fontsourcetype)常数。
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。

**退货：**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。
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




### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


当检测到可能导致格式保真度损失的问题时，在处理字体源期间调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。 |

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
