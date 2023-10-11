---
title: Paragraph.IsDeleteRevision
second_title: Aspose.Words for .NET API 参考
description: Paragraph 财产. 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象则返回 true
type: docs
weight: 40
url: /zh/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。

```csharp
public bool IsDeleteRevision { get; }
```

### 例子

展示如何使用修订段落。

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// 以上段落并非修订。
// 我们在开始修订跟踪后添加的段落将注册为“插入”修订。
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// 我们在开始修订跟踪后删除的段落将注册为“删除”修订。
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// 此类段落将一直保留，直到我们接受或拒绝删除修订。
// 接受修订将永久删除该段落，
// 拒绝修订会将其保留在文档中，就好像我们从未删除它一样。
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// 接受修改，然后验证该段落是否已消失。
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.That(para, Is.Empty);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### 也可以看看

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


