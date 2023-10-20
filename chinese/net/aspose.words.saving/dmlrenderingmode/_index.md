---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.DmlRenderingMode 枚举. 指定如何将 DrawingML 形状呈现为固定页面格式 在 C#.
type: docs
weight: 4920
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
| Fallback | `0` | 如果回退形状可用于 DrawingML，Aspose.Words 呈现回退形状而不是 DrawingML。 |
| DrawingML | `1` | Aspose.Words 忽略 DrawingML 的后备形状并呈现 DrawingML 本身。 这是默认模式。 |

## 例子

显示保存为 PDF 时如何呈现备用形状。

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 将“DmlRenderingMode”属性设置为“DmlRenderingMode.Fallback”
// 用它们的备用形状替换 DML 形状。
// 将“DmlRenderingMode”属性设置为“DmlRenderingMode.DrawingML”
// 自己渲染 DML 形状。
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

展示了当我们将文档保存为 PDF 时如何在文档中配置 DrawingML 效果的渲染质量。

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.None”以丢弃所有 DrawingML 效果。
// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.Simplified”
// 渲染一个简化版的 DrawingML 效果。
// 将“DmlEffectsRenderingMode”属性设置为“DmlEffectsRenderingMode.Fine”以
// 以更高的准确性和更高的处理成本渲染 DrawingML 效果。
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
