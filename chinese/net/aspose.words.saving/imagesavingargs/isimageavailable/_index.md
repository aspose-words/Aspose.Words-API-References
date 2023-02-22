---
title: ImageSavingArgs.IsImageAvailable
second_title: Aspose.Words for .NET API 参考
description: ImageSavingArgs 财产. 返回真的如果当前图像可用于导出
type: docs
weight: 50
url: /zh/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

返回`真的`如果当前图像可用于导出。

```csharp
public bool IsImageAvailable { get; }
```

### 评论

文档中的某些图像可能不可用，例如，因为 image 已链接并且链接不可访问或未指向有效图像。 在这种情况下，Aspose.Words 导出一个带有红十字的图标。此属性返回 `真的`如果原始图像可用；返回`错误的`如果原始 图像不可用并且将提供“无图像”图标以供保存。

保存组形状或不需要任何图像的形状时，此属性 始终`真的`.

### 例子

展示如何在 HTML 转换过程中涉及图像保存回调。

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象来指定一个回调
    // 自定义图像保存过程。
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// 打印每个图像的属性，因为保存过程将其保存到本地文件系统中的图像文件
/// 在将文档导出为 HTML 期间。
/// </summary>
private class ImageShapePrinter : IImageSavingCallback
{
    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        args.KeepImageStreamOpen = false;
        Assert.True(args.IsImageAvailable);

        Console.WriteLine($"{args.Document.OriginalFileName.Split('\\').Last()} Image #{++mImageCount}");

        LayoutCollector layoutCollector = new LayoutCollector(args.Document);

        Console.WriteLine($"\tOn page:\t{layoutCollector.GetStartPageIndex(args.CurrentShape)}");
        Console.WriteLine($"\tDimensions:\t{args.CurrentShape.Bounds}");
        Console.WriteLine($"\tAlignment:\t{args.CurrentShape.VerticalAlignment}");
        Console.WriteLine($"\tWrap type:\t{args.CurrentShape.WrapType}");
        Console.WriteLine($"Output filename:\t{args.ImageFileName}\n");
    }

    private int mImageCount;
}
```

### 也可以看看

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../imagesavingargs/)
* 部件 [Aspose.Words](../../../)


