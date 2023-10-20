---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphCollection Item 财产. 检索一个段落在给定的索引处 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

检索一个**段落**在给定的索引处。

```csharp
public Paragraph this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合中的索引。 |

## 评论

该索引从零开始。

允许使用负索引并指示从集合的背面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二个，依此类推。

如果 index 大于或等于列表中的项目数，则返回空引用。

如果 index 为负且其绝对值大于列表中的项目数，则返回空引用。

## 例子

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

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
