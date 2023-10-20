---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: 用于 .NET 的 Aspose.Words
description: Footnote ReferenceMark 财产. 获取/设置用于此脚注的自定义参考标记 默认值为空字符串Empty表示使用自动编号的脚注 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

获取/设置用于此脚注的自定义参考标记。 默认值为**空字符串**(Empty)，表示使用自动编号的脚注。

```csharp
public string ReferenceMark { get; set; }
```

## 评论

如果此属性设置为**空字符串**(Empty 或 null，则[`IsAuto`](../isauto/)属性将自动设置为 true， 如果设置为其他任何值，则[`IsAuto`](../isauto/)将设置为 false.

RTF 格式只能存储 1 个符号作为自定义参考标记，因此在导出时只会写入第一个符号，其他符号将被丢弃。

## 例子

显示如何插入和自定义脚注。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加文本，并用脚注引用它。这个脚注将放置一个小的上标参考
// 在它引用的文本之后标记，并在页面底部的主体文本下方创建一个条目。
// 此条目将包含脚注的参考标记和参考文本，
// 我们将传递给文档构建器的“InsertFootnote”方法。
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 如果这个属性设置为“true”，那么我们脚注的引用标记
// 将是它在所有部分脚注中的索引。
// 这是第一个脚注，所以引用标记为“1”。
Assert.True(footnote.IsAuto);

// 我们可以在脚注中移动文档构建器来编辑其参考文本。 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 我们可以设置一个自定义引用标记，脚注将使用它而不是它的索引号。
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// 将“IsAuto”标志设置为 true 的书签仍将显示其真实索引
// 即使以前的书签显示自定义参考标记，所以这个书签的参考标记将是“3”。
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### 也可以看看

* class [Footnote](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
