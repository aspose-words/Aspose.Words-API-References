---
title: FontSavingArgs.OriginalFileName
second_title: Aspose.Words für .NET-API-Referenz
description: FontSavingArgs eigendom. Ruft den ursprünglichen Schriftartdateinamen mit einer Erweiterung ab.
type: docs
weight: 100
url: /de/net/aspose.words.saving/fontsavingargs/originalfilename/
---
## FontSavingArgs.OriginalFileName property

Ruft den ursprünglichen Schriftartdateinamen mit einer Erweiterung ab.

```csharp
public string OriginalFileName { get; }
```

### Bemerkungen

Diese Eigenschaft enthält den ursprünglichen Dateinamen der aktuellen Schriftart, sofern bekannt. Andernfalls kann es sich um eine leere Zeichenfolge handeln.

### Beispiele

Zeigt, wie benutzerdefinierte Logik zum Exportieren von Schriftarten beim Speichern in HTML definiert wird.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Konfigurieren Sie ein SaveOptions-Objekt, um Schriftarten in separate Dateien zu exportieren.
    // Festlegen eines Rückrufs, der das Speichern von Schriftarten auf benutzerdefinierte Weise handhabt.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Der Callback exportiert .ttf-Dateien und speichert sie zusammen mit dem Ausgabedokument.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

/// <summary>
/// Druckt Informationen über exportierte Schriftarten und speichert sie im selben lokalen Systemordner wie ihre Ausgabe-.html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Von hier aus können wir auch auf das Quelldokument zugreifen.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Es gibt zwei Möglichkeiten, einen exportierten Font zu speichern.
        // 1 - Speichern Sie es an einem lokalen Speicherort im Dateisystem:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Speichern Sie es in einem Stream:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Siehe auch

* class [FontSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../fontsavingargs/)
* Montage [Aspose.Words](../../../)


