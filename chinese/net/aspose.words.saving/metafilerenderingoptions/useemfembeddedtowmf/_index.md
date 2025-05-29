---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words for .NET
description: 了解 UseEmfEmbeddedToWmf 属性如何优化 WMF 图元文件渲染，从而提高图形应用程序的性能和质量。
type: docs
weight: 70
url: /zh/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

获取或设置一个值，该值确定如何呈现嵌入 EMF 元文件的 WMF 元文件。

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## 评论

WMF 图元文件可能包含嵌入的 EMF 数据。MS Word 在大多数情况下使用嵌入的 EMF 数据。 GDI+ 始终使用 WMF 数据。

当此值设置为`真的`，Aspose.Words 在渲染时使用嵌入的 EMF 数据。

当此值设置为`错误的`，Aspose.Words 在渲染时使用 WMF 数据。

此选项仅在将图元文件渲染为矢量图形时使用。当将图元文件渲染为位图时，始终使用 WMF 数据。

默认值为`真的`。

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

* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
