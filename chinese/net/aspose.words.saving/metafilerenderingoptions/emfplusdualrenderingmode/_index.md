---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET API 参考
description: MetafileRenderingOptions 财产. 获取或设置一个值确定应如何呈现 EMF 双元文件
type: docs
weight: 20
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

获取或设置一个值，确定应如何呈现 EMF+ 双元文件。

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### 评论

EMF+ 双元文件包含 EMF+ 和 EMF 部分。 MS Word 和 GDI+ 总是渲染 EMF+ 部分。 Aspose.Words 目前并不完全支持所有 EMF+ 记录，在某些情况下， EMF 部分的渲染结果看起来比 EMF+ 部分的渲染结果更好。

此选项仅在元文件呈现为矢量图形时使用。当元文件render 到位图时，总是使用EMF+ 部分。

默认值为EmfPlusWithFallback.

### 例子

显示保存为 PDF 时如何配置增强的 Windows 图元文件相关的呈现选项。

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.Emf”
// 仅渲染 EMF+ 双元文件的 EMF 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlus”以
// 渲染 EMF+ 双元文件的 EMF+ 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlusWithFallback”
// 如果支持所有 EMF+ 记录，则呈现 EMF+ 双元文件的 EMF+ 部分。
// 否则，Aspose.Words 将渲染 EMF 部分。
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// 将“UseEmfEmbeddedToWmf”属性设置为“true”以呈现嵌入的 EMF 数据
// 对于我们可以渲染为矢量图形的元文件。
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### 也可以看看

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../metafilerenderingoptions/)
* 部件 [Aspose.Words](../../../)


