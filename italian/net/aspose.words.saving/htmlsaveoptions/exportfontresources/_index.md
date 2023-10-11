---
title: HtmlSaveOptions.ExportFontResources
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica se le risorse dei caratteri devono essere esportate in HTML MHTML o EPUB. Limpostazione predefinita èfalso .
type: docs
weight: 140
url: /it/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Specifica se le risorse dei caratteri devono essere esportate in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` .

```csharp
public bool ExportFontResources { get; set; }
```

### Osservazioni

L'esportazione delle risorse dei caratteri consente un rendering coerente del documento indipendentemente dai caratteri disponibili nell'ambiente di un determinato utente.

Se`ExportFontResources` è impostato per`VERO` , il documento HTML principale farà riferimento a ogni carattere tramite CSS 3 **@font-face** at-rule e i caratteri verranno restituiti come file separati. Quando si esporta nei formati IDPF EPUB o MHTML , i caratteri verranno incorporati nel pacchetto corrispondente insieme ad altri file sussidiari.

Se[`ExportFontsAsBase64`](../exportfontsasbase64/) è impostato per`VERO` i caratteri non verranno salvati in file separati. Verranno invece incorporati in **@font-face** regole at nella codifica Base64.

**Importante!** Quando si esportano risorse di caratteri, è necessario considerare i problemi di licenza dei caratteri. Gli autori che desiderano utilizzare caratteri specifici tramite un meccanismo di carattere downloadable devono sempre verificare attentamente che l'uso previsto rientri nell'ambito della licenza del carattere. Molti caratteri commerciali attualmente non consentono il download dal Web dei propri caratteri in qualsiasi forma. I contratti di licenza che coprono alcuni caratteri specificano specificamente che l'utilizzo tramite **@font-face** regole nei fogli di stile CSS non è consentito. Anche il sottoinsieme dei caratteri può violare i termini della licenza.

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

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


