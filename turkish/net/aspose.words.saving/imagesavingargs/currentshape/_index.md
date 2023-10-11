---
title: ImageSavingArgs.CurrentShape
second_title: Aspose.Words for .NET API Referansı
description: ImageSavingArgs mülk. AlırShapeBase kaydedilmek üzere olan şekline veya grup şekline karşılık gelen nesne.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Alır[`ShapeBase`](../../../aspose.words.drawing/shapebase/) kaydedilmek üzere olan şekline veya grup şekline karşılık gelen nesne.

```csharp
public ShapeBase CurrentShape { get; }
```

### Notlar

[`IImageSavingCallback`](../../iimagesavingcallback/) bir şekil veya grup şekli kaydedilirken tetiklenebilir. Bu nedenle mülkte[`ShapeBase`](../../../aspose.words.drawing/shapebase/) tip. 'yi karşılaştıran bir grup şekli olup olmadığını kontrol edebilirsiniz.[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) ileGroup veya türetilmiş sınıflardan birine aktararak: [`Shape`](../../../aspose.words.drawing/shape/) veya[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words, belgede bulunan her görüntü için benzersiz dosya adı oluşturmak amacıyla belge dosya adını ve benzersiz bir numarayı kullanır. Şunu kullanabilirsiniz:`CurrentShape`gibi şekil özelliklerini inceleyerek "daha iyi" bir dosya adı oluşturma özelliği[`Title`](../../../aspose.words.drawing/imagedata/title/) (Yalnızca şekil),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Yalnızca şekil) ve[`Name`](../../../aspose.words.drawing/shapebase/name/). Tabii ki, diğer herhangi bir özelliği veya kriteri ( ) kullanarak dosya adları oluşturabilirsiniz, ancak yardımcı dosya adlarının dışa aktarma işleminde benzersiz olması gerektiğini unutmayın.

Belgedeki bazı resimler kullanılamayabilir. Resmin kullanılabilirliğini kontrol etmek için şunu kullanın:[`IsImageAvailable`](../isimageavailable/) mülk.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../imagesavingargs/)
* toplantı [Aspose.Words](../../../)


