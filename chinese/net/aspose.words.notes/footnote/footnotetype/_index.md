---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words for .NET
description: 发现 FootnoteType 属性，轻松识别文档中的脚注或尾注，以增强清晰度和组织性。
type: docs
weight: 30
url: /zh/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

返回一个值，指定这是脚注还是尾注。

```csharp
public FootnoteType FootnoteType { get; }
```

## 例子

显示脚注和尾注之间的区别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是两种将编号引用附加到文本的方法。这两种引用都会添加
// 我们插入它们的位置的小上标引用标记。
// 引用标记默认是该引用在文档所有引用中的索引号。
// 每个引用也会创建一个条目，该条目将具有与正文中相同的引用标记
// 和参考文本，我们将其传递给文档构建器的“InsertFootnote”方法。
// 1 - 脚注，其条目将与其引用的文本出现在同一页面上：
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - 尾注，其条目将出现在文档末尾：
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### 也可以看看

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
