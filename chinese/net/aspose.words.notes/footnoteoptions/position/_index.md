---
title: FootnoteOptions.Position
second_title: Aspose.Words for .NET API 参考
description: FootnoteOptions 财产. 指定脚注位置
type: docs
weight: 30
url: /zh/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

指定脚注位置。

```csharp
public FootnotePosition Position { get; set; }
```

### 例子

演示如何选择文档收集和显示脚注的不同位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注是一种将引用或旁注附加到文本的方法
// 这不会干扰主体文本的流程。
// 插入脚注会添加一个小上标引用符号
// 在正文文本处插入脚注。
// 每个脚注还在页面底部创建一个条目，由一个符号组成
// 与主体文本中的引用符号相匹配。
// 我们传递给文档构建器的“InsertFootnote”方法的参考文本。
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// 我们可以使用“Position”属性来确定文档放置所有脚注的位置。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BottomOfPage”，
// 每个脚注都会显示在包含其引用标记的页面底部。这是默认值。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BeneathText”，
// 每个脚注都将显示在包含其引用标记的页面文本的末尾。
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### 也可以看看

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* 命名空间 [Aspose.Words.Notes](../../footnoteoptions/)
* 部件 [Aspose.Words](../../../)


