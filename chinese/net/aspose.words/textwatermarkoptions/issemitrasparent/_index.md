---
title: TextWatermarkOptions.IsSemitrasparent
linktitle: IsSemitrasparent
articleTitle: IsSemitrasparent
second_title: Aspose.Words for .NET
description: 探索 TextWatermarkOptions IsSemitransparent 属性——轻松控制水印透明度。自定义透明度设置，提升您的设计体验！
type: docs
weight: 50
url: /zh/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

获取或设置一个布尔值，该值决定水印的不透明度。 默认值为`真的`.

```csharp
public bool IsSemitrasparent { get; set; }
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

* class [TextWatermarkOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
