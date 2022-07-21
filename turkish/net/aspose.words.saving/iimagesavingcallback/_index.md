---
title: IImageSavingCallback
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Wordsün bir belgeyi HTMLye kaydederken görüntüleri nasıl kaydettiğini kontrol etmek istiyorsanız bu arayüzü uygulayın. Diğer biçimler tarafından kullanılabilir.
type: docs
weight: 4910
url: /tr/net/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface

Aspose.Words'ün bir belgeyi HTML'ye kaydederken görüntüleri nasıl kaydettiğini kontrol etmek istiyorsanız bu arayüzü uygulayın. Diğer biçimler tarafından kullanılabilir.

```csharp
public interface IImageSavingCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ImageSaving](../../aspose.words.saving/iimagesavingcallback/imagesaving)(ImageSavingArgs) | Aspose.Words bir görüntüyü HTML'ye kaydettiğinde çağrılır. |

### Örnekler

Markdown belgesine kaydetme sırasında görüntü adının nasıl yeniden adlandırılacağını gösterir.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();

    // Görüntü içeren bir belgeyi Markdown'a dönüştürürsek, birkaç görüntüye bağlanan bir Markdown dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacaktır.
    // Her görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri arama da vardır.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");

    // Geri aramamızın ImageSaving() metodu bu sefer çalıştırılacaktır.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// Bir Markdown belgesi kaydedildiğinde oluşturulan kayıtlı görüntüleri yeniden adlandırır.
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

        args.ImageFileName = imageFileName;
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

Bir belgenin nasıl parçalara ayrılacağını ve kaydedileceğini gösterir.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Belgeyi normal bir şekilde kaydedersek, bir çıktı HTML olacaktır
    // tüm kaynak belgenin içeriğini içeren belge.
    // "DocumentSplitCriteria" özelliğini "DocumentSplitCriteria.SectionBreak" olarak ayarlayın.
    // belgemizi birden çok HTML dosyasına kaydedin: her bölüm için bir tane.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Belge parçası kaydetme mantığını değiştirmek için "DocumentPartSavingCallback" özelliğine özel bir geri arama atayın.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Görüntü içeren bir belgeyi html'ye dönüştürürsek, birkaç görüntüye bağlanan bir html dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacaktır.
    // Her görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri arama da vardır.
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
        // "Document" özelliği ile kaynak belgenin tamamına erişebiliriz.
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

        // Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıdadır.
        // 1 - Çıktı parça dosyası için bir dosya adı belirleyin:
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
/// Bir HTML dönüşümünün oluşturduğu görüntü dosyaları için özel dosya adları ayarlar.
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

        // Aspose.Words'ün belgenin her bir bölümünü nereye kaydedeceğini belirlemenin iki yolu aşağıdadır.
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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
