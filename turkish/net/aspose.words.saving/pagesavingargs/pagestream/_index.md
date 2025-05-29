---
title: PageSavingArgs.PageStream
linktitle: PageStream
articleTitle: PageStream
second_title: .NET için Aspose.Words
description: Verimli dosya yönetimi için istediğiniz akışa sorunsuz belge sayfası kaydetmeyi sağlayan PageSavingArgs'ın PageStream özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/pagesavingargs/pagestream/
---
## PageSavingArgs.PageStream property

Belge sayfasının kaydedileceği akışı belirtmenize olanak tanır.

```csharp
public Stream PageStream { get; set; }
```

## Notlar

Bu özellik, belge sayfalarını dosyalar yerine akışlara kaydetmenize olanak tanır.

Varsayılan değer:`hükümsüz` Bu özellik olduğunda`hükümsüz` , belge sayfası belirtilen bir dosyaya kaydedilecektir.[`PageFileName`](../pagefilename/) mülk.

Eğer ikisi de`PageStream` Ve[`PageFileName`](../pagefilename/) ayarlanırsa, PageStream kullanılacaktır.

## Örnekler

Bir belgeyi sayfa sayfa HTML olarak kaydetmek için geri aramanın nasıl kullanılacağını gösterir.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // Belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Bu belgedeki her sayfayı yerel dosya sistemindeki ayrı bir HTML dosyasına kaydedeceğiz.
    // Her çıktı HTML belgesine isim vermemizi sağlayacak bir geri çağırma ayarlayın.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Tüm sayfaları belirtilen bir dosyaya ve dizine kaydeder.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Aşağıda Aspose.Words'ün belgenin her sayfasını nereye kaydedeceğini belirtmenin iki yolu bulunmaktadır.
        // 1 - Çıktı sayfası dosyası için bir dosya adı belirleyin:
        args.PageFileName = outFileName;

        // 2 - Çıktı sayfası dosyası için özel bir akış oluşturun:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Ayrıca bakınız

* class [PageSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
