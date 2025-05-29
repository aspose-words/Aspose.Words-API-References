---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words per .NET
description: Scopri la proprietà ExportFontResources di HtmlSaveOptions per controllare l'esportazione delle risorse font per HTML, MHTML o EPUB. Massimizza l'aspetto visivo del tuo documento!
type: docs
weight: 140
url: /it/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Specifica se le risorse dei font devono essere esportate in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportFontResources { get; set; }
```

## Osservazioni

L'esportazione delle risorse dei font consente un rendering coerente dei documenti indipendentemente dai font disponibili nell'ambiente di un determinato utente.

Se`ExportFontResources` è impostato su`VERO` , il documento HTML principale farà riferimento a ogni font tramite il CSS 3**@font-face** at-rule e i font verranno generati come file separati. Quando si esporta nei formati IDPF EPUB o MHTML , i font verranno incorporati nel pacchetto corrispondente insieme ad altri file ausiliari.

Se[`ExportFontsAsBase64`](../exportfontsasbase64/) è impostato su`VERO` , i font non verranno salvati in file separati. Invece, verranno incorporati in**@font-face** regole at nella codifica Base64.

**Importante!**Quando si esportano risorse font, è necessario considerare le questioni relative alla licenza dei font. Gli autori che desiderano utilizzare font specifici tramite un meccanismo di download devono sempre verificare attentamente che l'uso previsto rientri nell'ambito della licenza. Molti font commerciali attualmente non consentono il download dal web dei loro font in alcun formato. I contratti di licenza che coprono alcuni font specificano specificamente che l'utilizzo tramite**@font-face** rules nei fogli di stile CSS non è consentito. Anche la creazione di sottoinsiemi di font può violare i termini di licenza.

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

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
