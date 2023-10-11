---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words for .NET API 参考
description: MetafileRenderingOptions 财产. 获取或设置分辨率以每英寸像素为单位以模拟图元文件渲染为页面上的大小
type: docs
weight: 50
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

获取或设置分辨率（以每英寸像素为单位），以模拟图元文件渲染为页面上的大小。

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

### 评论

该选项仅在以下情况下使用[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/)被设定为`真的`。

默认值为 96。这是默认显示分辨率。即图元文件渲染将模拟 MS Word 中 100% 缩放系数的 图元文件的显示。

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


