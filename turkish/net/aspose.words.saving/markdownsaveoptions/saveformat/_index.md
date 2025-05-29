---
title: MarkdownSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: MarkdownSaveOptions SaveFormat özelliğini kullanarak belgeleri Markdown formatında zahmetsizce kaydedebilir, uyumluluğu ve kullanım kolaylığını garantileyebilirsiniz.
type: docs
weight: 130
url: /tr/net/aspose.words.saving/markdownsaveoptions/saveformat/
---
## MarkdownSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaMarkdown .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

Markdown belgesine kaydederken resim adının nasıl değiştirileceğini gösterir.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Resim içeren bir belgeyi Markdown'a dönüştürürsek, birden fazla resme bağlantı veren tek bir Markdown dosyası elde ederiz.
    // Her görüntü yerel dosya sisteminde bir dosya biçiminde olacak.
    // Ayrıca her bir görüntünün adını ve dosya sistemi konumunu özelleştirebilen bir geri çağırma da vardır.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // Geri aramamızın ImageSaving() metodu bu anda çalıştırılacak.
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
/// Bir Markdown belgesi kaydedildiğinde üretilen kaydedilmiş görüntüleri yeniden adlandırır.
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
