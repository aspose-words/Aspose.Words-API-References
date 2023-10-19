---
title: CssSavingArgs.IsExportNeeded
linktitle: IsExportNeeded
articleTitle: IsExportNeeded
second_title: Aspose.Words for .NET
description: CssSavingArgs IsExportNeeded mülk. CSSnin dosyaya aktarılıp aktarılmayacağını ve HTML belgesine gömülüp gömülmeyeceğini belirlemeye izin verir. Varsayılandoğru . Bu özellik kullanıldığındaYANLIŞ  CSS bilgileri bir CSS dosyasına kaydedilmeyecek ve HTML belgesine gömülmeyecektir C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/csssavingargs/isexportneeded/
---
## CssSavingArgs.IsExportNeeded property

CSS'nin dosyaya aktarılıp aktarılmayacağını ve HTML belgesine gömülüp gömülmeyeceğini belirlemeye izin verir. Varsayılan:`doğru` . Bu özellik kullanıldığında`YANLIŞ` , CSS bilgileri bir CSS dosyasına kaydedilmeyecek ve HTML belgesine gömülmeyecektir.

```csharp
public bool IsExportNeeded { get; set; }
```

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

* class [CssSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
