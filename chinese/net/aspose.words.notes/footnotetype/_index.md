---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Notes.FootnoteType 枚举. 指定这是脚注还是尾注 在 C#.
type: docs
weight: 4300
url: /zh/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

指定这是脚注还是尾注。

```csharp
public enum FootnoteType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Footnote | `0` | 该对象是脚注。 |
| Endnote | `1` | 该对象是尾注。 |

## 评论

脚注和尾注均由对象表示Footnote 类。使用[`FootnoteType`](../footnote/footnotetype/)区分脚注 和尾注。

## 例子

演示如何使用脚注和尾注引用文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一些文本并用脚注标记它，IsAuto 属性默认设置为“true”，
// 因此正文中看到的标记将自动编号为“1”，
// 脚注将出现在页面底部。
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// 插入更多文本并使用带有自定义引用标记的尾注进行标记，
// 将用来代替数字“2”并将“IsAuto”设置为 false。
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// 脚注总是出现在其引用文本的底部，
// 所以这个分页符不会影响脚注。
// 另一方面，尾注总是位于文档的末尾
// 这样分页符会将尾注推到下一页。
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

演示如何插入和自定义脚注。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加文本，并用脚注引用它。该脚注将放置一个小的上标参考
// 在其引用的文本后面进行标记，并在页面底部的主体文本下方创建一个条目。
// 该条目将包含脚注的参考标记和参考文本，
// 我们将其传递给文档生成器的“InsertFootnote”方法。
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 如果此属性设置为“true”，则脚注的引用标记
// 将成为该节所有脚注中的索引。
// 这是第一个脚注，因此引用标记将为“1”。
Assert.True(footnote.IsAuto);

 // 我们可以将文档构建器移动到脚注内以编辑其参考文本。
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 我们可以设置脚注将使用的自定义引用标记，而不是其索引号。
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// 将“IsAuto”标志设置为 true 的书签仍将显示其真实索引
// 即使以前的书签显示自定义引用标记，因此该书签的引用标记将为“3”。
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
