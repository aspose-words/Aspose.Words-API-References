---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.FontSavingArgs migliora l'elaborazione dei documenti con dati dettagliati sugli eventi FontSaving per una personalizzazione e un controllo superiori.
type: docs
weight: 5780
url: /it/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Fornisce dati per il[`FontSaving`](../ifontsavingcallback/fontsaving/) evento.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class FontSavingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Indica se il carattere corrente è in grassetto. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Ottiene l'oggetto documento che viene salvato. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Indica il nome della famiglia di font corrente. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Ottiene o imposta il nome del file (senza percorso) in cui verrà salvato il font. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Consente di specificare il flusso in cui verrà salvato il font. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Consente di specificare se il font corrente verrà esportato come risorsa font. Il valore predefinito è`VERO` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Consente di specificare se il font corrente verrà sottoposto a sottoinsieme prima dell'esportazione come risorsa font. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Indica se il carattere corrente è corsivo. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Specifica se Aspose.Words deve mantenere aperto il flusso o chiuderlo dopo aver salvato un font. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Ottiene il nome del file del font originale con estensione . |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Ottiene la dimensione originale del file del font. |

## Osservazioni

Quando Aspose.Words salva un documento in HTML o in formati correlati e[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) è impostato su`VERO`, salva ogni tipo di font per l'esportazione in un file separato.

`FontSavingArgs` controlla se una particolare risorsa di font deve essere esportata e come.

`FontSavingArgs`consente inoltre di ridefinire il modo in cui vengono generati i nomi dei file dei font o di aggirare completamente il salvataggio dei font nei file fornendo i propri oggetti stream.

Per decidere se salvare una particolare risorsa di font, utilizzare[`IsExportNeeded`](./isexportneeded/) proprietà.

Per salvare i font in flussi anziché in file, utilizzare[`FontStream`](./fontstream/) proprietà.

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
