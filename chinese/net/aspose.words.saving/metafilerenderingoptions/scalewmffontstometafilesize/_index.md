---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Aspose.Words for .NET API 参考
description: MetafileRenderingOptions 财产. 获取或设置一个值该值确定是否根据页面上的图元文件大小来缩放 WMF 图元文件中的字体
type: docs
weight: 50
url: /zh/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

获取或设置一个值，该值确定是否根据页面上的图元文件大小来缩放 WMF 图元文件中的字体。

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### 评论

当 WMF 图元文件在 MS Word 中显示时，字体可能会根据页面上的实际图元文件大小进行缩放。

当此值设置为`真的`, Aspose.Words 根据页面上的图元文件大小模拟字体缩放。

当此值设置为`错误的`, Aspose.Words 将字体显示为图元文件呈现为其默认大小。

此选项仅在元文件呈现为矢量图形时使用。

默认值为`真的`.

### 例子

显示如何根据页面上的图元文件大小缩放 WMF 字体。

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“ScaleWmfFontsToMetafileSize”属性设置为“true”以缩放字体
// 根据页面上图元文件的大小格式化 WMF 图像中的文本。
// 将“ScaleWmfFontsToMetafileSize”属性设置为“false”以
// 保留这些字体的默认比例。
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### 也可以看看

* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../metafilerenderingoptions/)
* 部件 [Aspose.Words](../../../)


