---
title: HtmlSaveOptions.CssStyleSheetType
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: .NET için Aspose.Words
description: HtmlSaveOptions'daki CssStyleSheetType özelliğinin sorunsuz entegrasyon için CSS aktarımını HTML, MHTML ve EPUB formatlarına nasıl optimize ettiğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/htmlsaveoptions/cssstylesheettype/
---
## HtmlSaveOptions.CssStyleSheetType property

CSS (Basamaklı Stil Sayfası) stillerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını belirtir. Varsayılan değerInline HTML/MHTML ve içinExternal EPUB için.

```csharp
public CssStyleSheetType CssStyleSheetType { get; set; }
```

## Notlar

CSS stil sayfasını harici bir dosyaya kaydetmek yalnızca HTML'e kaydederken desteklenir. Kapsayıcı biçimlerinden birine (EPUB veya MHTML) dışa aktarırken ve belirtirkenExternal, CSS dosyası çıktı paketine encapsulated eklenecektir.

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

* property [CssStyleSheetFileName](../cssstylesheetfilename/)
* enum [CssStyleSheetType](../../cssstylesheettype/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
