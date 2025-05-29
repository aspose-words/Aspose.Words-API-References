---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions PageLayout 属性，自定义 PDF 布局，以便在任何阅读器中都能获得最佳浏览体验。提升文档的呈现效果！
type: docs
weight: 250
url: /zh/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

指定在 PDF 阅读器中打开文档时使用的页面布局。

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## 评论

默认值为SinglePage.

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

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
