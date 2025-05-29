---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.ColorMode 枚举，优化色彩渲染。通过精确的颜色设置提升文档的视觉吸引力。
type: docs
weight: 5600
url: /zh/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

指定如何呈现颜色。

```csharp
public enum ColorMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Normal | `0` | 使用未修改的颜色进行渲染。 |
| Grayscale | `1` | 使用从白色到黑色的一系列灰色阴影进行渲染。 |

## 例子

展示如何使用保存选项属性来改变图像颜色。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 将“ColorMode”属性设置为“Grayscale”，以黑白色呈现文档中的所有图像。
// 使用此设置，输出文档的大小可能会更大。
// 将“ColorMode”属性设置为“Normal”以彩色呈现所有图像。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
