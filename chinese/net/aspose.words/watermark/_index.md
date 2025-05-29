---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Watermark 类，轻松在文档中添加和自定义水印，增强专业性和品牌影响力。
type: docs
weight: 7520
url: /zh/net/aspose.words/watermark/
---
## Watermark class

表示与文档水印配合使用的类。

要了解更多信息，请访问[使用水印](https://docs.aspose.com/words/net/working-with-watermark/)文档文章。

```csharp
public sealed class Watermark
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | 获取水印类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | 删除水印。 |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | 在文档中添加图像水印。 |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | 在文档中添加图像水印。 |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | 在文档中添加图像水印。 |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | 在文档中添加图像水印。 |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | 在文档中添加文本水印。 |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | 在文档中添加文本水印。 |

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
