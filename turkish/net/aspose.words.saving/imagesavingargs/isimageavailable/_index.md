---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: .NET için Aspose.Words
description: ImageSavingArgs'daki IsImageAvailable özelliği ile bir görüntünün dışa aktarılmaya hazır olup olmadığını kontrol edin. Sorunsuz görüntü yönetimi ve verimliliği sağlayın!
type: docs
weight: 50
url: /tr/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Geri Döndürür`doğru` Mevcut görüntü dışa aktarılabilirse.

```csharp
public bool IsImageAvailable { get; }
```

## Notlar

Belgedeki bazı resimler, örneğin image bağlantılı olduğu ve bağlantı erişilemez olduğu veya geçerli bir resme işaret etmediği için kullanılamayabilir. Bu durumda Aspose.Words kırmızı çarpı işareti olan bir simgeyi dışa aktarır. Bu özellik döndürür`doğru` eğer orijinal görüntü mevcutsa; döner`YANLIŞ`eğer orijinal görüntüsü mevcut değilse ve kaydetmek için "görüntü yok" simgesi sunulacaktır.

Bir grup şeklini veya herhangi bir görüntü gerektirmeyen bir şekli kaydederken bu özellik her zaman`doğru`.

## Örnekler

Bir HTML dönüştürme işleminde görüntü kaydetme geri aramasının nasıl dahil edileceğini gösterir.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Belgeyi HTML'e kaydettiğimizde, bir geri arama belirtmek için bir SaveOptions nesnesi geçirebiliriz
    // Görüntü kaydetme işlemini özelleştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Kaydetme işlemi görüntüyü yerel dosya sistemindeki bir görüntü dosyasına kaydederken her görüntünün özelliklerini yazdırır
/// Bir belgenin HTML'e aktarılması sırasında.
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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
