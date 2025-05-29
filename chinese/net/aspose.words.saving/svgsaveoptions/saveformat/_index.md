---
title: SvgSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 探索 SvgSaveOptions 的 SaveFormat 属性，轻松将文档保存为 SVG 格式。优化文件管理，简化您的工作流程！
type: docs
weight: 100
url: /zh/net/aspose.words.saving/svgsaveoptions/saveformat/
---
## SvgSaveOptions.SaveFormat property

指定如果使用此保存选项对象，文档将以哪种格式保存。 只能是Svg.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
