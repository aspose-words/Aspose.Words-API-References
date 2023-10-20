---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions OutlineOptions 财产. 允许指定轮廓选项 在 C#.
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

可以从标题和书签创建大纲。

对于标题大纲级别由标题级别决定。

可以设置要包含在大纲中的最大标题级别或完全禁用标题大纲。

对于书签，轮廓级别可以在选项中设置为所有书签的默认值或特定书签的单独值。

此外，可以使用相同的方法将轮廓导出为 XPS 格式`OutlineOptions`班级。

## 例子

展示如何限制已保存 PDF 文档大纲中显示的标题级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可作为 1、2、3 级目录条目的标题。
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

// 输出的 PDF 文档将包含一个大纲，它是列出文档正文中的标题的目录。
// 单击此大纲中的条目将带我们到达其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“2”，以从大纲中排除级别高于 2 的所有标题。
// 我们在上面插入的最后两个标题将不会出现。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

演示在保存 PDF 文档时如何使用不包含任何相应标题的大纲级别。

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

// 输出的 PDF 文档将包含一个大纲，它是列出文档正文中的标题的目录。
// 单击此大纲中的条目将带我们到达其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“5”，以在大纲中包含 5 级及以下级别的所有标题。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// 该文档包含1级和5级标题，没有2、3、4级标题。
// 输出 PDF 文档会将大纲级别 2、3 和 4 视为“缺失”。
// 将“CreateMissingOutlineLevels”属性设置为“true”以包含大纲中所有缺失的级别，
// 由于没有可用的标题，因此保留空白大纲条目。
// 将“CreateMissingOutlineLevels”属性设置为“false”以忽略缺失的轮廓级别，
// 并将大纲第 5 级标题视为第 2 级。
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### 也可以看看

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
