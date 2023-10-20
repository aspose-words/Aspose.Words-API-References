---
title: Paragraph.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph IsInsertRevision 财产. 如果在启用更改跟踪时将此对象插入 Microsoft Word则返回 true 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

```csharp
public bool IsInsertRevision { get; }
```

## 例子

显示如何使用修订段落。

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// 以上段落不是修订。
// 我们在开始修订跟踪后添加的段落将注册为“插入”修订。
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// 我们在开始修订跟踪后删除的段落将注册为“删除”修订。
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// 这样的段落将一直保留，直到我们接受或拒绝删除修订。
// 接受修订将永久删除该段落，
// 拒绝修订会将其留在文档中，就好像我们从未删除它一样。
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// 接受修订，然后验证段落是否消失。
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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
