---
title: ImageSavingArgs.KeepImageStreamOpen
linktitle: KeepImageStreamOpen
articleTitle: KeepImageStreamOpen
second_title: .NET için Aspose.Words
description: Aspose.Words için ImageSavingArgs'daki KeepImageStreamOpen özelliğini keşfedin. Verimli görüntü kaydetme ve gelişmiş performans için akış davranışını kontrol edin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

Aspose.Words'ün bir görüntüyü kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

## Notlar

Varsayılan`YANLIŞ` ve Aspose.Words, sağladığınız akışı kapatacaktır [`ImageStream`](../imagestream/) içine bir resim yazıldıktan sonra özellik. Belirtin`doğru` akışı açık tutmak için.

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

* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
