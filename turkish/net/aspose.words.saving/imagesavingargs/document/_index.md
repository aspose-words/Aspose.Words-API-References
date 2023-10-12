---
title: ImageSavingArgs.Document
second_title: Aspose.Words for .NET API Referansı
description: ImageSavingArgs mülk. Şu anda kaydedilmekte olan belge nesnesini alır.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/imagesavingargs/document/
---
## ImageSavingArgs.Document property

Şu anda kaydedilmekte olan belge nesnesini alır.

```csharp
public Document Document { get; }
```

### Örnekler

Görüntü kaydetme geri aramasının HTML dönüştürme sürecine nasıl dahil edileceğini gösterir.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Belgeyi HTML'ye kaydettiğimizde, bir geri çağrıyı belirtmek için SaveOptions nesnesini iletebiliriz
    // görüntü kaydetme işlemini özelleştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Kaydetme işlemi yerel dosya sistemindeki bir görüntü dosyasına kaydederken her görüntünün özelliklerini yazdırır
/// bir belgenin HTML'ye aktarılması sırasında.
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

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../imagesavingargs/)
* toplantı [Aspose.Words](../../../)


