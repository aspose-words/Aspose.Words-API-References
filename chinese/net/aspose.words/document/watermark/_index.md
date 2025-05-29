---
title: Document.Watermark
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words for .NET
description: 使用我们可自定义的水印功能保护您的文档。轻松增强保护并确保真实性！
type: docs
weight: 500
url: /zh/net/aspose.words/document/watermark/
---
## Document.Watermark property

提供对文档水印的访问。

```csharp
public Watermark Watermark { get; }
```

## 例子

展示如何创建文本水印。

```csharp
Document doc = new Document();

// 添加纯文本水印。
doc.Watermark.SetText("Aspose Watermark");

// 如果我们希望使用它作为水印来编辑文本格式，
// 我们可以在创建水印时通过传递 TextWatermarkOptions 对象来实现这一点。
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// 我们可以从这样的文档中删除水印。
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### 也可以看看

* class [Watermark](../../watermark/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
