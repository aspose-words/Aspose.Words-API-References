---
title: IFontSavingCallback Interface
linktitle: IFontSavingCallback
articleTitle: IFontSavingCallback
second_title: Aspose.Words per .NET
description: Controlla il salvataggio dei font in Aspose.Words con l'interfaccia IFontSavingCallback. Ricevi notifiche e personalizza le esportazioni HTML per una qualità ottimale dei documenti.
type: docs
weight: 5910
url: /it/net/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface

Implementa questa interfaccia se vuoi ricevere notifiche e controllare come Aspose.Words salva i font quando esporta un documento in formato HTML.

```csharp
public interface IFontSavingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [FontSaving](../../aspose.words.saving/ifontsavingcallback/fontsaving/)(*[FontSavingArgs](../fontsavingargs/)*) | Chiamato quando Aspose.Words sta per salvare una risorsa font. |

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
