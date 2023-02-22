---
title: Footnote.FootnoteType
second_title: Aspose.Words for .NET API 参考
description: Footnote 财产. 返回一个值该值指定这是脚注还是尾注
type: docs
weight: 20
url: /zh/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

返回一个值，该值指定这是脚注还是尾注。

```csharp
public FootnoteType FootnoteType { get; }
```

### 例子

显示脚注和尾注之间的区别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种将编号引用附加到文本的方法。这两个参考将添加一个
// 我们插入它们的位置的小上标参考标记。
// 引用标记，默认是文档中所有引用中引用的索引号。
// 每个引用也将创建一个条目，该条目将具有与正文中相同的引用标记
// 和参考文本，我们将把它传递给文档构建器的“InsertFootnote”方法。
// 1 - 脚注，其条目将与其引用的文本出现在同一页面上：
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - 一个尾注，其条目将出现在文档的末尾：
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
* 命名空间 [Aspose.Words.Notes](../../footnote/)
* 部件 [Aspose.Words](../../../)


