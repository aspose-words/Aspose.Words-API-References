---
title: DocumentPartSavingArgs.DocumentPartStream
linktitle: DocumentPartStream
articleTitle: DocumentPartStream
second_title: .NET için Aspose.Words
description: DocumentPartSavingArgs'daki DocumentPartStream özelliğinin, sorunsuz yönetim için belge parçalarınızı nereye kaydedeceğinizi kolayca belirtmenize nasıl olanak tanıdığını keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/documentpartsavingargs/documentpartstream/
---
## DocumentPartSavingArgs.DocumentPartStream property

Belge bölümünün kaydedileceği akışı belirtmenize olanak tanır.

```csharp
public Stream DocumentPartStream { get; set; }
```

## Notlar

Bu özellik, HTML dışa aktarımı sırasında belge parçalarını dosyalar yerine akışlara kaydetmenize olanak tanır.

Varsayılan değer:`hükümsüz` Bu özellik olduğunda`hükümsüz` , belge parçası belirtilen bir dosyaya kaydedilecektir.[`DocumentPartFileName`](../documentpartfilename/) mülk.

HTML formatında bir akışa kaydetme istendiğinde[`Save`](../../../aspose.words/document/save/) veya[`Save`](../../../aspose.words/document/save/) ve ilk belge kısmı kaydedilmek üzereyken, Aspose.Words burada çağıran tarafından başlangıçta geçirilen ana çıktı akışını öneriyor.

HTML tabanlı bir kapsayıcı biçimi olan EPUB biçimine kaydederken,`DocumentPartStream` belirtilemez çünkü tüm alt parçalar tek bir çıktı paketine kapsüllenecektir.

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

* class [DocumentPartSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
