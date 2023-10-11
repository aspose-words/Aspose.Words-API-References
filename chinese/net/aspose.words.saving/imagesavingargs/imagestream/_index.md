---
title: ImageSavingArgs.ImageStream
second_title: Aspose.Words for .NET API 参考
description: ImageSavingArgs 财产. 允许指定图像将保存到的流
type: docs
weight: 40
url: /zh/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

允许指定图像将保存到的流。

```csharp
public Stream ImageStream { get; set; }
```

### 评论

此属性允许您在 HTML 期间将图像保存到流而不是文件。

默认值为`无效的` 。当这个属性是`无效的` ，图像 将被保存到指定的文件中[`ImageFileName`](../imagefilename/)财产。

使用[`IImageSavingCallback`](../../iimagesavingcallback/)您不能用 一张图像替换另一张图像。它仅用于控制保存图像的位置。

### 例子

演示如何在 HTML 转换过程中涉及图像保存回调。

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象来指定回调
    // 自定义图像保存过程。
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// 在保存过程将每个图像保存到本地文件系统中的图像文件时打印每个图像的属性
/// 将文档导出为 HTML 期间。
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

* class [ImageSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../imagesavingargs/)
* 部件 [Aspose.Words](../../../)


