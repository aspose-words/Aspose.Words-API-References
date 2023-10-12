---
title: Footnote.Footnote
second_title: Aspose.Words for .NET API 参考
description: Footnote 构造函数. 初始化一个实例Footnote类.
type: docs
weight: 10
url: /zh/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

初始化一个实例[`Footnote`](../)类.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |
| footnoteType | FootnoteType | A[`FootnoteType`](../footnotetype/) value 指定这是脚注还是尾注。 |

### 评论

什么时候[`Footnote`](../)创建后，它属于指定文档，但还不是 文档的一部分并且[`ParentNode`](../../../aspose.words/node/parentnode/)是`无效的`。

追加[`Footnote`](../)到文档使用Node)或者Node) 位于要插入脚注的段落上。

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* 命名空间 [Aspose.Words.Notes](../../footnote/)
* 部件 [Aspose.Words](../../../)


