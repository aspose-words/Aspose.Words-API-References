---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: 用于 .NET 的 Aspose.Words
description: ImageSavingArgs IsImageAvailable 财产. 返回真的当前图像是否可导出 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

返回`真的`当前图像是否可导出。

```csharp
public bool IsImageAvailable { get; }
```

## 评论

文档中的某些图像可能不可用，例如，因为 image 已链接并且该链接无法访问或未指向有效图像。 在本例中，Aspose.Words 导出带有红叉的图标。该属性返回 `真的`原始图像是否可用；回报`错误的`如果原始 图像不可用，将提供“无图像”图标进行保存。

当保存组形状或不需要任何图像的形状时，此属性 始终为`真的`。

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
