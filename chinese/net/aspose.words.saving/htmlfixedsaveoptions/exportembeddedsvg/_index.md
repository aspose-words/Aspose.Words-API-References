---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions ExportEmbeddedSvg 财产. 指定 SVG 资源是否应嵌入到 Html 文档中 默认值为真的 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

指定 SVG 资源是否应嵌入到 Html 文档中。 默认值为`真的`.

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## 例子

演示将文档导出为 Html 时如何确定 SVG 对象的存储位置。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 当我们将带有 SVG 对象的文档导出为 .html 时，
// Aspose.Words 可以将这些对象放置在两个可能的位置。
// 将“ExportEmbeddedSvg”标志设置为“true”将嵌入所有 SVG 对象原始数据
// 在输出 HTML 中的 <image> 内标签。
// 将此标志设置为“false”将在本地文件系统中为每个 SVG 对象创建一个文件。
// HTML 将使用 <object> 的“data”属性链接到每个文件。标签。
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
