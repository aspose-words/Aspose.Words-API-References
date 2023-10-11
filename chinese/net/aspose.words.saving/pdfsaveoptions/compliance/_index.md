---
title: PdfSaveOptions.Compliance
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 指定输出文档的 PDF 标准合规级别
type: docs
weight: 40
url: /zh/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

指定输出文档的 PDF 标准合规级别。

```csharp
public PdfCompliance Compliance { get; set; }
```

### 评论

默认为Pdf17。

### 例子

演示如何设置已保存 PDF 文档的 PDF 标准合规级别。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 请注意，在保存到其中一种标准时，某些 PdfSaveOptions 是被禁止的，并且会自动修复。
// 使用 IWarningCallback 了解哪些选项会自动修复。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“Compliance”属性设置为“PdfCompliance.PdfA1b”以符合“PDF/A-1b”标准，
// 其目的是在 Aspose.Words 将文档转换为 PDF 时保留文档的视觉外观。
// 将“Compliance”属性设置为“PdfCompliance.Pdf17”以符合“1.7”标准。
// 将“Compliance”属性设置为“PdfCompliance.PdfA1a”以符合“PDF/A-1a”标准，
// 符合“PDF/A-1b”并保留原始文档的文档结构。
// 将“Compliance”属性设置为“PdfCompliance.PdfUa1”以符合“PDF/UA-1”(ISO 14289-1) 标准，
// 其目的是定义 PDF 中的电子文档，以允许文件被访问。
// 将“Compliance”属性设置为“PdfCompliance.Pdf20”以符合“PDF 2.0”(ISO 32000-2) 标准。
// 将“Compliance”属性设置为“PdfCompliance.PdfA4”以符合“PDF/A-4”(ISO 19004:2020) 标准，
// 随着时间的推移，它会保留文档的静态视觉外观。
// 这有助于使文档可搜索，但可能会显着增加已经很大的文档的大小。
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### 也可以看看

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


