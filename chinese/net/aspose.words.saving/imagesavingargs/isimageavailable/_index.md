---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: Aspose.Words for .NET
description: 使用 ImageSavingArgs 中的 IsImageAvailable 属性检查图像是否已准备好导出。确保无缝且高效的图像管理！
type: docs
weight: 50
url: /zh/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

返回`真的`如果当前图像可供导出。

```csharp
public bool IsImageAvailable { get; }
```

## 评论

文档中的某些图像可能不可用，例如，因为 image 已链接，但该链接无法访问或未指向有效图像。 在本例中，Aspose.Words 导出一个带有红叉的图标。此属性返回 `真的`如果原始图像可用；返回`错误的`如果原始 图像不可用，则会提供“无图像”图标以供保存。

保存组形状或不需要任何图像的形状时，此属性 始终为`真的`。

## 例子

展示如何在 HTML 转换过程中涉及图像保存回调。

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
/// 在保存过程中将每幅图像保存到本地文件系统中的图像文件时，打印其属性
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
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
