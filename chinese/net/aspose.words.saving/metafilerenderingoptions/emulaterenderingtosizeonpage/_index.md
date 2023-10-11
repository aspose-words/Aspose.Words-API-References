---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
second_title: Aspose.Words for .NET API 参考
description: MetafileRenderingOptions 财产. 获取或设置一个值该值确定图元文件渲染是根据页面 上的大小模拟图元文件的显示还是以其默认大小显示图元文件
type: docs
weight: 40
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

获取或设置一个值，该值确定图元文件渲染是根据页面 上的大小模拟图元文件的显示，还是以其默认大小显示图元文件。

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

### 评论

当图元文件在 MS Word 中显示时，某些图形可能会根据实际图元文件大小（以像素为单位）进行缩放。 即，即使缩放也可能会影响图元文件的显示。

当该值设置为`真的` Aspose.Words 根据页面上的图元文件大小模拟渲染。 大小（以像素为单位）是根据页面上的图元文件大小和指定的[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/)。

当该值设置为`错误的`，Aspose.Words 模拟图元文件渲染为其默认大小（以像素为单位）。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值为`真的`。

### 例子

展示如何根据页面大小显示图元文件。

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmulateRenderingToSizeOnPage”属性设置为“true”
// 根据页面上的图元文件大小模拟渲染。
// 将“EmulateRenderingToSizeOnPage”属性设置为“false”
// 模拟图元文件渲染为其默认大小（以像素为单位）。
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### 也可以看看

* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../metafilerenderingoptions/)
* 部件 [Aspose.Words](../../../)


