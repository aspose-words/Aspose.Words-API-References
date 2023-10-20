---
title: TextWatermarkOptions.FontFamily
linktitle: FontFamily
articleTitle: FontFamily
second_title: 用于 .NET 的 Aspose.Words
description: TextWatermarkOptions FontFamily 财产. 获取或设置字体系列名称默认值为Calibri 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/textwatermarkoptions/fontfamily/
---
## TextWatermarkOptions.FontFamily property

获取或设置字体系列名称。默认值为“Calibri”。

```csharp
public string FontFamily { get; set; }
```

## 例子

展示如何创建文本水印。

```csharp
Document doc = new Document();

// 添加纯文本水印。
doc.Watermark.SetText("Aspose Watermark");

// 如果我们希望使用它作为水印来编辑文本格式，
// 我们可以通过在创建水印时传递 TextWatermarkOptions 对象来做到这一点。
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// 我们可以像这样从文档中删除水印。
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### 也可以看看

* class [TextWatermarkOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
