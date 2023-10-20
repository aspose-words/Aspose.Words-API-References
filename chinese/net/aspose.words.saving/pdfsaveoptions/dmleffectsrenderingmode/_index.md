---
title: PdfSaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions DmlEffectsRenderingMode 财产. 获取或设置一个值确定如何呈现 DrawingML 效果 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

获取或设置一个值，确定如何呈现 DrawingML 效果。

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## 评论

默认值为Simplified.

当文档导出为固定页面格式时使用此属性。

如果[`Compliance`](../compliance/)被设定为PdfA1a或者PdfA1b , 属性始终返回None。

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
