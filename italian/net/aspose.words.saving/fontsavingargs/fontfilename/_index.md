---
title: FontSavingArgs.FontFileName
linktitle: FontFileName
articleTitle: FontFileName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontFileName di FontSavingArgs, gestisci facilmente i nomi dei file dei font e migliora il tuo flusso di lavoro di progettazione con funzionalità di salvataggio fluide.
type: docs
weight: 40
url: /it/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Ottiene o imposta il nome del file (senza percorso) in cui verrà salvato il font.

```csharp
public string FontFileName { get; set; }
```

## Osservazioni

Questa proprietà consente di ridefinire il modo in cui vengono generati i nomi dei file dei font durante l'esportazione in HTML.

Quando l'evento viene attivato, questa proprietà contiene il nome del file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare il font in un file diverso. Si noti che i nomi dei file devono essere univoci.

Aspose.Words genera automaticamente un nome file univoco per ogni font incorporato durante l'esportazione in formato HTML. La modalità di generazione del nome file del font varia a seconda che il documento venga salvato in un file o in un flusso.

Quando si salva un documento in un file, il nome del file del font generato appare come &lt;nome file base documento&gt;.&lt;nome file originale&gt;&lt;suffisso facoltativo&gt;.&lt;estensione&gt;.

Quando si salva un documento in un flusso, il nome del file del font generato appare come Aspose.Words.&lt;guid documento&gt;.&lt;nome file originale&gt;&lt;suffisso facoltativo&gt;.&lt;estensione&gt;.

`FontFileName` deve contenere solo il nome del file senza il percorso. Aspose.Words determina il percorso per il salvataggio utilizzando il nome del file del documento, [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) e [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) proprietà.

## Esempi

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configura un oggetto SaveOptions per esportare i font in file separati.
    // Imposta un callback che gestirà il salvataggio dei font in modo personalizzato.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Il callback esporterà i file .ttf e li salverà insieme al documento di output.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Stampa informazioni sui font esportati e li salva nella stessa cartella di sistema locale del loro output .html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Da qui possiamo anche accedere al documento sorgente.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Esistono due modi per salvare un font esportato.
        // 1 - Salvalo in una posizione del file system locale:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Salvalo in uno stream:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Guarda anche

* class [FontSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
