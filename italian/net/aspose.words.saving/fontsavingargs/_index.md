---
title: FontSavingArgs
second_title: Aspose.Words per .NET API Reference
description: Fornisce i dati per ilFontSaving./ifontsavingcallback/fontsaving/ evento.
type: docs
weight: 4770
url: /it/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Fornisce i dati per il[`FontSaving`](../ifontsavingcallback/fontsaving/) evento.

```csharp
public class FontSavingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Indica se il carattere corrente è in grassetto. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Ottiene l'oggetto del documento che viene salvato. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Indica il nome della famiglia di font corrente. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Ottiene o imposta il nome del file (senza percorso) in cui verrà salvato il carattere. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Consente di specificare lo stream in cui verrà salvato il font. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Consente di specificare se il font corrente verrà esportato come risorsa font. L'impostazione predefinita è`VERO` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Consente di specificare se il font corrente verrà inserito in un sottoinsieme prima dell'esportazione come risorsa font. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Indica se il font corrente è in corsivo. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato un font. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Ottiene il nome del file del font originale con un'estensione. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Ottiene la dimensione del file del carattere originale. |

### Osservazioni

Quando Aspose.Words salva un documento in HTML o formati correlati e[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) è impostato su **VERO**, salva ogni oggetto del carattere per l'esportazione in un file separato.

`FontSavingArgs` controlla se una particolare risorsa di carattere deve essere esportata e come.

`FontSavingArgs`consente anche di ridefinire il modo in cui vengono generati i nomi dei file dei font o di eludere completamente il salvataggio dei font nei file fornendo i propri oggetti stream.

Per decidere se salvare una particolare risorsa di font, utilizzare il[`IsExportNeeded`](./isexportneeded/) proprietà.

Per salvare i caratteri negli stream anziché nei file, usa il file[`FontStream`](./fontstream/) proprietà.

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
