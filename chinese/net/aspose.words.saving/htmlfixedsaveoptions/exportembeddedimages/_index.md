---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words for .NET
description: 了解 HtmlFixedSaveOptions 中的 ExportEmbeddedImages 属性如何通过嵌入 Base64 格式的图像来增强您的 HTML 文档，从而优化视觉质量并管理文件大小。
type: docs
weight: 60
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

指定是否应将图像以 Base64 格式嵌入到 Html 文档中。 请注意，设置此标志会显著增加输出 Html 文件的大小。

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## 例子

展示如何确定将文档导出为 Html 时存储图像的位置。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 当我们将嵌入图像的文档导出为 .html 时，
// Aspose.Words 可以将图像放置在两个可能的位置。
// 将“ExportEmbeddedImages”标志设置为“true”将存储原始数据
// 对于输出 HTML 文档中的所有图像，在 <image> 标签的“src”属性中。
// 将此标志设置为“false”将在本地文件系统中为每个图像创建一个图像文件，
// 并将所有这些文件存储在单独的文件夹中。
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
