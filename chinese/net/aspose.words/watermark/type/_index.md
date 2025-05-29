---
title: Watermark.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 探索“水印类型”属性，使用可自定义的水印增强您的设计，打造品牌形象并保护您的作品。立即提升您的视觉效果！
type: docs
weight: 10
url: /zh/net/aspose.words/watermark/type/
---
## Watermark.Type property

获取水印类型。

```csharp
public WatermarkType Type { get; }
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

* enum [WatermarkType](../../watermarktype/)
* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
