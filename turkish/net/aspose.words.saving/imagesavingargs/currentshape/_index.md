---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: .NET için Aspose.Words
description: Projelerinizde etkili şekil ve grup şekli kaydetme için ShapeBase nesnesine erişmek üzere ImageSavingArgs CurrentShape özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Şunu alır:[`ShapeBase`](../../../aspose.words.drawing/shapebase/) kaydedilmek üzere olan şekil veya grup şekline karşılık gelen nesne

```csharp
public ShapeBase CurrentShape { get; }
```

## Notlar

[`IImageSavingCallback`](../../iimagesavingcallback/) bir şekli veya bir grup şeklini kaydederken tetiklenebilir. Bu nedenle özellik[`ShapeBase`](../../../aspose.words.drawing/shapebase/) türü. ile karşılaştırarak bir grup şekli olup olmadığını kontrol edebilirsiniz.[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) ileGroup veya türetilmiş sınıflardan birine dönüştürerek: [`Shape`](../../../aspose.words.drawing/shape/) veya[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words, belgede bulunan her görüntü için benzersiz dosya adı oluşturmak üzere belge dosya adını ve benzersiz bir numarayı kullanır.`CurrentShape`şekil özelliklerini inceleyerek "daha iyi" bir dosya adı oluşturmak için özellik[`Title`](../../../aspose.words.drawing/imagedata/title/) (Yalnızca Şekil),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Sadece şekil) ve[`Name`](../../../aspose.words.drawing/shapebase/name/)Elbette dosya adlarını başka herhangi bir özellik veya ölçüt kullanarak da oluşturabilirsiniz ancak yan dosya adlarının dışa aktarma işlemi içinde benzersiz olması gerektiğini unutmayın.

Belgedeki bazı resimler kullanılamayabilir. Resim kullanılabilirliğini kontrol etmek için kullanın[`IsImageAvailable`](../isimageavailable/) mülk.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
