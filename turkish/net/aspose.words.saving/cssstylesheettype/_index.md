---
title: CssStyleSheetType Enum
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: .NET için Aspose.Words
description: Aspose.Words.CssStyleSheetType'ın daha iyi web sunumu ve performansı için CSS stillerini optimize ederek HTML dışa aktarımını nasıl geliştirdiğini keşfedin.
type: docs
weight: 5630
url: /tr/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

CSS (Basamaklı Stil Sayfası) stillerinin HTML'ye nasıl aktarılacağını belirtir.

```csharp
public enum CssStyleSheetType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Inline | `0` | CSS stilleri satır içi olarak yazılır (bir değer olarak)**stil** her öğedeki öznitelik). |
| Embedded | `1` | CSS stilleri, HTML dosyasına gömülü bir stil sayfasında içerikten ayrı olarak yazılır. |
| External | `2` | CSS stilleri, harici bir dosyadaki stil sayfasındaki içerikten ayrı olarak yazılır. HTML dosyası, stil sayfasına bağlanır. |

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

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
