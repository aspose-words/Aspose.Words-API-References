---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: 了解 PdfSaveOptions 合规性属性，以确保您的 PDF 文档符合质量和兼容性的行业标准。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

指定输出文档的 PDF 标准合规级别。

```csharp
public PdfCompliance Compliance { get; set; }
```

## 评论

默认为Pdf17。

## 例子

展示如何设置已保存 PDF 文档的 PDF 标准合规级别。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 请注意，保存为某个标准时，某些 PdfSaveOptions 是被禁止的，并且会自动修复。
// 使用 IWarningCallback 了解哪些选项已自动修复。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“Compliance”属性设置为“PdfCompliance.PdfA1b”以符合“PDF/A-1b”标准，
// 其目的是在 Aspose.Words 将文档转换为 PDF 时保留文档的视觉外观。
// 将“Compliance”属性设置为“PdfCompliance.Pdf17”以符合“1.7”标准。
// 将“Compliance”属性设置为“PdfCompliance.PdfA1a”以符合“PDF/A-1a”标准，
// 符合“PDF/A-1b”并保留原始文档的文档结构。
// 将“Compliance”属性设置为“PdfCompliance.PdfUa1”以符合“PDF/UA-1”（ISO 14289-1）标准，
// 旨在定义以 PDF 形式表示的电子文档，以允许文件被访问。
// 将“Compliance”属性设置为“PdfCompliance.Pdf20”以符合“PDF 2.0”（ISO 32000-2）标准。
// 将“Compliance”属性设置为“PdfCompliance.PdfA4”以符合“PDF/A-4”（ISO 19004:2020）标准，
// 随着时间的推移，保持文档的静态视觉外观。
// 将“Compliance”属性设置为“PdfCompliance.PdfA4Ua2”以符合 PDF/A-4（ISO 19005-4:2020）
// 和 PDF/UA-2（ISO 14289-2:2024）标准。
// 将“Compliance”属性设置为“PdfCompliance.PdfUa2”以符合 PDF/UA-2（ISO 14289-2:2024）标准。
// 这有助于使文档可搜索，但可能会显著增加已经很大的文档的大小。
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### 也可以看看

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
