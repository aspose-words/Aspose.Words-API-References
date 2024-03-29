---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.PdfCompliance 枚举. 指定 PDF 标准合规级别 在 C#.
type: docs
weight: 5410
url: /zh/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

指定 PDF 标准合规级别。

```csharp
public enum PdfCompliance
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Pdf17 | `0` | 输出文件将符合 PDF 1.7 (ISO 32000-1) 标准。 |
| Pdf20 | `1` | 输出文件将符合 PDF 2.0 (ISO 32000-2) 标准。 |
| PdfA1a | `2` | 输出文件将符合 PDF/A-1a (ISO 19005-1) 标准。 此级别包括 PDF/A-1b 的所有要求，并且还要求 包含文档结构（也称为“标记”） ), 目的是确保文档内容可以被搜索和重新利用。 |
| PdfA1b | `3` | 输出文件将符合 PDF/A-1b (ISO 19005-1) 标准。 PDF/A-1b 的目标是确保可靠地再现 文档的视觉外观。 |
| PdfA2a | `4` | 输出文件将符合 PDF/A-2a (ISO 19005-2) 标准。 此级别包括 PDF/A-2u 的所有要求，另外还要求 包含文档结构（也称为“标记”） ), 目的是确保文档内容可以被搜索和重新利用。 |
| PdfA2u | `5` | 输出文件将符合 PDF/A-2u (ISO 19005-2) 标准。 PDF/A-2u 的目标是随着时间的推移保留文档静态视觉外观，独立于用于创建、存储的工具 和系统或渲染文件。此外，文档 中包含的任何文本都可以可靠地提取为一系列 Unicode 代码点。 |
| PdfA4 | `6` | 输出文件将符合 PDF/A-4 (ISO 19005-4:2020) 标准。 PDF/A-4 的目标是随着时间的推移保留文档静态视觉外观，独立于用于创建的工具 和系统、存储或渲染文件。此外，文档 中包含的任何文本都可以可靠地提取为一系列 Unicode 代码点。 |
| PdfUa1 | `7` | 输出文件将符合 PDF/UA-1 (ISO 14289-1) 标准。 PDF/UA 的主要目的是定义如何以 a 方式表示 PDF 格式的电子文档，从而允许文件可访问. |

## 例子

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
