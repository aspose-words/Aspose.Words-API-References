---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: 用于 .NET 的 Aspose.Words
description: MetafileRenderingOptions EmfPlusDualRenderingMode 财产. 获取或设置一个值确定应如何呈现 EMF 双图元文件 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

获取或设置一个值，确定应如何呈现 EMF+ 双图元文件。

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## 评论

EMF+ 双元文件包含 EMF+ 和 EMF 部分。 MS Word 和 GDI+ 始终渲染 EMF+ 部分。 Aspose.Words 目前并不完全支持所有 EMF+ 记录，在某些情况下， EMF 部分的渲染结果看起来比 EMF+ 部分的渲染结果更好。

仅当图元文件呈现为矢量图形时才使用此选项。当图元文件渲染 位图时，始终使用 EMF+ 部分。

默认值为EmfPlusWithFallback。

## 例子

演示如何在保存为 PDF 时配置增强型 Windows 图元文件相关的渲染选项。

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.Emf”
// 仅渲染 EMF+ 双图元文件的 EMF 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlus”
// 渲染 EMF+ 双图元文件的 EMF+ 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlusWithFallback”
// 如果支持所有 EMF+ 记录，则渲染 EMF+ 双图元文件的 EMF+ 部分。
// 否则，Aspose.Words 将渲染 EMF 部分。
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// 将“UseEmfEmbeddedToWmf”属性设置为“true”以渲染嵌入的 EMF 数据
// 用于我们可以渲染为矢量图形的图元文件。
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### 也可以看看

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
