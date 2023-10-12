---
title: Class FontSavingArgs
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.FontSavingArgs sınıf. Şunun için veri sağlarFontSaving olay.
type: docs
weight: 5030
url: /tr/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Şunun için veri sağlar:[`FontSaving`](../ifontsavingcallback/fontsaving/) olay.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

```csharp
public class FontSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Geçerli yazı tipinin kalın olup olmadığını belirtir. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Kaydedilen belge nesnesini alır. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Geçerli yazı tipi ailesinin adını belirtir. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Yazı tipinin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Yazı tipinin kaydedileceği akışı belirtmeye izin verir. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Geçerli yazı tipinin yazı tipi kaynağı olarak dışa aktarılıp aktarılmayacağını belirlemeye olanak tanır. Varsayılan:`doğru` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Geçerli yazı tipinin, bir yazı tipi kaynağı olarak dışa aktarılmadan önce alt kümeye alınıp alınmayacağını belirlemeye izin verir. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Geçerli yazı tipinin italik olup olmadığını belirtir. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Aspose.Words'ün bir yazı tipini kaydettikten sonra akışı açık mı tutması yoksa kapatması mı gerektiğini belirtir. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Uzantısıyla orijinal yazı tipi dosyasının adını alır. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Orijinal yazı tipi dosyasının boyutunu alır. |

### Notlar

Aspose.Words bir belgeyi HTML'ye veya ilgili formatlara kaydettiğinde ve[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) şu şekilde ayarlandı`doğru`, her yazı tipi konusunu dışa aktarılmak üzere ayrı bir dosyaya kaydeder.

`FontSavingArgs` belirli yazı tipi kaynağının dışa aktarılıp aktarılmayacağını ve nasıl dışa aktarılacağını kontrol eder.

`FontSavingArgs`ayrıca yazı tipi dosyası adlarının nasıl oluşturulduğunu yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak yazı tiplerinin dosyalara kaydedilmesini tamamen engellemenize olanak tanır.

Belirli bir yazı tipi kaynağının kaydedilip kaydedilmeyeceğine karar vermek için[`IsExportNeeded`](./isexportneeded/) mülk.

Yazı tiplerini dosyalar yerine akışlara kaydetmek için[`FontStream`](./fontstream/) mülk.

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


