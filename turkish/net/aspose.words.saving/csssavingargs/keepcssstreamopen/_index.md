---
title: CssSavingArgs.KeepCssStreamOpen
linktitle: KeepCssStreamOpen
articleTitle: KeepCssStreamOpen
second_title: Aspose.Words for .NET
description: CssSavingArgs KeepCssStreamOpen mülk. Aspose.Wordsün CSS bilgilerini kaydettikten sonra akışı açık mı tutması yoksa kapatması mı gerektiğini belirtir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/csssavingargs/keepcssstreamopen/
---
## CssSavingArgs.KeepCssStreamOpen property

Aspose.Words'ün CSS bilgilerini kaydettikten sonra akışı açık mı tutması yoksa kapatması mı gerektiğini belirtir.

```csharp
public bool KeepCssStreamOpen { get; set; }
```

## Notlar

Varsayılan:`YANLIŞ` ve Aspose.Words, sağladığınız akışını kapatacaktır.[`CssStream`](../cssstream/) içine bir CSS bilgisi yazdıktan sonra özellik. Belirt`doğru` Akışı açık tutmak için.

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
