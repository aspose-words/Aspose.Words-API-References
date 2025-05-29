---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TextWatermarkOptions，定制文本水印。使用独特、专业的品牌选项，提升您的文档品质！
type: docs
weight: 7290
url: /zh/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

包含添加带有文本的水印时可以指定的选项。

要了解更多信息，请访问[使用水印](https://docs.aspose.com/words/net/working-with-watermark/)文档文章。

```csharp
public class TextWatermarkOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | 获取或设置字体颜色。默认值为Silver. |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | 获取或设置字体系列名称。默认值为“Calibri”。 |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | 获取或设置字体大小。默认值为 0 - 自动。 |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | 获取或设置一个布尔值，该值决定水印的不透明度。 默认值为`真的`. |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | 获取或设置水印布局。默认值为Diagonal. |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
