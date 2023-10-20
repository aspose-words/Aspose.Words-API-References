---
title: SvgSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: 用于 .NET 的 Aspose.Words
description: SvgSaveOptions ResourcesFolderAlias 财产. 指定用于构造写入 SVG 文档的图像 URI 的文件夹的名称 默认为无效的 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.saving/svgsaveoptions/resourcesfolderalias/
---
## SvgSaveOptions.ResourcesFolderAlias property

指定用于构造写入 SVG 文档的图像 URI 的文件夹的名称。 默认为`无效的`.

```csharp
public string ResourcesFolderAlias { get; set; }
```

## 评论

当你保存一个[`Document`](../../../aspose.words/document/)在 SVG 格式中，Aspose.Words 需要将文档中嵌入的所有 图像保存为独立文件。[`ResourcesFolder`](../resourcesfolder/) 允许您指定图像的保存位置和`ResourcesFolderAlias` 允许指定如何构建图像 URI。

## 例子

演示如何操作和打印在将文档转换为 .svg 时创建的链接资源的 URI。

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
/// 在转换为 .svg 时计算并打印包含的资源的 URI。
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
