---
title: FontSavingArgs.FontFileName
second_title: Aspose.Words per .NET API Reference
description: FontSavingArgs proprietà. Ottiene o imposta il nome del file senza percorso in cui verrà salvato il carattere.
type: docs
weight: 40
url: /it/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Ottiene o imposta il nome del file (senza percorso) in cui verrà salvato il carattere.

```csharp
public string FontFileName { get; set; }
```

### Osservazioni

Questa proprietà consente di ridefinire il modo in cui i nomi dei file dei font vengono generati durante l'esportazione in HTML.

Quando l'evento viene generato, questa proprietà contiene il nome del file che è stato generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare il carattere in un file diverso. Tieni presente che i nomi dei file devono essere univoci.

Aspose.Words genera automaticamente un nome file univoco per ogni font incorporato durante l'esportazione di in formato HTML. La modalità di generazione del nome del file del carattere dipende dal fatto che il documento venga salvato in un file o in un flusso.

Quando si salva un documento in un file, il nome del file del carattere generato è simile a &lt;nome file base documento&gt;.&lt;nome file originale&gt;&lt;suffisso opzionale&gt;.&lt;estensione&gt;.

Quando si salva un documento in uno stream, il nome del file del font generato è simile a Aspose.Words.&lt;document guid&gt;.&lt;nome file originale&gt;&lt;suffisso opzionale&gt;.&lt;estensione&gt;.

`FontFileName` deve contenere solo il nome del file senza il percorso. Aspose.Words determina il percorso per il salvataggio utilizzando il nome del file del documento, il[`FontsFolder`](../../htmlsaveoptions/fontsfolder/) e [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) proprietà.

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

* class [FontSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../fontsavingargs/)
* assemblea [Aspose.Words](../../../)


