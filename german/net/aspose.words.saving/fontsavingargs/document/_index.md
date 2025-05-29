---
title: FontSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontSavingArgs-Eigenschaft, um während Speichervorgängen auf das Dokumentobjekt zuzugreifen und so die Effizienz Ihrer Dokumentverwaltung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.saving/fontsavingargs/document/
---
## FontSavingArgs.Document property

Ruft das Dokumentobjekt ab, das gespeichert wird.

```csharp
public Document Document { get; }
```

## Beispiele

Zeigt, wie Sie beim Speichern im HTML-Format eine benutzerdefinierte Logik zum Exportieren von Schriftarten definieren.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Konfigurieren Sie ein SaveOptions-Objekt, um Schriftarten in separate Dateien zu exportieren.
    // Legen Sie einen Rückruf fest, der das Speichern von Schriftarten auf benutzerdefinierte Weise handhabt.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Der Rückruf exportiert .ttf-Dateien und speichert sie zusammen mit dem Ausgabedokument.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Druckt Informationen zu exportierten Schriftarten und speichert sie im selben lokalen Systemordner wie ihre Ausgabe-HTML.
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

        // Es gibt zwei Möglichkeiten, eine exportierte Schriftart zu speichern.
        // 1 – Speichern Sie es an einem lokalen Dateisystemspeicherort:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - In einem Stream speichern:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [FontSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
