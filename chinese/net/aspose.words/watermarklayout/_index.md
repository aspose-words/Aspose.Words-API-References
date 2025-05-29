---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.WatermarkLayout 枚举，实现最佳水印定位。通过精确的布局控制和自定义功能，增强您的文档设计。
type: docs
weight: 7530
url: /zh/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

定义相对于水印中心的水印布局。

```csharp
public enum WatermarkLayout
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Horizontal | `0` | 水平水印布局。对应于 0 度旋转。 |
| Diagonal | `315` | 对角线水印布局。相当于 315 度旋转。 |

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
