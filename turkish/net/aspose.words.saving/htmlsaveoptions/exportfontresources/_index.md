---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: .NET için Aspose.Words
description: HTML, MHTML veya EPUB için font kaynağı dışa aktarımını kontrol etmek için HtmlSaveOptions ExportFontResources özelliğini keşfedin. Belgenizin görsel çekiciliğini en üst düzeye çıkarın!
type: docs
weight: 140
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Yazı tipi kaynaklarının HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool ExportFontResources { get; set; }
```

## Notlar

Yazı tipi kaynaklarının dışa aktarılması, belirli bir kullanıcının ortamındaki mevcut yazı tiplerinden bağımsız olarak tutarlı belge oluşturulmasına olanak tanır.

Eğer`ExportFontResources` ayarlandı`doğru` , ana HTML belgesi CSS 3 aracılığıyla her yazı tipine başvuracaktır**@yazı-yüzü** at-rule ve fontlar ayrı dosyalar olarak çıktı olarak verilecektir. IDPF EPUB veya MHTML biçimlerine dışa aktarırken, fontlar diğer yardımcı dosyalarla birlikte ilgili pakete gömülecektir.

Eğer[`ExportFontsAsBase64`](../exportfontsasbase64/) ayarlandı`doğru` , yazı tipleri ayrı dosyalara kaydedilmeyecektir. Bunun yerine, bunlar**@yazı-yüzü** Base64 kodlamasında at-kuralları.

**Önemli!**Font kaynaklarını dışa aktarırken, font lisanslama sorunları dikkate alınmalıdır. Belirli fontları downloadable font mekanizması aracılığıyla kullanmak isteyen yazarlar, amaçlanan kullanımlarının font lisansının kapsamında olduğundan her zaman dikkatlice emin olmalıdır. Birçok ticari font şu anda fontlarının herhangi bir biçimde web üzerinden indirilmesine izin vermemektedir. Bazı fontları kapsayan lisans sözleşmeleri, özellikle kullanımın**@yazı-yüzü** CSS stil sayfalarında rules izin verilmez. Yazı tipi alt kümelemesi de lisans koşullarını ihlal edebilir.

## Örnekler

HTML'e kaydederken yazı tiplerini dışa aktarmak için özel mantığın nasıl tanımlanacağını gösterir.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Yazı tiplerini ayrı dosyalara aktarmak için bir SaveOptions nesnesi yapılandırın.
    // Yazı tipi kaydetmeyi özel bir şekilde işleyecek bir geri çağırma ayarlayın.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Geri arama .ttf dosyalarını dışa aktaracak ve bunları çıktı belgesinin yanına kaydedecektir.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Dışa aktarılan yazı tipleri hakkında bilgi yazdırır ve bunları çıktı .html'leriyle aynı yerel sistem klasörüne kaydeder.
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
        // 1 - Bunu yerel bir dosya sistemi konumuna kaydedin:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Bunu bir akışa kaydedin:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
