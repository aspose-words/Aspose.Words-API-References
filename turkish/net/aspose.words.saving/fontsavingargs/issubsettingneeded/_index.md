---
title: FontSavingArgs.IsSubsettingNeeded
second_title: Aspose.Words for .NET API Referansı
description: FontSavingArgs mülk. Geçerli yazı tipinin bir yazı tipi kaynağı olarak dışa aktarılmadan önce alt kümeye alınıp alınmayacağını belirlemeye izin verir.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/fontsavingargs/issubsettingneeded/
---
## FontSavingArgs.IsSubsettingNeeded property

Geçerli yazı tipinin, bir yazı tipi kaynağı olarak dışa aktarılmadan önce alt kümeye alınıp alınmayacağını belirlemeye izin verir.

```csharp
public bool IsSubsettingNeeded { get; set; }
```

### Notlar

Yazı tipleri, tam orijinal yazı tipi dosyaları olarak dışa aktarılabilir veya yalnızca belgede kullanılan karakterleri içerecek şekilde alt kümelere ayrılabilir. Alt kümeleme, ortaya çıkan yazı tipi kaynağı boyutunun azaltılmasına olanak tanır.

Varsayılan olarak Aspose.Words, orijinal yazı tipi dosyasının boyutunu şurada belirtilenle karşılaştırarak alt kümeleme yapılıp yapılmayacağına karar verir.[`FontResourcesSubsettingSizeThreshold`](../../htmlsaveoptions/fontresourcessubsettingsizethreshold/) . Tek tek yazı tipleri için bu davranışı geçersiz kılabilirsiniz.`IsSubsettingNeeded` mülk.

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

* class [FontSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../fontsavingargs/)
* toplantı [Aspose.Words](../../../)


