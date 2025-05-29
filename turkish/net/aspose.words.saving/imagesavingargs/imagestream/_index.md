---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: .NET için Aspose.Words
description: Görüntülerinizi nereye kaydedeceğinizi kolayca belirlemek için ImageSavingArgs'daki ImageStream özelliğini keşfedin, böylece iş akışınızı ve verimliliğinizi artırın.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Görüntünün kaydedileceği akışı belirtmenize olanak tanır.

```csharp
public Stream ImageStream { get; set; }
```

## Notlar

Bu özellik HTML sırasında dosyaların yerine akışlara resim kaydetmenize olanak tanır.

Varsayılan değer:`hükümsüz` Bu özellik olduğunda`hükümsüz` , görüntüsü belirtilen bir dosyaya kaydedilecektir.[`ImageFileName`](../imagefilename/) mülk.

Kullanarak[`IImageSavingCallback`](../../iimagesavingcallback/) bir resmi başka bir resimle değiştiremezsiniz. Bu sadece resimlerin kaydedileceği yerin kontrolü için tasarlanmıştır.

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
