---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words for .NET
description: 了解如何在 SvgSaveOptions 中设置 ResourcesFolder，以便在将文档导出为 SVG 格式时高效存储图像。立即优化您的工作流程！
type: docs
weight: 80
url: /zh/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

指定将文档导出为 Svg 格式时保存资源（图像）的物理文件夹。 默认值为`无效的`.

```csharp
public string ResourcesFolder { get; set; }
```

## 评论

仅在以下情况下有效[`ExportEmbeddedImages`](../exportembeddedimages/)财产是`错误的`。

当你保存[`Document`](../../../aspose.words/document/)在 SVG 格式中，Aspose.Words 需要将文档中嵌入的所有 图像保存为独立文件。`ResourcesFolder` 允许您指定图像的保存位置，并且[`ResourcesFolderAlias`](../resourcesfolderalias/) 允许指定如何构建图像 URI。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认会将 图像保存在文档文件所在的文件夹中。使用`ResourcesFolder` 来覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有用于保存图像的文件夹 ，但仍需要将图像保存在某个位置。在这种情况下，您需要在`ResourcesFolder`财产

## 例子

展示如何操作和打印将文档转换为 .svg 时创建的链接资源的 URI。

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// 在转换为 .svg 时计算并打印所包含资源的 URI。
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### 也可以看看

* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
