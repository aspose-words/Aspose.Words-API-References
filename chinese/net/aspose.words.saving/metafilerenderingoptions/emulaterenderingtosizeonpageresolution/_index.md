---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words for .NET
description: 探索 MetafileRenderingOptions 的 EmulateRenderingToSizeOnPageResolution 属性。控制图元文件渲染分辨率，以实现最佳页面显示效果。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

获取或设置用于模拟图元文件渲染到页面大小的分辨率（以像素/英寸为单位）。

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## 评论

此选项仅用于[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/)设置为`真的`。

默认值为 96。这是默认的显示分辨率。也就是说，图元文件渲染将模拟 MS Word 中图元文件的显示，缩放比例为 100%。

## 例子

显示如何根据页面大小显示图元文件。

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmulateRenderingToSizeOnPage”属性设置为“true”
// 根据页面上的图元文件大小模拟渲染。
// 将“EmulateRenderingToSizeOnPage”属性设置为“false”
// 模拟图元文件渲染到其默认像素大小。
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### 也可以看看

* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
