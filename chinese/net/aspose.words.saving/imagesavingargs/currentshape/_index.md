---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: 用于 .NET 的 Aspose.Words
description: ImageSavingArgs CurrentShape 财产. 获取ShapeBase与即将保存的形状或组形状 对应的对象 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

获取[`ShapeBase`](../../../aspose.words.drawing/shapebase/)与即将保存的形状或组形状 对应的对象。

```csharp
public ShapeBase CurrentShape { get; }
```

## 评论

[`IImageSavingCallback`](../../iimagesavingcallback/)可以在保存形状或组形状时触发。 这就是为什么该属性有[`ShapeBase`](../../../aspose.words.drawing/shapebase/)类型。你可以检查它是否是一个组形状比较 [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/)和Group或者将其强制转换为派生类之一： [`Shape`](../../../aspose.words.drawing/shape/)或者[`GroupShape`](../../../aspose.words.drawing/groupshape/)。

Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个图像生成唯一的文件名 。您可以使用`CurrentShape`属性通过检查形状属性来生成 “更好”的文件名，例如[`Title`](../../../aspose.words.drawing/imagedata/title/) （仅形状），[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) （仅形状） 和[`Name`](../../../aspose.words.drawing/shapebase/name/)。当然，您可以使用任何其他属性或条件 构建文件名，但请注意，辅助文件名在导出操作中必须是唯一的。

文档中的某些图像可能不可用。要检查图像可用性 ，请使用[`IsImageAvailable`](../isimageavailable/)财产。

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
