---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words for .NET
description: 了解 HtmlSaveOptions 的 ExportCidUrlsForMhtmlResources 如何通过启用图像、字体和 CSS 的 CID URL 来增强 MHTML 文档。默认值为 false。
type: docs
weight: 110
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

指定是否使用 CID (Content-ID) URL 引用 MHTML 文档中包含的资源（图片、字体、CSS）。默认值为`错误的`.

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## 评论

此选项仅影响保存为 MHTML 的文档。

默认情况下，MHTML 文档中的资源通过文件名引用（例如“image.png”），该文件名与 MIME 部分的“Content-Location”标头进行匹配。

此选项启用一种替代方法，其中对资源文件的引用被写为 CID (Content-ID) URL（例如，“cid:image.png”）并与“Content-ID”标头进行匹配。

理论上，这两种引用方法应该没有区别，并且在任何浏览器或邮件代理中都可以正常工作。然而，在实践中，某些代理无法通过文件名获取资源。如果您的浏览器或邮件代理拒绝加载 MTHML 文档中包含的资源（不显示图片或不加载 CSS 样式），请尝试使用 CID URL 导出文档。

## 例子

展示如何为输出 MHTML 文档启用内容 ID。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 设置此标志将替换“Content-Location”标签
// 使用输入文档中每个资源的“Content-ID”标签。
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
