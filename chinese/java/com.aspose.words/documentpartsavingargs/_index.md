---
title: DocumentPartSavingArgs
second_title: Aspose.Words for Java API 参考
description: 为回调提供数据。
type: docs
weight: 125
url: /zh/java/com.aspose.words/documentpartsavingargs/
---

**遗产：**
java.lang.Object
```
public class DocumentPartSavingArgs
```

提供数据[IDocumentPartSavingCallback.documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../../com.aspose.words/idocumentpartsavingcallback\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-)打回来。

要了解更多信息，请访问**Save a Document**文档文章。

当 Aspose.Words 将文档保存为 HTML 或相关格式并且[HtmlSaveOptions.getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [HtmlSaveOptions.setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-)指定时，文档被拆分成多个部分，默认情况下，每个文档部分都保存到一个单独的文件中。

班级[DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs)允许您控制每个文档部分的保存方式。它允许重新定义文件名的生成方式，或者通过提供您自己的流对象来完全避免将文档部分保存到文件中。

要将文档部分保存到流而不是文件中，请使用**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | 获取正在保存的文档对象。 |
| [getDocumentPartFileName()](#getDocumentPartFileName--) | 获取文档部分将保存到的文件名（不带路径）。 |
| [getDocumentPartStream()](#getDocumentPartStream--) |  |
| [getKeepDocumentPartStreamOpen()](#getKeepDocumentPartStreamOpen--) | 指定 Aspose.Words 是否应该在保存文档部分后保持流打开或关闭它。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDocumentPartFileName(String value)](#setDocumentPartFileName-java.lang.String-) | 设置文档部分将保存到的文件名（无路径）。 |
| [setDocumentPartStream(OutputStream value)](#setDocumentPartStream-java.io.OutputStream-) |  |
| [setKeepDocumentPartStreamOpen(boolean value)](#setKeepDocumentPartStreamOpen-boolean-) | 指定 Aspose.Words 是否应该在保存文档部分后保持流打开或关闭它。 |
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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取正在保存的文档对象。

**退货：**
[Document](../../com.aspose.words/document) - 正在保存的文档对象。
### getDocumentPartFileName() {#getDocumentPartFileName--}
```
public String getDocumentPartFileName()
```


获取文档部分将保存到的文件名（不带路径）。

此属性允许您重新定义文档部分文件名在导出为 HTML 或 EPUB 期间的生成方式。

调用回调时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将文档部分保存到不同的文件中。请注意，每个部分的文件名必须是唯一的。

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs\#getDocumentPartFileName--) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs\#setDocumentPartFileName-java.lang.String-)必须只包含没有路径的文件名。 Aspose.Words 使用文档文件名确定保存路径。如果未指定输出文档文件名，例如在保存到流时，此文件名仅用于引用文档部分。保存为 EPUB 格式时也是如此。

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**退货：**
java.lang.String - 文档部分将保存到的文件名（不带路径）。
### getDocumentPartStream() {#getDocumentPartStream--}
```
public OutputStream getDocumentPartStream()
```




**退货：**
java.io.OutputStream
### getKeepDocumentPartStreamOpen() {#getKeepDocumentPartStreamOpen--}
```
public boolean getKeepDocumentPartStreamOpen()
```


指定 Aspose.Words 是否应该在保存文档部分后保持流打开或关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**将文档部分写入其中后的属性。指定 true 以保持流打开。请注意，调用中提供的主要输出流**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**或者**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)**永远不会被 Aspose.Words 关闭，即使[getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs\#getKeepDocumentPartStreamOpen--) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs\#setKeepDocumentPartStreamOpen-boolean-)设置为 false 。

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**退货：**
boolean - 相应的布尔值。
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




### setDocumentPartFileName(String value) {#setDocumentPartFileName-java.lang.String-}
```
public void setDocumentPartFileName(String value)
```


设置文档部分将保存到的文件名（无路径）。

此属性允许您重新定义文档部分文件名在导出为 HTML 或 EPUB 期间的生成方式。

调用回调时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将文档部分保存到不同的文件中。请注意，每个部分的文件名必须是唯一的。

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs\#getDocumentPartFileName--) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs\#setDocumentPartFileName-java.lang.String-)必须只包含没有路径的文件名。 Aspose.Words 使用文档文件名确定保存路径。如果未指定输出文档文件名，例如在保存到流时，此文件名仅用于引用文档部分。保存为 EPUB 格式时也是如此。

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档部分将保存到的文件名（不带路径）。 |

### setDocumentPartStream(OutputStream value) {#setDocumentPartStream-java.io.OutputStream-}
```
public void setDocumentPartStream(OutputStream value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepDocumentPartStreamOpen(boolean value) {#setKeepDocumentPartStreamOpen-boolean-}
```
public void setKeepDocumentPartStreamOpen(boolean value)
```


指定 Aspose.Words 是否应该在保存文档部分后保持流打开或关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**将文档部分写入其中后的属性。指定 true 以保持流打开。请注意，调用中提供的主要输出流**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**或者**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)**永远不会被 Aspose.Words 关闭，即使[getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs\#getKeepDocumentPartStreamOpen--) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs\#setKeepDocumentPartStreamOpen-boolean-)设置为 false 。

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
