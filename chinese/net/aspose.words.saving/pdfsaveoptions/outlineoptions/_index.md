---
title: OutlineOptions
second_title: Aspose.Words for .NET API 参考
description: 允许指定大纲选项
type: docs
weight: 210
url: /zh/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

允许指定大纲选项。

```csharp
public OutlineOptions OutlineOptions { get; }
```

### 评论

可以从标题和书签创建大纲。

对于标题大纲级别由标题级别决定。

可以将最大标题级别设置为包含在大纲中或完全禁用标题大纲。

对于书签，大纲级别可以在选项中设置为所有书签的默认值或特定书签的单独值。

此外，可以使用相同的方法将轮廓导出为 XPS 格式`OutlineOptions`班级。

### 例子

显示如何限制将出现在已保存 PDF 文档大纲中的标题级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可以用作级别 1、2 和 3 的 TOC 条目的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// 输出的 PDF 文档将包含一个大纲，它是一个目录，列出了文档正文中的标题。
// 单击此大纲中的条目会将我们带到其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“2”，从大纲中排除所有级别高于2的标题。
// 我们在上面插入的最后两个标题不会出现。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

演示如何在保存 PDF 文档时使用不包含任何相应标题的大纲级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可作为 1 级和 5 级 TOC 条目的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是一个目录，列出了文档正文中的标题。
// 单击此大纲中的条目会将我们带到其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“5”，以在大纲中包含所有级别 5 及以下的标题。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

 // 此文档包含 1 级和 5 级的标题，没有 2、3 和 4 级的标题。
// 输出的 PDF 文档会将大纲级别 2、3 和 4 视为“缺失”。
// 将“CreateMissingOutlineLevels”属性设置为“true”以在大纲中包含所有缺失的级别，
// 因为没有可用的标题，所以留下空白的大纲条目。
// 将“CreateMissingOutlineLevels”属性设置为“false”以忽略缺少的大纲级别，
// 并将大纲级别 5 的标题视为级别 2。
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### 也可以看看

* class [OutlineOptions](../../outlineoptions)
* class [PdfSaveOptions](../../pdfsaveoptions)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->