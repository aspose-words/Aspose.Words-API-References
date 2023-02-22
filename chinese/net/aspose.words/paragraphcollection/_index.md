---
title: Class ParagraphCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.ParagraphCollection 班级. 提供对集合的类型化访问Paragraph节点.
type: docs
weight: 4170
url: /zh/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

提供对集合的类型化访问[`Paragraph`](../paragraph/)节点.

```csharp
public class ParagraphCollection : NodeCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | 获取集合中的节点数。 |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | 检索一个 **段落**在给定的索引处。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | 将一个节点添加到集合的末尾。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中删除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | 确定一个节点是否在集合中。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | 在节点集合上提供简单的“foreach”样式迭代。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | 将一个节点插入到集合中指定索引处。 |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | 从集合和文档中删除节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | 从集合和文档中删除指定索引处的节点。 |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | 将集合中的所有段落复制到新的段落数组中。 (2 methods) |

### 例子

显示如何检查段落是否为移动修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// 此文档包含“移动”修订，当我们用光标突出显示文本时，它会出现，
// 然后拖动它以将其移动到另一个位置
// 同时通过“审阅”跟踪 Microsoft Word 中的修订 -> “跟踪变化”。
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// 移动修订由成对的“Move from”和“Move to”修订组成。 
// 这些修订是对文档的潜在更改，我们可以接受或拒绝。
// 在我们接受/拒绝移动修订之前，文档
// 必须跟踪文本的出发地和到达地。
// 第二段和第四段定义了一个这样的修订，因此两者具有相同的内容。
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// “Move from” 修订版是我们从中拖动文本的段落。
// 如果我们接受修改，这一段会消失，
// 另一个将保留并且不再是修订版。
Assert.True(paragraphs[1].IsMoveFromRevision);

// “移动到”修订版是我们将文本拖到的段落。
// 如果我们拒绝修订，则此段落将消失，而其他段落将保留。
Assert.True(paragraphs[3].IsMoveToRevision);
```

### 也可以看看

* class [NodeCollection](../nodecollection/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


