---
title: ImageSavingArgs.ImageFileName
linktitle: ImageFileName
articleTitle: ImageFileName
second_title: Aspose.Words for .NET
description: ImageSavingArgs ImageFileName mülk. Görüntünün kaydedileceği dosya adını yol olmadan alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

Görüntünün kaydedileceği dosya adını (yol olmadan) alır veya ayarlar.

```csharp
public string ImageFileName { get; set; }
```

## Notlar

Bu özellik, HTML'ye dışa aktarma sırasında görüntü dosyası adlarının nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Etkinlik başlatıldığında bu özellik, Aspose.Words tarafından oluşturulan dosya adını içerir. Görüntüyü farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, HTML formatına aktarıldığında her gömülü görüntü için otomatik olarak benzersiz bir dosya adı oluşturur. Görüntü dosyası adının nasıl oluşturulduğu ( ), belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi bir dosyaya kaydederken oluşturulan görüntü dosyasının adı gibi görünür&lt;belge tabanı dosya adı&gt;.&lt;görüntü numarası&gt;.&lt;uzantı&gt;.

Bir belgeyi bir akışa kaydederken oluşturulan görüntü dosyasının adı gibi görünürAspose.Words.&lt;belge kılavuzu&gt;.&lt;görüntü numarası&gt;.&lt;uzantı&gt;.

`ImageFileName` yol olmadan yalnızca dosya adını içermelidir. Aspose.Words, kaydetme yolunu ve dosyanın değerini belirler.`kaynak` belge dosya adını kullanarak HTML'ye yazma özelliği,[`ImagesFolder`](../../htmlsaveoptions/imagesfolder/) ve [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias/) özellikler.

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

* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
