---
title: ImageSavingArgs.KeepImageStreamOpen
linktitle: KeepImageStreamOpen
articleTitle: KeepImageStreamOpen
second_title: 用于 .NET 的 Aspose.Words
description: ImageSavingArgs KeepImageStreamOpen 财产. 指定 Aspose.Words 在保存图像后是否应保持流打开或关闭它 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

指定 Aspose.Words 在保存图像后是否应保持流打开或关闭它。

```csharp
public bool KeepImageStreamOpen { get; set; }
```

## 评论

默认为`错误的` Aspose.Words 将关闭您提供的流 [`ImageStream`](../imagestream/)写入图像后的属性。 指定`真的`以保持流打开。

## 例子

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
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
