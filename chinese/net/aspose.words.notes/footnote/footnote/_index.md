---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words for .NET
description: 使用我们的脚注构造器轻松创建引人入胜的脚注。只需点击几下，即可提升内容的清晰度和专业性！
type: docs
weight: 10
url: /zh/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

初始化[`Footnote`](../)类.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |
| footnoteType | FootnoteType | 一个[`FootnoteType`](../footnotetype/) value 指定这是脚注还是尾注。 |

## 评论

什么时候[`Footnote`](../)已创建，它属于指定文档，但尚未成为文档的一部分，并且[`ParentNode`](../../../aspose.words/node/parentnode/)是`无效的`。

附加[`Footnote`](../)文档使用[`InsertAfter`](../../../aspose.words/compositenode/insertafter/)或者[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)在要插入脚注的段落上输入 。

## 例子

展示如何插入和自定义脚注。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加文本，并用脚注引用。此脚注将放置一个小的上标引用
// 在其引用的文本后进行标记，并在页面底部的正文下方创建一个条目。
// 此条目将包含脚注的引用标记和引用文本，
// 我们将把它传递给文档构建器的“InsertFootnote”方法。
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 如果此属性设置为“true”，那么我们的脚注的引用标记
// 将成为该部分所有脚注中的索引。
// 这是第一个脚注，因此引用标记将为“1”。
Assert.True(footnote.IsAuto);

 // 我们可以将文档构建器移动到脚注内来编辑其参考文本。
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 我们可以设置一个自定义引用标记，脚注将使用它来代替其索引号。
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// 将“IsAuto”标志设置为 true 的书签仍将显示其真实索引
// 即使以前的书签显示自定义引用标记，所以这个书签的引用标记将是“3”。
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### 也可以看看

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
