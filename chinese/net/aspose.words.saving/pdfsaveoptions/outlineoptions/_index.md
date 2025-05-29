---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions 的 OutlineOptions 属性，轻松自定义 PDF 轮廓。增强导航功能，提升文档可用性！
type: docs
weight: 240
url: /zh/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

允许指定轮廓选项。

```csharp
public OutlineOptions OutlineOptions { get; }
```

## 评论

可以根据标题和书签创建大纲。

对于标题，大纲级别由标题级别决定。

可以设置要包含在大纲中的最大标题级别或完全禁用标题大纲。

对于书签，大纲级别可以在选项中设置为所有书签的默认值或特定书签的单独值。

此外，还可以使用相同的`OutlineOptions`班级。

## 例子

展示如何限制已保存的 PDF 文档大纲中出现的标题级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可作为 1、2 和 3 级目录条目的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// 输出的 PDF 文档将包含一个大纲，它是一个列出文档正文中标题的目录。
// 单击此大纲中的条目将带我们到其相应标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“2”，以从大纲中排除所有级别高于 2 的标题。
// 我们上面插入的最后两个标题将不会出现。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

展示如何在保存 PDF 文档时处理不包含任何相应标题的大纲级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可作为 1 级和 5 级目录条目的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是一个列出文档正文中标题的目录。
// 单击此大纲中的条目将带我们到其相应标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“5”，以在大纲中包含 5 级及以下的所有标题。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// 本文档包含 1 级和 5 级标题，不包含 2、3 和 4 级标题。
// 输出 PDF 文档将把大纲级别 2、3 和 4 视为“缺失”。
// 将“CreateMissingOutlineLevels”属性设置为“true”，以包含轮廓中所有缺失的级别，
// 由于没有可用的标题，因此留下空白的大纲条目。
// 将“CreateMissingOutlineLevels”属性设置为“false”以忽略缺失的轮廓级别，
// 并将大纲 5 级标题视为 2 级。
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### 也可以看看

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
