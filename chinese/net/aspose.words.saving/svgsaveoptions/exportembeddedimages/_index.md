---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words for .NET
description: 了解 SvgSaveOptions ExportEmbeddedImages 属性如何让您将图像以 base64 格式嵌入 SVG 文件中，从而在管理文件大小的同时增强可移植性。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

指定是否应将图像以 base64 格式嵌入到 SVG 文档中。 请注意，激活此选项可能会导致输出 SVG 文件的大小显著增加。

```csharp
public bool ExportEmbeddedImages { get; set; }
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

* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
