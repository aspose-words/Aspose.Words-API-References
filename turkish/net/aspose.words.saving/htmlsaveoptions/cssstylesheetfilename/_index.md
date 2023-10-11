---
title: HtmlSaveOptions.CssStyleSheetFileName
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Bir document HTMLye aktarıldığında yazılan Basamaklı Stil Sayfası CSS dosyasının yolunu ve adını belirtir. Varsayılan boş bir dizedir.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Bir document HTML'ye aktarıldığında yazılan Basamaklı Stil Sayfası (CSS) dosyasının yolunu ve adını belirtir. Varsayılan, boş bir dizedir.

```csharp
public string CssStyleSheetFileName { get; set; }
```

### Notlar

Bu özellik yalnızca bir belge HTML biçiminde kaydedildiğinde ve harici CSS stil sayfası kullanılarak istendiğinde etkili olur.[`CssStyleSheetType`](../cssstylesheettype/).

Bu özellik boşsa, CSS dosyası HTML belgesiyle aynı klasöre ve aynı adla ancak ".css" uzantısıyla kaydedilecektir.

Bu özellikte yalnızca yol belirtilir ancak dosya adı belirtilmezse, CSS dosyası belirtilen klasörüne kaydedilecek ve HTML belgesiyle aynı adı taşıyacak ancak ".css" uzantısına sahip olacaktır.

Bu özellik tarafından belirtilen klasör mevcut değilse, CSS file kaydedilmeden önce otomatik olarak oluşturulacaktır.

Harici CSS dosyasının kaydedildiği klasörü belirtmenin başka bir yolu da kullanmaktır.[`ResourceFolder`](../resourcefolder/) .

### Örnekler

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

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


