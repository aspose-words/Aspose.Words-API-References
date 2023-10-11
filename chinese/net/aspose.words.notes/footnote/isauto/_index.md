---
title: Footnote.IsAuto
second_title: Aspose.Words for .NET API 参考
description: Footnote 财产. 保存一个值指定这是自动编号的脚注还是带有用户定义的自定义引用标记的 脚注
type: docs
weight: 30
url: /zh/net/aspose.words.notes/footnote/isauto/
---
## Footnote.IsAuto property

保存一个值，指定这是自动编号的脚注还是带有用户定义的自定义引用标记的 脚注。

```csharp
public bool IsAuto { get; set; }
```

### 评论

[`ReferenceMark`](../referencemark/)用空字符串初始化 if`IsAuto`设置`错误的`.

### 例子

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

* class [Footnote](../)
* 命名空间 [Aspose.Words.Notes](../../footnote/)
* 部件 [Aspose.Words](../../../)


