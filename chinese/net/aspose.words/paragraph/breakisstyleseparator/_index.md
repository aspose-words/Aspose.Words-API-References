---
title: Paragraph.BreakIsStyleSeparator
second_title: Aspose.Words for .NET API 参考
description: Paragraph 财产. 如果此段落分隔符是样式分隔符则为 True样式分隔符允许 one 段落由具有不同段落样式的部分组成
type: docs
weight: 20
url: /zh/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

如果此段落分隔符是样式分隔符，则为 True。样式分隔符允许 one 段落由具有不同段落样式的部分组成。

```csharp
public bool BreakIsStyleSeparator { get; }
```

### 例子

演示如何将文本写入与目录标题相同的行，并且使其不显示在目录中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// 插入一个段落，该段落的样式将被目录选择为一个条目。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// 这两个字符串都在同一段落中，因此将显示在同一目录条目中。
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// 如果我们插入样式分隔符，我们可以在同一段落中写入更多文本
// 并使用不同的样式而不显示在目录中。
// 如果我们在分隔符后使用标题类型样式，我们可以从一个文档文本行中绘制多个 TOC 条目。
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### 也可以看看

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


