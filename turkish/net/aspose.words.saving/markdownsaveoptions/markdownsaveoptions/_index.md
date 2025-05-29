---
title: MarkdownSaveOptions
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: .NET için Aspose.Words
description: Belgeleri Markdown formatında zahmetsizce kaydetmek için MarkdownSaveOptions oluşturucusunu keşfedin. Bu temel araçla iş akışınızı kolaylaştırın.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/markdownsaveoptions/markdownsaveoptions/
---
## MarkdownSaveOptions constructor

Bu sınıfın, bir document dosyasını kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Markdown biçim.

```csharp
public MarkdownSaveOptions()
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

* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
