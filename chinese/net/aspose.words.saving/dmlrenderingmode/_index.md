---
title: Enum DmlRenderingMode
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.DmlRenderingMode 枚举. 指定如何将 DrawingML 形状呈现为固定页面格式
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
| Fallback | `0` | 如果后备形状可用于 DrawingML，Aspose.Words 将渲染后备形状而不是 DrawingML。 |
| DrawingML | `1` | Aspose.Words 忽略 DrawingML 的后备形状并渲染 DrawingML 本身。 这是默认模式。 |

### 例子

展示保存为 PDF 时如何渲染后备形状。

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“DmlRenderingMode”属性设置为“DmlRenderingMode.Fallback”
// 用后备形状替换 DML 形状。
// 将“DmlRenderingMode”属性设置为“DmlRenderingMode.DrawingML”
// 渲染 DML 形状本身。
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

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


