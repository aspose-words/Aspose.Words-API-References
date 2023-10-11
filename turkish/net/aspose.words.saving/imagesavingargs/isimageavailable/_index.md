---
title: ImageSavingArgs.IsImageAvailable
second_title: Aspose.Words for .NET API Referansı
description: ImageSavingArgs mülk. İadelerdoğru mevcut görüntü dışa aktarım için mevcutsa.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

İadeler`doğru` mevcut görüntü dışa aktarım için mevcutsa.

```csharp
public bool IsImageAvailable { get; }
```

### Notlar

Örneğin, image bağlantılı olduğundan ve bağlantıya erişilemediğinden veya geçerli bir resme işaret etmediğinden belgedeki bazı resimler kullanılamayabilir. Bu durumda Aspose.Words kırmızı çarpı işaretli bir simgeyi dışa aktarır. Bu özellik değerini döndürür`doğru` orijinal görsel mevcutsa; İadeler`YANLIŞ`orijinal görüntüsü mevcut değilse ve kaydetme için "görüntü yok" simgesi sunulur.

Bir grup şeklini veya herhangi bir görüntü gerektirmeyen bir şekli kaydederken bu özellik her zaman olur`doğru`.

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../imagesavingargs/)
* toplantı [Aspose.Words](../../../)


