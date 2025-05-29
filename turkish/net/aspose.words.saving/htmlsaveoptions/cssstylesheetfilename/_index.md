---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: .NET için Aspose.Words
description: HtmlSaveOptions CssStyleSheetFileName özelliğinin, belirtilen CSS dosya yoluyla HTML dışa aktarımlarınızı nasıl özelleştirerek belgenizin stilini geliştirdiğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Bir belge HTML'e aktarıldığında yazılan Basamaklı Stil Sayfası (CSS) dosyasının yolunu ve adını belirtir. Varsayılan boş bir dizedir.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## Notlar

Bu özellik yalnızca bir belgeyi HTML formatı olarak kaydederken ve harici CSS stil sayfası kullanılarak istendiğinde etkilidir[`CssStyleSheetType`](../cssstylesheettype/).

Bu özellik boş bırakıldığında, CSS dosyası HTML belgesiyle aynı klasöre ve aynı adla ancak ".css" uzantısıyla kaydedilecektir.

Bu özellikte yalnızca yol belirtilir ancak dosya adı belirtilmezse, CSS dosyası belirtilen klasörüne kaydedilir ve HTML belgesiyle aynı ada sahip olur ancak ".css" uzantısına sahip olur.

Bu özellik tarafından belirtilen klasör mevcut değilse, CSS dosyası kaydedilmeden önce otomatik olarak oluşturulacaktır.

Harici CSS dosyasının kaydedileceği klasörü belirtmenin bir başka yolu da şunu kullanmaktır:[`ResourceFolder`](../resourcefolder/) .

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

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
