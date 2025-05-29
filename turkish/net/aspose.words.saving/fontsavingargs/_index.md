---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.FontSavingArgs sınıfını keşfedin; üstün özelleştirme ve kontrol için ayrıntılı FontSaving olay verileriyle belge işlemeyi geliştirin.
type: docs
weight: 5780
url: /tr/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Şunun için veri sağlar:[`FontSaving`](../ifontsavingcallback/fontsaving/) olay.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

```csharp
public class FontSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Mevcut yazı tipinin kalın olup olmadığını gösterir. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Kaydedilen belge nesnesini alır. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Mevcut yazı tipi aile adını belirtir. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Yazı tipinin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Yazı tipinin kaydedileceği akışı belirtmenize olanak tanır. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Geçerli yazı tipinin bir yazı tipi kaynağı olarak dışa aktarılıp aktarılmayacağını belirtmenize olanak tanır. Varsayılan`doğru` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Geçerli yazı tipinin yazı tipi kaynağı olarak dışa aktarılmadan önce alt kümeye ayrılıp ayrılmayacağını belirtmeye olanak tanır. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Mevcut yazı tipinin italik olup olmadığını belirtir. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Aspose.Words'ün bir fontu kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Orijinal yazı tipi dosya adını uzantıyla birlikte alır. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Orijinal yazı tipi dosya boyutunu alır. |

## Notlar

Aspose.Words bir belgeyi HTML veya ilgili biçimlere kaydettiğinde ve[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) olarak ayarlandı`doğru`, her yazı tipi konusunu ayrı bir dosyaya aktarılmak üzere kaydeder.

`FontSavingArgs` Belirli bir yazı tipi kaynağının dışa aktarılıp aktarılmayacağını ve nasıl aktarılacağını kontrol eder.

`FontSavingArgs`Ayrıca, kendi akış nesnelerinizi sağlayarak font dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza veya fontların dosyalara kaydedilmesini tamamen engellemenize olanak tanır.

Belirli bir yazı tipi kaynağını kaydedip kaydetmemeye karar vermek için şunu kullanın:[`IsExportNeeded`](./isexportneeded/) mülk.

Yazı tiplerini dosyalar yerine akışlara kaydetmek için şunu kullanın:[`FontStream`](./fontstream/) mülk.

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
