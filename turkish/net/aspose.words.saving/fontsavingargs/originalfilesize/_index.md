---
title: FontSavingArgs.OriginalFileSize
linktitle: OriginalFileSize
articleTitle: OriginalFileSize
second_title: .NET için Aspose.Words
description: Orijinal yazı tipi dosya boyutunu etkili bir şekilde almak ve yazı tipi yönetimi deneyiminizi geliştirmek için FontSavingArgs OriginalFileSize özelliğini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words.saving/fontsavingargs/originalfilesize/
---
## FontSavingArgs.OriginalFileSize property

Orijinal yazı tipi dosya boyutunu alır.

```csharp
public int OriginalFileSize { get; }
```

## Notlar

Bu özellik, biliniyorsa geçerli yazı tipinin orijinal dosya boyutunu içerir. Aksi takdirde sıfır olabilir.

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

* class [FontSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
