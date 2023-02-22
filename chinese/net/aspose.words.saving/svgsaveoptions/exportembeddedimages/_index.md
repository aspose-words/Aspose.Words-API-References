---
title: SvgSaveOptions.ExportEmbeddedImages
second_title: Aspose.Words for .NET API 参考
description: SvgSaveOptions 财产. 指定图像是否应作为base64 嵌入到SVG 文档中 注意设置此标志可以显着增加输出SVG 文件的大小
type: docs
weight: 20
url: /zh/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

指定图像是否应作为base64 嵌入到SVG 文档中。 注意设置此标志可以显着增加输出SVG 文件的大小。

```csharp
public bool ExportEmbeddedImages { get; set; }
```

### 例子

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
* 命名空间 [Aspose.Words.Saving](../../svgsaveoptions/)
* 部件 [Aspose.Words](../../../)


