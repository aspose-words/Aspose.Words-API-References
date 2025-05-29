---
title: OutlineOptions.ExpandedOutlineLevels
linktitle: ExpandedOutlineLevels
articleTitle: ExpandedOutlineLevels
second_title: Aspose.Words for .NET
description: 发现 OutlineOptions 中的 ExpandedOutlineLevels 属性，允许您自定义文档大纲可见性，以增强导航和用户体验。
type: docs
weight: 60
url: /zh/net/aspose.words.saving/outlineoptions/expandedoutlinelevels/
---
## OutlineOptions.ExpandedOutlineLevels property

指定查看文件时文档大纲中展开显示的级别数。

```csharp
public int ExpandedOutlineLevels { get; set; }
```

## 评论

请注意，保存为 XPS 时此选项将不起作用。

指定 0 时文档大纲将会折叠；指定 1 时大纲中第一级 items 将会展开，依此类推。

默认值为 0。有效范围是 0 到 9。

## 例子

展示如何将整个文档转换为具有文档大纲三个级别的 PDF。

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

// 输出的 PDF 文档将包含一个大纲，它是一个列出文档正文中标题的目录。
// 单击此大纲中的条目将带我们到其相应标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“4”，以从大纲中排除所有级别高于 4 的标题。
options.OutlineOptions.HeadingsOutlineLevels = 4;

// 如果大纲条目在其自身和相同或较低级别下一个条目之间有更高级别的后续条目，
// 条目左侧会出现一个箭头。此条目是多个此类“子条目”的“所有者”。
// 在我们的文档中，第 5 个标题级别的大纲条目是第二个第 4 级大纲条目的子条目，
// 第 4 和第 5 个标题级条目是第二个第 3 级条目的子条目，依此类推。
// 在大纲中，我们可以点击“所有者”条目的箭头来折叠/展开其所有子条目。
// 将“ExpandedOutlineLevels”属性设置为“2”，以自动展开所有标题级别 2 及以下的大纲条目
// 当我们打开文档时，折叠所有级别和 3 及更高级别的条目。
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### 也可以看看

* class [OutlineOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
