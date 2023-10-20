---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.DmlEffectsRenderingMode 枚举. 指定如何将 DrawingML 效果呈现为固定页面格式 在 C#.
type: docs
weight: 4910
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
| Simplified | `0` | DrawingML 效果的渲染得到简化。 |
| None | `1` | 未渲染 DrawingML 效果。 |
| Fine | `2` | DrawingML 效果以精细模式渲染，涉及高级处理。 在此模式下，效果渲染可提供更好的结果，但性能成本高于Simplified模式. |

## 例子

演示如何在将文档保存为 PDF 时配置 DrawingML 效果的渲染质量。

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.None”以放弃所有 DrawingML 效果。
// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.Simplified”
// 渲染 DrawingML 效果的简化版本。
// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.Fine”
// 更准确地渲染 DrawingML 效果，但处理成本也更高。
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
