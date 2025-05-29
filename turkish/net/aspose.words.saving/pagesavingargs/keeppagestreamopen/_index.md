---
title: PageSavingArgs.KeepPageStreamOpen
linktitle: KeepPageStreamOpen
articleTitle: KeepPageStreamOpen
second_title: .NET için Aspose.Words
description: PageSavingArgs'daki KeepPageStreamOpen özelliğinin, optimum performans için akış davranışını kontrol ederek Aspose.Words ile belge yönetimini nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pagesavingargs/keeppagestreamopen/
---
## PageSavingArgs.KeepPageStreamOpen property

Aspose.Words'ün bir belge sayfasını kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir.

```csharp
public bool KeepPageStreamOpen { get; set; }
```

## Notlar

Varsayılan`YANLIŞ` ve Aspose.Words, sağladığınız akışı kapatacaktır [`PageStream`](../pagestream/) Bir belge sayfasını yazdıktan sonra özelliği belirtin. `doğru` akışı açık tutmak için.

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
