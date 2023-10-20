---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: 用于 .NET 的 Aspose.Words
description: SaveOptions DmlRenderingMode 财产. 获取或设置一个值确定如何呈现 DrawingML 形状 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

获取或设置一个值，确定如何呈现 DrawingML 形状。

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## 评论

默认值为Fallback.

当文档导出为固定页面格式时使用此属性。

## 例子

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

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
