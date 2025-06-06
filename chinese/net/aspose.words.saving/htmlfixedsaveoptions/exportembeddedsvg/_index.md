---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words for .NET
description: 探索 HtmlFixedSaveOptions 的 ExportEmbeddedSvg 属性，轻松将 SVG 资源嵌入 HTML 文档，以增强视觉效果。默认值为 true。
type: docs
weight: 70
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

指定是否应将 SVG 资源嵌入到 Html 文档中。 默认值为`真的`.

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## 例子

展示如何确定将文档导出为 Html 时存储 SVG 对象的位置。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 当我们将包含 SVG 对象的文档导出为 .html 时，
// Aspose.Words 可以将这些对象放置在两个可能的位置。
// 将“ExportEmbeddedSvg”标志设置为“true”将嵌入所有 SVG 对象原始数据
// 在输出 HTML 中，在 <image> 标签内。
// 将此标志设置为“false”将在本地文件系统中为每个 SVG 对象创建一个文件。
// HTML 将使用 <object> 标签的“数据”属性链接到每个文件。
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
