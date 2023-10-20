---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ImageSavingArgs sınıf. Şunun için veri sağlarImageSaving olay C#'da.
type: docs
weight: 5240
url: /tr/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Şunun için veri sağlar:[`ImageSaving`](../iimagesavingcallback/imagesaving/) olay.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

```csharp
public class ImageSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Alır[`ShapeBase`](../../aspose.words.drawing/shapebase/) kaydedilmek üzere olan şekline veya grup şekline karşılık gelen nesne. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Şu anda kaydedilmekte olan belge nesnesini alır. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Görüntünün kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Görüntünün kaydedileceği akışı belirtmeye izin verir. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | İadeler`doğru` mevcut görüntü dışa aktarım için mevcutsa. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Aspose.Words'ün görüntüyü kaydettikten sonra akışı açık mı tutması yoksa kapatması mı gerektiğini belirtir. |

## Notlar

Varsayılan olarak Aspose.Words bir belgeyi HTML'ye kaydettiğinde her görüntüyü ayrı bir dosyaya kaydeder. Aspose.Words, belgede bulunan her görüntü için benzersiz dosya name oluşturmak amacıyla belge dosya adını ve benzersiz bir numarayı kullanır.

`ImageSavingArgs`görüntü dosyası adlarının nasıl oluşturulduğunu yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak görüntülerin dosyalara kaydedilmesini tamamen engellemenize olanak tanır.

Görüntü dosyası adları oluşturmak için kendi mantığınızı uygulamak için kullanın[`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) Ve[`IsImageAvailable`](./isimageavailable/) özellikleri.

Görüntüleri dosyalar yerine akışlara kaydetmek için[`ImageStream`](./imagestream/) mülk.

## Örnekler

Bir belgenin nasıl parçalara ayrılacağını ve kaydedileceğini gösterir.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Belgenin "Save" yöntemine aktarabileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Belgeyi normal şekilde kaydedersek tek bir çıktı HTML'si olacaktır
    // kaynak belgenin tüm içeriğini içeren belge.
    // "DocumentSplitCriteria" özelliğini "DocumentSplitCriteria.SectionBreak" olarak ayarlayın
    // belgemizi birden fazla HTML dosyasına kaydedin: her bölüm için bir tane.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Belge bölümü kaydetme mantığını değiştirmek için "DocumentPartSavingCallback" özelliğine özel bir geri çağırma atayın.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Eğer görseller içeren bir belgeyi html'ye dönüştürürsek, birden fazla görsele bağlantı veren bir html dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacaktır.
    // Her görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri çağırma da vardır.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Kaydetme işleminin bir belgeyi böldüğü çıktı belgeleri için özel dosya adlarını ayarlar.
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
        // Kaynak belgenin tamamına "Belge" özelliği aracılığıyla erişebiliriz.
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

        // Aspose.Words'ün belgenin her bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıda verilmiştir.
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
/// HTML dönüştürmesinin oluşturduğu görüntü dosyaları için özel dosya adlarını ayarlar.
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

        // Aspose.Words'ün belgenin her bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıda verilmiştir.
        // 1 - Çıktı görüntü dosyası için bir dosya adı belirleyin:
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
