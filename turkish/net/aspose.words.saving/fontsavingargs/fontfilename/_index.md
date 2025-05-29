---
title: FontSavingArgs.FontFileName
linktitle: FontFileName
articleTitle: FontFileName
second_title: .NET için Aspose.Words
description: FontSavingArgs FontFileName özelliğini keşfedin, font dosya adlarını kolayca yönetin ve sorunsuz kaydetme özellikleriyle tasarım iş akışınızı geliştirin.
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

Bu özellik, HTML'e aktarma sırasında font dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Bu özelliğin değerini değiştirerek yazı tipini farklı bir dosyaya kaydedebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, HTML biçimine aktarırken her gömülü font için otomatik olarak benzersiz bir dosya adı oluşturur. Font dosya adının nasıl oluşturulacağı , belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi bir dosyaya kaydederken, oluşturulan yazı tipi dosya adı gibi görünür&lt;belge temel dosya adı&gt;.&lt;orijinal dosya adı&gt;&lt;isteğe bağlı son ek&gt;.&lt;uzantı&gt;.

Bir belgeyi bir akışa kaydederken, oluşturulan yazı tipi dosya adı gibi görünürAspose.Words.&lt;belge kılavuzu&gt;.&lt;orijinal dosya adı&gt;&lt;isteğe bağlı ek&gt;.&lt;uzantı&gt;.

`FontFileName` yalnızca dosya adını içermelidir, yol hariç. Aspose.Words, belge dosya adını kullanarak kaydetme yolunu belirler, [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) ve [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) özellikler.

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
