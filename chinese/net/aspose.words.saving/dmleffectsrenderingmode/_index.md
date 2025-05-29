---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words DmlEffectsRenderingMode 枚举，优化固定页面格式的 DrawingML 效果渲染。提升您的文档质量！
type: docs
weight: 5660
url: /zh/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

指定如何将 DrawingML 效果呈现为固定页面格式。

```csharp
public enum DmlEffectsRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Simplified | `0` | 简化了 DrawingML 效果的渲染。 |
| None | `1` | 未呈现任何 DrawingML 效果。 |
| Fine | `2` | DrawingML 效果在精细模式下渲染，涉及高级处理。 在此模式下渲染效果可获得更好的结果，但性能成本高于Simplified模式. |

## 例子

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
