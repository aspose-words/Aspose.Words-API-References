---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words for .NET
description: 使用 Story LastParagraph 属性轻松访问故事的最后一段，增强叙述管理和编辑体验。
type: docs
weight: 20
url: /zh/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

获取故事的最后一段。

```csharp
public Paragraph LastParagraph { get; }
```

## 例子

展示如何将 DocumentBuilder 的光标位置移动到指定节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// 文档构建器有一个游标，它充当文档的一部分
// 当我们使用其文档构造方法时，构建器会附加新节点。
// 此光标的功能与 Microsoft Word 的闪烁光标相同，
// 并且它也总是在构建器刚刚插入的任何节点之后立即结束。
// 要将内容附加到文档的不同部分，
// 我们可以使用“MoveTo”方法将光标移动到不同的节点。
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// 光标现在位于我们将其移动到的节点前面。
// 添加第二个运行将会把它插入到第一个运行的前面。
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// 将光标移动到文档末尾，像之前一样继续将文本附加到末尾。
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### 也可以看看

* class [Paragraph](../../paragraph/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
