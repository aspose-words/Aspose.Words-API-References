---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: .NET için Aspose.Words
description: Ayrıntılı PageSaving olay verileriyle belge işlemeyi optimize etmek için gerekli olan Aspose.Words.Saving.PageSavingArgs sınıfını keşfedin. İş akışınızı geliştirin!
type: docs
weight: 6160
url: /tr/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Şunun için veri sağlar:[`PageSaving`](../ipagesavingcallback/pagesaving/) olay.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class PageSavingArgs
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Aspose.Words'ün bir belge sayfasını kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Belge sayfasının kaydedileceği dosya adını alır veya ayarlar. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Mevcut sayfa dizini. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Belge sayfasının kaydedileceği akışı belirtmenize olanak tanır. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
