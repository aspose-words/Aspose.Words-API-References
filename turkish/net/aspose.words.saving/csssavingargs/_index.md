---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: .NET için Aspose.Words
description: En iyi sonuçları elde etmek için özelleştirilebilir CssSaving olay verileriyle belge işlemenizi geliştirmek üzere tasarlanmış Aspose.Words.CssSavingArgs sınıfını keşfedin.
type: docs
weight: 5620
url: /tr/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Şunun için veri sağlar:[`CssSaving`](../icsssavingcallback/csssaving/) olay.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

```csharp
public class CssSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | CSS bilgilerinin kaydedileceği akışı belirtmenize olanak tanır. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Şu anda kaydedilmekte olan belge nesnesini alır. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | CSS'nin dosyaya aktarılıp aktarılmayacağını ve HTML belgesine yerleştirilip yerleştirilmeyeceğini belirtmeye olanak tanır. Varsayılan`doğru` . Bu özellik olduğunda`YANLIŞ` , CSS bilgisi bir CSS dosyasına kaydedilmeyecek ve HTML belgesine gömülmeyecektir. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Aspose.Words'ün CSS bilgilerini kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir. |

## Notlar

Varsayılan olarak, Aspose.Words bir belgeyi HTML'ye kaydettiğinde, CSS bilgilerini inline (bir değer olarak) kaydeder.**stil** her öğedeki öznitelik).

`CssSavingArgs` Kendi akış nesnenizi sağlayarak CSS bilgilerinin dosyaya kaydedilmesine olanak tanır.

CSS'yi akışa kaydetmek için şunu kullanın:[`CssStream`](./cssstream/) mülk.

CSS'yi bir dosyaya kaydetmeyi ve HTML belgesine yerleştirmeyi engellemek için şunu kullanın:[`IsExportNeeded`](./isexportneeded/) mülk.

## Örnekler

HTML dönüşümünün oluşturduğu CSS stil sayfalarıyla nasıl çalışılacağını gösterir.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // Belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // "CssStylesheetType" özelliğini "CssStyleSheetType.External" olarak ayarlayın
    // Kaydedilmiş bir HTML belgesine harici bir CSS stil sayfası dosyası eşlik eder.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Aşağıda çıktı CSS stil sayfaları için dizinleri ve dosya adlarını belirtmenin iki yolu bulunmaktadır.
    // 1 - Stil sayfamıza bir dosya adı atamak için "CssStyleSheetFileName" özelliğini kullanın:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Stil sayfamızı adlandırmak için özel bir geri arama kullanın:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Harici bir CSS stil sayfası için diğer parametrelerle birlikte özel bir dosya adı ayarlar.
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
        // "Belge" özelliği aracılığıyla kaynak belgenin tamamına erişebiliriz.
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
