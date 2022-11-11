---
title: IHyphenationCallback
second_title: Aspose.Words for Java API 参考
description: 由可以注册连字符字典的类实现。
type: docs
weight: 647
url: /zh/java/com.aspose.words/ihyphenationcallback/
---
```
public interface IHyphenationCallback
```

由可以注册连字符字典的类实现。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [requestDictionary(String language)](#requestDictionary-java.lang.String-) | 通知应用程序未找到指定语言的断字字典，可能需要注册。 |
### requestDictionary(String language) {#requestDictionary-java.lang.String-}
```
public abstract void requestDictionary(String language)
```


通知应用程序未找到指定语言的断字字典，可能需要注册。

实现应该找到一个字典并使用它注册它**M:Aspose.Words.Hyphenation.RegisterDictionary(System.String,System.IO.Stream)**方法。

如果指定语言实现的字典不可用，则可以选择退出对同一语言的进一步调用，使用[Hyphenation.registerDictionary(java.lang.String, java.lang.String)](../../com.aspose.words/hyphenation\#registerDictionary-java.lang.String--java.lang.String-)具有空值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| language | java.lang.String | 语言名称，例如“en-US”。有关详细信息，请参阅 .NET 文档以了解“文化名称”和 RFC 4646。此方法抛出的异常将中止页面布局过程的执行。 |
