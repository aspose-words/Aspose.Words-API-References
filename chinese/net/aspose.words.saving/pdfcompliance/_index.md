---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.PdfCompliance 枚举，增强您的 PDF 标准合规性。通过定制选项，满足各种需求，提升文档质量！
type: docs
weight: 6200
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
| Pdf17 | `0` | 输出文件将符合 PDF 1.7（ISO 32000-1）标准。 |
| Pdf20 | `1` | 输出文件将符合 PDF 2.0（ISO 32000-2）标准。 |
| PdfA1a | `2` | 输出文件将符合 PDF/A-1a (ISO 19005-1) 标准。 此级别包含 PDF/A-1b 的所有要求，此外还要求 包含文档结构（也称为“带标签”）， 以确保文档内容可搜索和重新利用。 |
| PdfA1b | `3` | 输出文件将符合 PDF/A-1b (ISO 19005-1) 标准。 PDF/A-1b 的目标是确保可靠地再现文档的 视觉外观。 |
| PdfA2a | `4` | 输出文件将符合 PDF/A-2a (ISO 19005-2) 标准。 此级别包含 PDF/A-2u 的所有要求，此外还要求 包含文档结构（也称为“标记”）， 以确保文档内容可搜索和重新利用。 |
| PdfA2u | `5` | 输出文件将符合 PDF/A-2u (ISO 19005-2) 标准。 PDF/A-2u 的目标是长期保留文档的静态视觉外观，不受用于创建、存储或渲染文件的工具 和系统的影响。此外，文档中包含的任何文本 都可以可靠地提取为一系列 Unicode 码位。 |
| PdfA3a | `6` | 输出文件将符合 PDF/A-3a (ISO 19005-3) 标准。 此级别包含 PDF/A-3u 的所有要求，此外还要求 包含文档结构（也称为“标记”）， 以确保文档内容可搜索和重新利用。 |
| PdfA3u | `7` | 输出文件将符合 PDF/A-3u (ISO 19005-3) 标准。 PDF/A-3u（以及 PDF/A-2u）的目标是长期保留文档的静态视觉外观，不受用于创建、存储或渲染文件的工具 和系统的影响。此外，文档中包含的任何文本 都可以可靠地提取为一系列 Unicode 码位。除了 PDF/A-2u 之外，PDF/A-3u 还允许将 附件嵌入 PDF 文档。 |
| PdfA4 | `8` | 输出文件将符合 PDF/A-4 (ISO 19005-4:2020) 标准。 PDF/A-4 的目标是长期保留文档的静态视觉外观，不受用于创建、存储或渲染文件的工具 和系统的影响。此外，文档中包含的任何文本 都可以可靠地提取为一系列 Unicode 码位。 |
| PdfA4f | `9` | 输出文件将符合 PDF/A-4f (ISO 19005-4:2020) 标准。 此级别包含 PDF/A-4 的所有要求，此外还允许将附件嵌入 PDF 文档。 |
| PdfA4Ua2 | `10` | 输出文件将同时符合 PDF/A-4 (ISO 19005-4:2020) 和 PDF/UA-2 (ISO 14289-2:2024) 标准。 PDF/A-4 的目标是长期保留文档的静态视觉外观，不受用于创建、存储或渲染文件的工具 和系统的影响。PDF/UA 的主要目的是定义如何 以 PDF 格式呈现电子文档，以便于文件访问。 |
| PdfUa1 | `11` | 输出文件将符合 PDF/UA-1 (ISO 14289-1) 标准。 PDF/UA 的主要目的是定义如何以 PDF 格式表示电子文档，以便于文件访问。 |
| PdfUa2 | `12` | 输出文件将符合 PDF/UA-2 (ISO 14289-2:2024) 标准。 PDF/UA 的主要目的是定义如何以 PDF 格式表示电子文档，以便于文件访问。 |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
