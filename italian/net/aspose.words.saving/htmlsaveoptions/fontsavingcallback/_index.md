---
title: HtmlSaveOptions.FontSavingCallback
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Consente di controllare come vengono salvati i caratteri quando un documento viene salvato in HTML MHTML o EPUB.
type: docs
weight: 310
url: /it/net/aspose.words.saving/htmlsaveoptions/fontsavingcallback/
---
## HtmlSaveOptions.FontSavingCallback property

Consente di controllare come vengono salvati i caratteri quando un documento viene salvato in HTML, MHTML o EPUB.

```csharp
public IFontSavingCallback FontSavingCallback { get; set; }
```

### Esempi

Mostra come definire una logica personalizzata per l'esportazione dei caratteri durante il salvataggio in HTML.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configura un oggetto SaveOptions per esportare i caratteri in file separati.
    // Imposta una richiamata che gestirà il salvataggio dei caratteri in modo personalizzato.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // La richiamata esporterà i file .ttf e li salverà insieme al documento di output.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

/// <summary>
/// Stampa le informazioni sui caratteri esportati e li salva nella stessa cartella di sistema locale del file .html di output.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Possiamo anche accedere al documento sorgente da qui.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Esistono due modi per salvare un font esportato.
        // 1 - Salvalo in una posizione del file system locale:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Salvalo in un flusso:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Guarda anche

* interface [IFontSavingCallback](../../ifontsavingcallback/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


