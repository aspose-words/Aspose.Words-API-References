---
title: MarkdownSaveOptions.ImageSavingCallback
second_title: Aspose.Words for .NET API Referansı
description: MarkdownSaveOptions mülk. Bir belge konumuna kaydedildiğinde resimlerin nasıl kaydedileceğini kontrol etmenizi sağlarMarkdown biçim.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/markdownsaveoptions/imagesavingcallback/
---
## MarkdownSaveOptions.ImageSavingCallback property

Bir belge konumuna kaydedildiğinde resimlerin nasıl kaydedileceğini kontrol etmenizi sağlarMarkdown biçim.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

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

### Ayrıca bakınız

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../markdownsaveoptions/)
* toplantı [Aspose.Words](../../../)


