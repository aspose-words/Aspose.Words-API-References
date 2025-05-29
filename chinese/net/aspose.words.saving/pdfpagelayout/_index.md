---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.PdfPageLayout 枚举，实现最佳 PDF 浏览体验。自定义页面布局，增强任何 PDF 阅读器的可读性。
type: docs
weight: 6290
url: /zh/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

指定在 PDF 阅读器中打开文档时使用的页面布局。

```csharp
public enum PdfPageLayout
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| SinglePage | `0` | 一次显示一页。 |
| OneColumn | `1` | 在一列中显示页面。 |
| TwoColumnLeft | `2` | 将页面显示为两列，奇数页在左侧。 |
| TwoColumnRight | `3` | 将页面显示为两列，奇数页在右侧。 |
| TwoPageLeft | `4` | 一次显示两页，奇数页在左边。 |
| TwoPageRight | `5` | 一次显示两页，奇数页在右侧。 |

## 例子

展示如何在 PDF 阅读器中打开时显示页面。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// 一次显示两页，奇数页在左边。
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
