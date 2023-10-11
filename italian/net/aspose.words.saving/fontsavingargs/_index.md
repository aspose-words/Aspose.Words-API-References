---
title: Class FontSavingArgs
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.FontSavingArgs classe. Fornisce i dati per ilFontSaving evento.
type: docs
weight: 5030
url: /it/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Fornisce i dati per il[`FontSaving`](../ifontsavingcallback/fontsaving/) evento.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class FontSavingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Indica se il carattere corrente è in grassetto. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Ottiene l'oggetto documento che viene salvato. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Indica il nome della famiglia di caratteri corrente. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Ottiene o imposta il nome del file (senza percorso) in cui verrà salvato il carattere. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Permette di specificare lo stream in cui verrà salvato il carattere. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Permette di specificare se il carattere corrente verrà esportato come risorsa carattere. L'impostazione predefinita è`VERO` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Permette di specificare se il carattere corrente verrà sottoinsieme prima dell'esportazione come risorsa carattere. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Indica se il carattere corrente è corsivo. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Specifica se Aspose.Words deve mantenere aperto lo stream o chiuderlo dopo aver salvato un font. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Ottiene il nome del file del carattere originale con un'estensione. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Ottiene la dimensione del file del carattere originale. |

### Osservazioni

Quando Aspose.Words salva un documento in HTML o formati correlati e[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) è impostato su`VERO`, salva ciascun oggetto del carattere per l'esportazione in un file separato.

`FontSavingArgs` controlla se una particolare risorsa di carattere deve essere esportata e come.

`FontSavingArgs`consente inoltre di ridefinire il modo in cui vengono generati i nomi dei file di caratteri o di eludere completamente il salvataggio dei caratteri nei file fornendo i propri oggetti di flusso.

Per decidere se salvare una particolare risorsa di carattere, utilizzare il file[`IsExportNeeded`](./isexportneeded/) proprietà.

Per salvare i caratteri in flussi anziché in file, utilizzare il file[`FontStream`](./fontstream/) proprietà.

### Esempi

Mostra come definire la logica personalizzata per l'esportazione dei caratteri durante il salvataggio in HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configura un oggetto SaveOptions per esportare i caratteri in file separati.
    // Imposta un callback che gestirà il salvataggio dei caratteri in modo personalizzato.
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

}

/// <summary>
/// Stampa le informazioni sui caratteri esportati e le salva nella stessa cartella di sistema locale del file .html di output.
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

        // Esistono due modi per salvare un carattere esportato.
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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


