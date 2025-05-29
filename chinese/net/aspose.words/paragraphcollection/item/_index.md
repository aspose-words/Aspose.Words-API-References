---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 使用 ParagraphCollection Item 属性轻松访问特定段落。通过索引检索任意段落，实现无缝文本管理。
type: docs
weight: 10
url: /zh/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

检索[`Paragraph`](../../paragraph/)在给定的索引处。

```csharp
public Paragraph this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合的索引。 |

## 评论

该索引从零开始。

允许使用负索引，表示从集合的后面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负数并且其绝对值大于列表中的项目数，则返回空引用。

## 例子

展示如何检查某个段落是否为移动修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// 本文档包含“移动”修订，当我们用光标突出显示文本时，这些修订就会出现，
// 然后拖动它以将其移动到另一个位置
// 同时通过“审阅”->“跟踪更改”在 Microsoft Word 中跟踪修订。
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // 移动修订由“移动自”和“移动到”修订对组成。
// 这些修订是文档的潜在更改，我们可以接受或拒绝。
// 在我们接受/拒绝移动修订之前，文档
// 必须跟踪文本的出发和到达目的地。
// 第二段和第四段定义了一个这样的修订，因此两者具有相同的内容。
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// “从中移动”修订版是我们从中拖动文本的段落。
// 如果我们接受修改，此段落将会消失，
// 另一个将保留并且不再是修订版。
Assert.True(paragraphs[1].IsMoveFromRevision);

// “移动到”修订版是我们将文本拖到的段落。
// 如果我们拒绝修改，则此段落将会消失，而另一段落将保留。
Assert.True(paragraphs[3].IsMoveToRevision);
```

### 也可以看看

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
