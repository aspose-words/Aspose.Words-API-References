---
title: ImageSavingArgs.ImageStream
second_title: Aspose.Words for .NET API Referansı
description: ImageSavingArgs mülk. Görüntünün kaydedileceği akışı belirtmeye izin verir.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Görüntünün kaydedileceği akışı belirtmeye izin verir.

```csharp
public Stream ImageStream { get; set; }
```

### Notlar

Bu özellik, HTML sırasında görüntüleri dosyalar yerine akışlara kaydetmenize olanak tanır.

Varsayılan değer:`hükümsüz` . Bu özellik olduğunda`hükümsüz` görüntüsü, belirtilen dosyaya kaydedilecektir.[`ImageFileName`](../imagefilename/) mülk.

Kullanma[`IImageSavingCallback`](../../iimagesavingcallback/) bir resmi başka bir resimle değiştiremezsiniz. Yalnızca görüntülerin kaydedileceği konumu kontrol etmek için tasarlanmıştır.

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

* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../imagesavingargs/)
* toplantı [Aspose.Words](../../../)


