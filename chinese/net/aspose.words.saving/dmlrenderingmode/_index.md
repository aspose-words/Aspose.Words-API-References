---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Saving.DmlRenderingMode 如何增强 DrawingML 形状渲染，以实现高质量的固定页面格式。优化您的文档视觉效果！
type: docs
weight: 5670
url: /zh/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

指定如何将 DrawingML 形状呈现为固定页面格式。

```csharp
public enum DmlRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Fallback | `0` | 如果 DrawingML 有后备形状，Aspose.Words 会渲染后备形状而不是 DrawingML。 |
| DrawingML | `1` | Aspose.Words 忽略 DrawingML 的后备形状并渲染 DrawingML 本身。 这是默认模式。 |

## 例子

展示如何在保存为 PDF 时呈现后备形状。

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“DmlRenderingMode”属性设置为“DmlRenderingMode.Fallback”
// 用后备形状替换 DML 形状。
// 将“DmlRenderingMode”属性设置为“DmlRenderingMode.DrawingML”
// 来呈现 DML 形状本身。
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

展示如何在将文档保存为 PDF 时配置文档中 DrawingML 效果的渲染质量。

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.None”以放弃所有DrawingML效果。
// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.Simplified”
// 呈现 DrawingML 效果的简化版本。
// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.Fine”
// 以更高的精度和更高的处理成本渲染 DrawingML 效果。
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
