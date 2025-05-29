---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words for .NET
description: 了解 PdfSaveOptions DisplayDocTitle 属性如何通过在 Windows 标题栏中显示文档标题以便于识别来增强您的 PDF 体验。
type: docs
weight: 90
url: /zh/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

一个标志，指定窗口的标题栏是否应显示从文档信息字典的标题条目中获取的文档标题。

```csharp
public bool DisplayDocTitle { get; set; }
```

## 评论

如果`错误的`，标题栏应该显示包含该文档的 PDF 文件的名称。

PDF/UA 合规性要求此标志。`真的`将 保存为 PDF/UA 时将自动使用该值。

默认值为`错误的`。

## 例子

展示如何将文档的标题显示为标题栏。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 将“DisplayDocTitle”设置为“true”以获取一些 PDF 阅读器，例如 Adobe Acrobat Pro，
// 在属于该文档的选项卡中显示文档的“标题”内置属性的值。
// 将“DisplayDocTitle”设置为“false”以使此类阅读器显示文档的文件名。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
