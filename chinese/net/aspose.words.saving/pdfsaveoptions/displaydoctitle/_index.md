---
title: PdfSaveOptions.DisplayDocTitle
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 一个标志指定窗口的标题栏是否应显示取自 文档信息字典的标题条目的文档标题
type: docs
weight: 80
url: /zh/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

一个标志，指定窗口的标题栏是否应显示取自 文档信息字典的标题条目的文档标题。

```csharp
public bool DisplayDocTitle { get; set; }
```

### 评论

如果`错误的`，标题栏应显示包含该文档的 PDF 文件的名称。

PDF/UA 合规性需要此标志。`真的`将 保存到PDF/UA时将自动使用该值。

默认值为`错误的`。

### 例子

演示如何将文档的标题显示为标题栏。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 将“DisplayDocTitle”设置为“true”以获取一些PDF阅读器，例如Adobe Acrobat Pro，
// 在属于该文档的选项卡中显示文档“Title”内置属性的值。
// 将“DisplayDocTitle”设置为“false”以使此类阅读器显示文档的文件名。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


