---
title: ImageSavingArgs.ImageFileName
linktitle: ImageFileName
articleTitle: ImageFileName
second_title: .NET için Aspose.Words
description: Verimli görüntü işleme için görüntü dosyası adlarını ve kaydetme konumlarını kolayca yönetmek üzere ImageSavingArgs ImageFileName özelliğini keşfedin.
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

Bu özellik, HTML'e aktarma sırasında resim dosyası adlarının nasıl oluşturulacağını yeniden tanımlamanıza olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Görüntüyü farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, HTML biçimine aktarırken her gömülü görüntü için otomatik olarak benzersiz bir dosya adı oluşturur. Görüntü dosya adının nasıl oluşturulacağı , belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi bir dosyaya kaydederken, oluşturulan görüntü dosya adı gibi görünür&lt;belge temel dosya adı&gt;.&lt;görüntü numarası&gt;.&lt;uzantı&gt;.

Bir belgeyi bir akışa kaydederken, oluşturulan görüntü dosyası adı gibi görünürAspose.Words.&lt;belge kılavuzu&gt;.&lt;görüntü numarası&gt;.&lt;uzantı&gt;.

`ImageFileName` yalnızca dosya adını içermeli, yol içermemelidir. Aspose.Words, kaydetme yolunu ve değeri belirler`kaynak` 'yi belge dosya adını kullanarak HTML'ye yazmak için öznitelik,[`ImagesFolder`](../../htmlsaveoptions/imagesfolder/) ve [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias/) özellikler.

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

* class [ImageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
