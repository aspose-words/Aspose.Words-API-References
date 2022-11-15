---
title: NodeImporter
second_title: Aspose.Words for Java API 参考
description: 允许有效地执行节点从一个文档到另一个文档的重复导入。
type: docs
weight: 405
url: /zh/java/com.aspose.words/nodeimporter/
---

**遗产：**
java.lang.Object
```
public class NodeImporter
```

允许有效地执行节点从一个文档到另一个文档的重复导入。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

Aspose.Words 提供了在 Microsoft Word 文档之间轻松复制和移动片段的功能。这被称为“导入节点”。在将一个文档的片段插入另一个文档之前，您需要“导入”它。导入创建原始节点的深层克隆，准备插入到目标文档中。

导入节点的最简单方法是使用[DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-)提供的方法[DocumentBase](../../com.aspose.words/documentbase)目的。

但是，当您需要多次将节点从一个文档导入另一个文档时，最好使用[NodeImporter](../../com.aspose.words/nodeimporter)班级。这[NodeImporter](../../com.aspose.words/nodeimporter)class 允许最小化在目标文档中创建的样式和列表的数量。

将片段从一个 Microsoft Word 文档复制或移动到另一个文档对 Aspose.Words 提出了许多技术挑战。在 Word 文档中，样式和列表格式集中存储，与文档的文本分开。段落和文本运行仅通过内部唯一标识符引用样式。

挑战来自不同文档中的样式和列表不同的事实。例如，要将使用 Heading 1 样式格式化的段落从一个文档复制到另一个文档，必须考虑一些事情：决定是否将 Heading 1 样式从源文档复制到目标文档，克隆段落，更新克隆的段落，使其引用目标文档中正确的标题 1 样式。如果必须复制样式，则应分析它引用的所有样式（基于样式和下一段样式）并可能也复制等等。复制项目符号或编号段落时也存在类似问题，因为 Microsoft Word 将列表定义与文本分开存储。

这[NodeImporter](../../com.aspose.words/nodeimporter)类就像一个上下文，在导入期间保存“翻译表”。它在源文档和目标文档中的样式和列表之间正确转换。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-) | 初始化此类的新实例。 |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean-) | 将节点从一个文档导入到另一个文档。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions-}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

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
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean-}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


将节点从一个文档导入到另一个文档。

导入节点会创建属于导入文档的源节点的副本。返回的节点没有父节点。源节点未更改或从原始文档中删除。

在将来自另一个文档的节点插入到该文档之前，必须导入它。在导入过程中，特定于文档的属性（例如对样式和列表的引用）将从原始文档转换为导入文档。节点导入后，可以使用插入到文档中的适当位置[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-)或者[CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

如果源节点已经属于目标文档，则只需创建源节点的深度克隆。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | 要导入的节点。 |
| isImportChildren | boolean | True 递归导入所有子节点；否则，假的。 |

**退货：**
[Node](../../com.aspose.words/node) 克隆的导入节点。该节点属于目标文档，但没有父节点。
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
