---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.ColorMode 枚举. 指定如何渲染颜色 在 C#.
type: docs
weight: 4860
url: /zh/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

指定如何渲染颜色。

```csharp
public enum ColorMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Normal | `0` | 使用未修改的颜色进行渲染。 |
| Grayscale | `1` | 使用从白色到黑色的一系列灰色色调的颜色进行渲染。 |

## 例子

演示如何使用保存选项属性更改图像颜色。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 将“ColorMode”属性设置为“Grayscale”，以黑白方式渲染文档中的所有图像。
// 使用此设置，输出文档的大小可能会更大。
// 将“ColorMode”属性设置为“Normal”，以彩色渲染所有图像。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
