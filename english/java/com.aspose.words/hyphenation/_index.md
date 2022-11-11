---
title: Hyphenation
second_title: Aspose.Words for Java API 参考
description: 提供使用连字字典的方法。
type: docs
weight: 333
url: /zh/java/com.aspose.words/hyphenation/
---

**遗产:**
java.lang.Object
```
public class Hyphenation
```

提供使用连字字典的方法。这些字典规定了特定语言的单词可以在何处连字。

要了解更多信息，请访问**Working with Hyphenation**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCallback()](#getCallback--) | 获取构建文档页面布局时用于请求字典的回调接口。 |
| [get班级()](#get班级--) |  |
| [getWarningCallback()](#getWarningCallback--) | 在加载断字模式期间调用，当检测到可能导致格式保真度丢失的问题时。 |
| [hashCode()](#hashCode--) |  |
| [isDictionaryRegistered(String language)](#isDictionaryRegistered-java.lang.String-) | 如果指定的语言没有注册字典或注册为 Null 字典，则返回 False，否则返回 True。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [registerDictionary(String language, InputStream stream)](#registerDictionary-java.lang.String-java.io.InputStream-) |  |
| [registerDictionary(String language, String fileName)](#registerDictionary-java.lang.String-java.lang.String-) | 从文件中注册并加载指定语言的断字字典。 |
| [setCallback(IHyphenationCallback value)](#setCallback-com.aspose.words.IHyphenationCallback-) | 设置构建文档页面布局时用于请求字典的回调接口。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | 在加载断字模式期间调用，当检测到可能导致格式保真度丢失的问题时。 |
| [toString()](#toString--) |  |
| [unregisterDictionary(String language)](#unregisterDictionary-java.lang.String-) | 取消注册指定语言的断字字典。 |
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
### getCallback() {#getCallback--}
```
public static IHyphenationCallback getCallback()
```


获取构建文档页面布局时用于请求字典的回调接口。这允许延迟加载字典，这在处理多种语言的文档时可能很有用。

**退货:**
[IHyphenationCallback](../../com.aspose.words/ihyphenationcallback) - 构建文档页面布局时用于请求字典的回调接口。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getWarningCallback() {#getWarningCallback--}
```
public static IWarningCallback getWarningCallback()
```


在加载断字模式期间调用，当检测到可能导致格式保真度丢失的问题时。

**退货:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isDictionaryRegistered(String language) {#isDictionaryRegistered-java.lang.String-}
```
public static boolean isDictionaryRegistered(String language)
```


如果指定的语言没有注册字典或注册为 Null 字典，则返回 False，否则返回 True。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | java.lang.String |  |

**退货:**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### registerDictionary(String language, InputStream stream) {#registerDictionary-java.lang.String-java.io.InputStream-}
```
public static void registerDictionary(String language, InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | java.lang.String |  |
| stream | java.io.InputStream |  |

### registerDictionary(String language, String fileName) {#registerDictionary-java.lang.String-java.lang.String-}
```
public static void registerDictionary(String language, String fileName)
```


从文件中注册并加载指定语言的断字字典。如果字典无法读取或格式无效，则抛出。

该方法也可用于注册 Null 字典以防止[getCallback()](../../com.aspose.words/hyphenation\#getCallback--) / [setCallback(com.aspose.words.IHyphenationCallback)](../../com.aspose.words/hyphenation\#setCallback-com.aspose.words.IHyphenationCallback-)免于因同一种语言而被反复调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | java.lang.String | 语言名称，例如“en-US”。有关详细信息，请参阅 .NET 文档以了解“文化名称”和 RFC 4646。 |
| fileName | java.lang.String | Open Office 格式的字典文件的路径。

如果此参数为 null 或空字符串，则注册为 Null 字典，并且不再为此语言调用回调。

要再次启用回调，请使用[unregisterDictionary(java.lang.String)](../../com.aspose.words/hyphenation\#unregisterDictionary-java.lang.String-)方法。|

### setCallback(IHyphenationCallback value) {#setCallback-com.aspose.words.IHyphenationCallback-}
```
public static void setCallback(IHyphenationCallback value)
```


设置构建文档页面布局时用于请求字典的回调接口。这允许延迟加载字典，这在处理多种语言的文档时可能很有用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IHyphenationCallback](../../com.aspose.words/ihyphenationcallback) | 构建文档页面布局时用于请求字典的回调接口。 |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public static void setWarningCallback(IWarningCallback value)
```


在加载断字模式期间调用，当检测到可能导致格式保真度丢失的问题时。

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
### unregisterDictionary(String language) {#unregisterDictionary-java.lang.String-}
```
public static void unregisterDictionary(String language)
```


取消注册指定语言的断字字典。

这与注册 Null 字典不同。取消注册字典会启用指定语言的回调。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | java.lang.String | 语言名称，例如“en-US”。有关详细信息，请参阅 .NET 文档以了解“文化名称”和 RFC 4646。

如果为 null 或空字符串，则所有字典都未注册。|

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
