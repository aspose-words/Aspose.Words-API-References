---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET
description: 了解 EmfPlusDualRenderingMode 属性如何增强 EMF Dual 图元文件渲染。立即使用灵活的渲染选项优化您的图形！
type: docs
weight: 20
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

获取或设置一个值，确定如何呈现 EMF+ Dual 图元文件。

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## 评论

EMF+ 双图元文件包含 EMF+ 和 EMF 部分。MS Word 和 GDI+ 始终渲染 EMF+ 部分。 Aspose.Words 目前并不完全支持所有 EMF+ 记录，在某些情况下， EMF 部分的渲染结果看起来比 EMF+ 部分的渲染结果更好。

此选项仅在图元文件渲染为矢量图形时使用。当图元文件渲染为位图时，始终使用 EMF+ 部分。

默认值为EmfPlusWithFallback。

## 例子

展示如何在保存为 PDF 时配置增强型 Windows 图元文件相关的渲染选项。

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.Emf”
// 仅呈现 EMF+ 双元文件的 EMF 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlus”
// 呈现 EMF+ 双元文件的 EMF+ 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlusWithFallback”
// 如果所有 EMF+ 记录都受支持，则呈现 EMF+ 双元文件的 EMF+ 部分。
// 否则，Aspose.Words 将呈现 EMF 部分。
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// 将“UseEmfEmbeddedToWmf”属性设置为“true”以呈现嵌入的 EMF 数据
// 对于我们可以渲染为矢量图形的元文件。
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### 也可以看看

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
