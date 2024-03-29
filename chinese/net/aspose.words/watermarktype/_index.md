---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.WatermarkType 枚举. 指定水印类型 在 C#.
type: docs
weight: 6690
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
| Text | `0` | 表示该文本将用作水印。 |
| Image | `1` | 表示该图像将用作水印。 |
| None | `2` | 表示未设置水印。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
