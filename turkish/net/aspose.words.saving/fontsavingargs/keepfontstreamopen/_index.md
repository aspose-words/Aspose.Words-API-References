---
title: FontSavingArgs.KeepFontStreamOpen
linktitle: KeepFontStreamOpen
articleTitle: KeepFontStreamOpen
second_title: .NET için Aspose.Words
description: FontSavingArgs'daki KeepFontStreamOpen özelliğinin Aspose.Words'ün yazı tipi akışlarını verimli bir şekilde yönetmesini ve belge işleme deneyiminizi geliştirmesini nasıl sağladığını keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/fontsavingargs/keepfontstreamopen/
---
## FontSavingArgs.KeepFontStreamOpen property

Aspose.Words'ün bir fontu kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir.

```csharp
public bool KeepFontStreamOpen { get; set; }
```

## Notlar

Varsayılan`YANLIŞ` ve Aspose.Words, sağladığınız akışı kapatacaktır [`FontStream`](../fontstream/) içine bir yazı tipi yazdıktan sonra özellik. Belirtin`doğru` akışı açık tutmak için.

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
