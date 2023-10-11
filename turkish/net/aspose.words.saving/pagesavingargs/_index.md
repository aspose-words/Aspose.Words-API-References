---
title: Class PageSavingArgs
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PageSavingArgs sınıf. Şunun için veri sağlarPageSaving olay.
type: docs
weight: 5380
url: /tr/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Şunun için veri sağlar:[`PageSaving`](../ipagesavingcallback/pagesaving/) olay.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

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
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Aspose.Words'ün belge sayfasını kaydettikten sonra akışı açık mı tutması yoksa kapatması mı gerektiğini belirtir. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Belge sayfasının kaydedileceği dosya adını alır veya ayarlar. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Geçerli sayfa dizini. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Belge sayfasının kaydedileceği akışı belirtmeye izin verir. |

### Örnekler

Bir belgeyi sayfa sayfa HTML'ye kaydetmek için geri aramanın nasıl kullanılacağını gösterir.

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

    // Belgenin "Save" yöntemine aktarabileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Bu belgedeki her sayfayı yerel dosya sisteminde ayrı bir HTML dosyasına kaydedeceğiz.
    // Her çıktı HTML belgesini adlandırmamızı sağlayan bir geri çağırma ayarlayın.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Tüm sayfaları belirtilen dosya ve dizine kaydeder.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Aşağıda Aspose.Words'ün belgenin her sayfasını nereye kaydedeceğini belirtmenin iki yolu verilmiştir.
        // 1 - Çıkış sayfası dosyası için bir dosya adı belirleyin:
        args.PageFileName = outFileName;

        // 2 - Çıkış sayfası dosyası için özel bir akış oluşturun:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


