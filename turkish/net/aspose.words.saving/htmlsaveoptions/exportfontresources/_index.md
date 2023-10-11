---
title: HtmlSaveOptions.ExportFontResources
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Yazı tipi kaynaklarının HTMLye mi MHTMLye mi yoksa EPUBa mı aktarılacağını belirtir. VarsayılanYANLIŞ .
type: docs
weight: 140
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Yazı tipi kaynaklarının HTML'ye mi, MHTML'ye mi yoksa EPUB'a mı aktarılacağını belirtir. Varsayılan:`YANLIŞ` .

```csharp
public bool ExportFontResources { get; set; }
```

### Notlar

Yazı tipi kaynaklarının dışa aktarılması, belirli bir kullanıcı ortamında mevcut yazı tiplerinden bağımsız olarak tutarlı belge oluşturmaya olanak tanır.

Eğer`ExportFontResources` ayarlandı`doğru` , ana HTML belgesi CSS 3'teki aracılığıyla her yazı tipine atıfta bulunacaktır **@yazı tipi yüzü** at-rule ve yazı tipleri ayrı dosyalar olarak yayınlanacaktır. IDPF EPUB veya MHTML formatlarına dışa aktarırken yazı tipleri, diğer yardımcı dosyalarla birlikte ilgili pakete eklenecektir.

Eğer[`ExportFontsAsBase64`](../exportfontsasbase64/) ayarlandı`doğru` yazı tipleri ayrı dosyalara kaydedilmeyecektir. Bunun yerine, yazı tipleri ayrı dosyalara kaydedilmeyecektir. **@yazı tipi yüzü** Base64 kodlamasında kurallarda.

**Önemli!** Yazı tipi kaynaklarını dışa aktarırken yazı tipi lisanslama sorunları dikkate alınmalıdır. Downloadable yazı tipi mekanizması aracılığıyla belirli yazı tiplerini kullanmak isteyen yazarların, kullanım amaçlarının yazı tipi lisansı kapsamında olduğunu her zaman dikkatli bir şekilde doğrulamaları gerekir. Pek çok ticari yazı tipi şu anda kendi yazı tiplerinin herhangi bir biçimde web'den indirilmesine izin vermemektedir. Bazı yazı tiplerini kapsayan lisans sözleşmeleri, özellikle şunu belirtir: **@yazı tipi yüzü** CSS stil sayfalarında Rules 'ye izin verilmiyor. Yazı tipi alt kümelemesi aynı zamanda lisans koşullarını da ihlal edebilir.

### Örnekler

HTML'ye kaydederken yazı tiplerini dışa aktarmak için özel mantığın nasıl tanımlanacağını gösterir.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Yazı tiplerini ayrı dosyalara aktarmak için bir SaveOptions nesnesi yapılandırın.
    // Yazı tipi kaydetmeyi özel bir şekilde gerçekleştirecek bir geri arama ayarlayın.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Geri arama, .ttf dosyalarını dışa aktaracak ve bunları çıktı belgesinin yanına kaydedecektir.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Dışa aktarılan yazı tipleri hakkındaki bilgileri yazdırır ve bunları çıktı .html'leriyle aynı yerel sistem klasörüne kaydeder.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Kaynak dokümana buradan da ulaşabiliriz.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Dışa aktarılan bir yazı tipini kaydetmenin iki yolu vardır.
        // 1 - Yerel dosya sistemi konumuna kaydedin:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Bir akışa kaydedin:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


