---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.CssSavingArgs sınıf. Şunun için veri sağlarCssSaving olay C#'da.
type: docs
weight: 4880
url: /tr/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Şunun için veri sağlar:[`CssSaving`](../icsssavingcallback/csssaving/) olay.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

```csharp
public class CssSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | CSS bilgilerinin kaydedileceği akışı belirtmeye izin verir. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Şu anda kaydedilmekte olan belge nesnesini alır. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | CSS'nin dosyaya aktarılıp aktarılmayacağını ve HTML belgesine gömülüp gömülmeyeceğini belirlemeye izin verir. Varsayılan:`doğru` . Bu özellik kullanıldığında`YANLIŞ` , CSS bilgileri bir CSS dosyasına kaydedilmeyecek ve HTML belgesine gömülmeyecektir. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Aspose.Words'ün CSS bilgilerini kaydettikten sonra akışı açık mı tutması yoksa kapatması mı gerektiğini belirtir. |

## Notlar

Varsayılan olarak Aspose.Words bir belgeyi HTML'ye kaydettiğinde CSS bilgilerini inline (bir değer olarak) kaydeder.**stil** her öğedeki özellik).

`CssSavingArgs`kendi akış nesnenizi sağlayarak CSS bilgilerini dosyaya kaydetmenize olanak tanır.

CSS'yi akışa kaydetmek için şunu kullanın:[`CssStream`](./cssstream/) mülk.

CSS'nin bir dosyaya kaydedilmesini ve HTML belgesine gömülmesini engellemek için şunu kullanın:[`IsExportNeeded`](./isexportneeded/) mülk.

## Örnekler

Bir HTML dönüşümünün oluşturduğu CSS stil sayfalarıyla nasıl çalışılacağını gösterir.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Belgenin "Save" yöntemine aktarabileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // "CssStylesheetType" özelliğini "CssStyleSheetType.External" olarak ayarlayın
    // kayıtlı bir HTML belgesine harici bir CSS stil sayfası dosyasıyla eşlik edin.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Aşağıda çıktı CSS stil sayfaları için dizinleri ve dosya adlarını belirtmenin iki yolu verilmiştir.
    // 1 - Stil sayfamıza bir dosya adı atamak için "CssStyleSheetFileName" özelliğini kullanın:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Stil sayfamızı adlandırmak için özel bir geri arama kullanın:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Harici bir CSS stil sayfası için diğer parametrelerle birlikte özel bir dosya adı belirler.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // Kaynak belgenin tamamına "Belge" özelliği aracılığıyla erişebiliriz.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
