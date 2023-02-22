---
title: ImageSavingArgs.KeepImageStreamOpen
second_title: Aspose.Words for .NET API 参考
description: ImageSavingArgs 财产. 指定 Aspose.Words 是否应在保存图像后保持流打开或关闭
type: docs
weight: 60
url: /zh/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

指定 Aspose.Words 是否应在保存图像后保持流打开或关闭。

```csharp
public bool KeepImageStreamOpen { get; set; }
```

### 评论

默认为`错误的` Aspose.Words 将关闭您在[`ImageStream`](../imagestream/)将图像写入其中后的属性。 指定`真的`保持流打开。

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

* class [ImageSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../imagesavingargs/)
* 部件 [Aspose.Words](../../../)


