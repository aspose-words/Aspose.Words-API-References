---
title: OutlineOptions.HeadingsOutlineLevels
linktitle: HeadingsOutlineLevels
articleTitle: HeadingsOutlineLevels
second_title: 用于 .NET 的 Aspose.Words
description: OutlineOptions HeadingsOutlineLevels 财产. 指定要包含在 文档大纲中的标题级别使用标题样式格式化的段落 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

指定要包含在 文档大纲中的标题级别（使用标题样式格式化的段落）。

```csharp
public int HeadingsOutlineLevels { get; set; }
```

## 评论

指定 0 表示大纲中没有标题；为大纲中的一级标题指定 1，依此类推。

默认值为 0。有效范围为 0 到 9。

## 例子

演示如何将整个文档转换为具有文档大纲三个级别的 PDF。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入 1 至 5 级标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是列出文档正文中的标题的目录。
// 单击此大纲中的条目将带我们到达其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“4”，以从大纲中排除级别高于 4 的所有标题。
options.OutlineOptions.HeadingsOutlineLevels = 4;

// 如果大纲条目在其自身和相同或较低级别的下一个条目之间有更高级别的后续条目，
// 条目左侧将出现一个箭头。该条目是多个此类“子条目”的“所有者”。
// 在我们的文档中，第 5 级标题级别的大纲条目是第二个第 4 级大纲条目的子条目，
// 第 4 和第 5 标题级别条目是第二个 3 级别条目的子条目，依此类推。
// 在大纲中，我们可以单击“所有者”条目的箭头来折叠/展开其所有子条目。
// 将“ExpandedOutlineLevels”属性设置为“2”以自动展开所有标题级别 2 和较低的大纲条目
// 当我们打开文档时，折叠所有级别、3 级及更高级别的条目。
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### 也可以看看

* class [OutlineOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
