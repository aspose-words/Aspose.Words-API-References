---
title: ParagraphFormat.IsHeading
linktitle: IsHeading
articleTitle: IsHeading
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat IsHeading 财产. 当段落样式是内置标题样式之一时为真 在 C#.
type: docs
weight: 140
url: /zh/net/aspose.words/paragraphformat/isheading/
---
## ParagraphFormat.IsHeading property

当段落样式是内置标题样式之一时为真。

```csharp
public bool IsHeading { get; }
```

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

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
