---
title: PlainTextDocument
second_title: Aspose.Words for Java API Reference
description: 允许提取文档内容的纯文本表示。
type: docs
weight: 465
url: /zh/java/com.aspose.words/plaintextdocument/
---

**遗产:**
java.lang.Object
```
public class PlainTextDocument
```

允许提取文档内容的纯文本表示。

要了解更多信息，请访问**Working with Text Document**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [PlainTextDocument(String fileName)](#PlainTextDocument-java.lang.String-) | 从文件创建纯文本文档。 |
| [PlainTextDocument(String fileName, LoadOptions loadOptions)](#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions-) | 从文件创建纯文本文档。 |
| [PlainTextDocument(InputStream stream)](#PlainTextDocument-java.io.InputStream-) | 初始化此类的新实例。 |
| [PlainTextDocument(InputStream stream, LoadOptions loadOptions)](#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties--) | 获取[getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument\#getBuiltInDocumentProperties--)的文件。 |
| [get班级()](#get班级--) |  |
| [getCustomDocumentProperties()](#getCustomDocumentProperties--) | 获取[getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument\#getCustomDocumentProperties--)的文件。 |
| [getText()](#getText--) | 获取连接为字符串的文档的文本内容。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PlainTextDocument(String fileName) {#PlainTextDocument-java.lang.String-}
```
public PlainTextDocument(String fileName)
```


从文件创建纯文本文档。自动检测文件格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 要从中提取文本的文件的名称。 |

### PlainTextDocument(String fileName, LoadOptions loadOptions) {#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions-}
```
public PlainTextDocument(String fileName, LoadOptions loadOptions)
```


从文件创建纯文本文档。允许指定其他选项，例如加密密码。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 要从中提取文本的文件的名称。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) | 加载文档时使用的其他选项。可以为空。 |

### PlainTextDocument(InputStream stream) {#PlainTextDocument-java.io.InputStream-}
```
public PlainTextDocument(InputStream stream)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### PlainTextDocument(InputStream stream, LoadOptions loadOptions) {#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions-}
```
public PlainTextDocument(InputStream stream, LoadOptions loadOptions)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) |  |

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
### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties--}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


获取[getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument\#getBuiltInDocumentProperties--)的文件。

**退货:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) -\{[getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument\#getBuiltInDocumentProperties--)的文件。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCustomDocumentProperties() {#getCustomDocumentProperties--}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


获取[getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument\#getCustomDocumentProperties--)的文件。

**退货:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) -\{[getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument\#getCustomDocumentProperties--)的文件。
### getText() {#getText--}
```
public String getText()
```


获取连接为字符串的文档的文本内容。

**退货:**
java.lang.String - 连接为字符串的文档的文本内容。
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
