---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions FontsFolderAlias 属性，自定义 HTML 文档中的字体 URI。轻松提升您的网页设计！
type: docs
weight: 320
url: /zh/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

指定用于构建写入 HTML 文档的字体 URI 的文件夹的名称。 默认值为空字符串。

```csharp
public string FontsFolderAlias { get; set; }
```

## 评论

当你保存[`Document`](../../../aspose.words/document/) HTML 格式和[`ExportFontResources`](../exportfontresources/) 设置为`真的`，Aspose.Words 需要将文档中使用的字体保存为独立文件。 [`FontsFolder`](../fontsfolder/)允许您指定字体的保存位置和 `FontsFolderAlias`允许指定如何构建字体 URI。

如果`FontsFolderAlias`不是空字符串，那么字体 URI written 到 HTML 将是FontsFolderAlias + &lt;字体文件名&gt;。

如果`FontsFolderAlias`是空字符串，那么字体 URI written 到 HTML 将是FontsFolder + &lt;字体文件名&gt;。

如果`FontsFolderAlias`设置为“.”（点），则无论其他选项如何，字体文件 name 都将被写入不带路径的 HTML。

指定文件夹名称以构造字体 URIs 的另一种方法是使用[`ResourceFolderAlias`](../resourcefolderalias/)。

## 例子

展示如何设置 Aspose.Words 在将文档保存为 HTML 时创建的外部保存资源的文件夹和文件夹别名。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
