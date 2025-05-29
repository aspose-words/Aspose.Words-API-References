---
title: CssSavingArgs.CssStream
linktitle: CssStream
articleTitle: CssStream
second_title: .NET için Aspose.Words
description: CSSSavingArgs CssStream özelliğiyle CSS depolamanızı optimize ederek CSS verilerinizin tercih ettiğiniz akışa sorunsuz bir şekilde kaydedilmesini sağlayın.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

CSS bilgilerinin kaydedileceği akışı belirtmenize olanak tanır.

```csharp
public Stream CssStream { get; set; }
```

## Notlar

Bu özellik CSS bilgilerini bir akışa kaydetmenize olanak tanır.

Varsayılan değer:`hükümsüz` Bu özellik, CSS bilgilerinin bir dosyaya kaydedilmesini veya HTML belgesine gömülmesini engellemez. CSS'nin dışa aktarılmasını engellemek için şunu kullanın:[`IsExportNeeded`](../isexportneeded/) mülk.

Kullanarak[`ICssSavingCallback`](../../icsssavingcallback/) CSS'yi ile değiştiremezsiniz. Bu yalnızca CSS'yi bir akışa kaydetmek için tasarlanmıştır.

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

* class [CssSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
