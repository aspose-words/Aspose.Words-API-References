---
title: Class FontSavingArgs
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.FontSavingArgs sınıf. için veri sağlarFontSaving olay.
type: docs
weight: 4770
url: /tr/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

için veri sağlar[`FontSaving`](../ifontsavingcallback/fontsaving/) olay.

```csharp
public class FontSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Geçerli yazı tipinin kalın olup olmadığını gösterir. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Kaydedilen belge nesnesini alır. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Geçerli yazı tipi aile adını gösterir. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Yazı tipinin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Yazı tipinin kaydedileceği akışı belirtmeye izin verir. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Geçerli yazı tipinin bir yazı tipi kaynağı olarak dışa aktarılıp aktarılmayacağını belirlemeye izin verir. Varsayılan`doğru` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Bir yazı tipi kaynağı olarak dışa aktarmadan önce mevcut yazı tipinin alt kümelenip alt küme oluşturulmayacağını belirlemeye izin verir. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Geçerli yazı tipinin italik olup olmadığını gösterir. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Aspose.Words'ün bir fontu kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Bir uzantıyla orijinal yazı tipi dosya adını alır. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Orijinal yazı tipi dosya boyutunu alır. |

### Notlar

Aspose.Words bir belgeyi HTML veya ilgili formatlara kaydettiğinde ve[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) olarak ayarlandı **doğru**, her yazı tipi konusunu ayrı bir dosyaya dışa aktarmak için kaydeder.

`FontSavingArgs` belirli bir yazı tipi kaynağının dışa aktarılıp aktarılmayacağını ve nasıl yapılacağını kontrol eder.

`FontSavingArgs`ayrıca yazı tipi dosya adlarının nasıl oluşturulduğunu yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak yazı tiplerinin dosyalara kaydedilmesini tamamen engellemenize olanak tanır.

Belirli bir yazı tipi kaynağını kaydedip kaydetmemeye karar vermek için[`IsExportNeeded`](./isexportneeded/) Emlak.

Yazı tiplerini dosyalar yerine akışlara kaydetmek için[`FontStream`](./fontstream/) Emlak.

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


