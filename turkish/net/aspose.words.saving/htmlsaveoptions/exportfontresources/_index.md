---
title: HtmlSaveOptions.ExportFontResources
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Yazı tipi kaynaklarının HTML MHTML veya EPUBa aktarılıp aktarılmayacağını belirtir. Varsayılanyanlış .
type: docs
weight: 150
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Yazı tipi kaynaklarının HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`yanlış` .

```csharp
public bool ExportFontResources { get; set; }
```

### Notlar

Yazı tipi kaynaklarının dışa aktarılması, belirli bir kullanıcının ortamında mevcut yazı tiplerinden bağımsız olarak tutarlı belge oluşturmayı sağlar.

Eğer`ExportFontResources` ayarlandı`doğru` , ana HTML belgesi CSS 3 aracılığıyla her yazı tipine atıfta bulunacaktır. **@ yazı tipi-yüz**at-rule ve yazı tipleri ayrı dosyalar olarak çıkarılacaktır. IDPF EPUB veya MHTML biçimlerine dışa aktarırken, yazı tipleri diğer yardımcı dosyalarla birlikte ilgili pakete gömülür.

Eğer[`ExportFontsAsBase64`](../exportfontsasbase64/) ayarlandı`doğru` , yazı tipleri ayrı dosyalara kaydedilmeyecek. Bunun yerine, **@ yazı tipi-yüz** Base64 kodlamasında at-kuralları.

**Önemli!** Yazı tipi kaynaklarını dışa aktarırken, yazı tipi lisanslama sorunları dikkate alınmalıdır. İndirilebilir yazı tipi mekanizması aracılığıyla belirli yazı tiplerini kullanmak isteyen yazarlar, kullanım amaçlarının yazı tipi lisansı kapsamında olduğunu her zaman dikkatli bir şekilde doğrulamalıdır. Şu anda birçok ticari yazı tipi, yazı tiplerinin herhangi bir biçimde web'den indirilmesine izin vermemektedir. Bazı yazı tiplerini kapsayan lisans sözleşmeleri, özellikle **@ yazı tipi-yüz** CSS stil sayfalarında kurallar 'ye izin verilmez. Yazı tipi alt kümesi, lisans koşullarını da ihlal edebilir.

### Örnekler

HTML'ye kaydederken yazı tiplerini dışa aktarmak için özel mantığın nasıl tanımlanacağını gösterir.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Fontları ayrı dosyalara aktarmak için bir SaveOptions nesnesi yapılandırın.
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

/// <summary>
/// Dışa aktarılan yazı tipleriyle ilgili bilgileri yazdırır ve bunları çıktıları .html ile aynı yerel sistem klasörüne kaydeder.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Kaynak belgeye buradan da ulaşabiliriz.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Dışa aktarılan bir yazı tipini kaydetmenin iki yolu vardır.
        // 1 - Yerel bir dosya sistemi konumuna kaydedin:
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


