---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: .NET için Aspose.Words
description: En iyi performans için özelleştirilebilir görüntü kaydetme seçenekleriyle belge işlemeyi geliştiren Aspose.Words.ImageSavingArgs sınıfını keşfedin.
type: docs
weight: 5990
url: /tr/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Şunun için veri sağlar:[`ImageSaving`](../iimagesavingcallback/imagesaving/) olay.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

```csharp
public class ImageSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Şunu alır:[`ShapeBase`](../../aspose.words.drawing/shapebase/) kaydedilmek üzere olan şekil veya grup şekline karşılık gelen nesne |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Şu anda kaydedilmekte olan belge nesnesini alır. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Görüntünün kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Görüntünün kaydedileceği akışı belirtmenize olanak tanır. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Geri Döndürür`doğru` Mevcut görüntü dışa aktarılabilirse. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Aspose.Words'ün bir görüntüyü kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir. |

## Notlar

Varsayılan olarak, Aspose.Words bir belgeyi HTML'ye kaydettiğinde, her resmi ayrı bir dosya olan 'ye kaydeder. Aspose.Words, belgede bulunan her resim için benzersiz dosya adı oluşturmak amacıyla belge dosya adını ve benzersiz bir numarayı kullanır.

`ImageSavingArgs`görüntü dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak görüntülerin dosyalara kaydedilmesini tamamen engellemenize olanak tanır.

Görüntü dosyası adlarını oluşturmak için kendi mantığınızı uygulamak üzere kullanın[`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) Ve[`IsImageAvailable`](./isimageavailable/) özellikleri.

Görüntüleri dosyalar yerine akışlara kaydetmek için şunu kullanın:[`ImageStream`](./imagestream/) mülk.

## Örnekler

Bir belgenin parçalara nasıl bölüneceğini ve kaydedileceğini gösterir.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // Belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Belgeyi normal şekilde kaydedersek, bir HTML çıktısı olacaktır
    // kaynak belgenin tüm içeriğini içeren belge.
    // "DocumentSplitCriteria" özelliğini "DocumentSplitCriteria.SectionBreak" olarak ayarlayın
    // Belgemizi birden fazla HTML dosyasına kaydedelim: her bölüm için bir tane.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Belge parçası kaydetme mantığını değiştirmek için "DocumentPartSavingCallback" özelliğine özel bir geri arama atayın.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Resim içeren bir belgeyi html'e dönüştürürsek, birden fazla resme bağlantı veren tek bir html dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacak.
    // Ayrıca her bir görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri çağırma da vardır.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Kaydetme işleminin bir belgeyi böldüğü çıktı belgeleri için özel dosya adları ayarlar.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // "Belge" özelliği aracılığıyla kaynak belgenin tamamına erişebiliriz.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Aşağıda Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirtmenin iki yolu bulunmaktadır.
        // 1 - Çıktı parçası dosyası için bir dosya adı belirleyin:
        args.DocumentPartFileName = partFileName;

        // 2 - Çıktı parça dosyası için özel bir akış oluşturun:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// HTML dönüşümünün oluşturduğu resim dosyaları için özel dosya adları ayarlar.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Aşağıda Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirtmenin iki yolu bulunmaktadır.
        // 1 - Çıkış görüntü dosyası için bir dosya adı belirleyin:
        args.ImageFileName = imageFileName;

        // 2 - Çıktı görüntü dosyası için özel bir akış oluşturun:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
