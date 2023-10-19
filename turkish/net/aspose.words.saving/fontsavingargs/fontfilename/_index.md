---
title: FontSavingArgs.FontFileName
linktitle: FontFileName
articleTitle: FontFileName
second_title: Aspose.Words for .NET
description: FontSavingArgs FontFileName mülk. Yazı tipinin kaydedileceği dosya adını yol olmadan alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Yazı tipinin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar.

```csharp
public string FontFileName { get; set; }
```

## Notlar

Bu özellik, HTML'ye dışa aktarma sırasında yazı tipi dosya adlarının nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Etkinlik başlatıldığında bu özellik, Aspose.Words tarafından oluşturulan dosya adını içerir. Yazı tipini farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, HTML formatına aktarıldığında her gömülü yazı tipi için otomatik olarak benzersiz bir dosya adı oluşturur. yazı tipi dosyası adının nasıl oluşturulduğu, belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi bir dosyaya kaydederken oluşturulan yazı tipi dosyasının adı gibi görünür&lt;belge temel dosya adı&gt;.&lt;orijinal dosya adı&gt;&lt;isteğe bağlı sonek&gt;.&lt;uzantı&gt;.

Bir belgeyi bir akışa kaydederken oluşturulan yazı tipi dosyasının adı gibi görünürAspose.Words.&lt;belge guid'i&gt;.&lt;orijinal dosya adı&gt;&lt;isteğe bağlı son ek&gt;.&lt;uzantı&gt;.

`FontFileName` yol olmadan yalnızca dosya adını içermelidir. Aspose.Words, belge dosya adını kullanarak kaydetme yolunu belirler, [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) ve [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) özellikler.

## Örnekler

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

* class [FontSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
