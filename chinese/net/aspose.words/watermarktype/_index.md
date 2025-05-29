---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.WatermarkType 枚举，轻松自定义文档中的水印。使用丰富的水印选项增强您的项目！
type: docs
weight: 7540
url: /zh/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

指定水印类型。

```csharp
public enum WatermarkType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Text | `0` | 表示文本将用作水印。 |
| Image | `1` | 表示该图像将用作水印。 |
| None | `2` | 表示未设置水印。 |

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
