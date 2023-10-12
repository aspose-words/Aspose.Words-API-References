---
title: Class SubDocument
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.SubDocument 班级. 代表一个 子文档 这是对外部存储文档的引用
type: docs
weight: 6170
url: /zh/net/aspose.words/subdocument/
---
## SubDocument class

代表一个 **子文档** 这是对外部存储文档的引用。

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class SubDocument : Node
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果该节点可以包含其他节点. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words/subdocument/nodetype/) { get; } | 返回SubDocument. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../range/)表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept/)(DocumentVisitor) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | 获取指定对象类型的第一个祖先。 |
| virtual [GetText](../../aspose.words/node/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | 根据先序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | 使用指定的保存选项将节点的内容导出到字符串中。 |

### 评论

在此版本的 Aspose.Words 中，`SubDocument`节点不提供公共methods 和属性来创建或修改子文档。在此版本中，您无法实例化 `SubDocument`节点或修改现有节点，但删除它们除外。

`SubDocument`只能是一个孩子[`Paragraph`](../paragraph/)。

### 例子

演示如何访问主文档的子文档。

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// 该节点作为外部文档的引用，其内容无法访问。
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### 也可以看看

* class [Node](../node/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


