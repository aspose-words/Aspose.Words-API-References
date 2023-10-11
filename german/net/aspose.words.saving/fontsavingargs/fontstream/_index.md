---
title: FontSavingArgs.FontStream
second_title: Aspose.Words für .NET-API-Referenz
description: FontSavingArgs eigendom. Ermöglicht die Angabe des Streams in dem die Schriftart gespeichert wird.
type: docs
weight: 50
url: /de/net/aspose.words.saving/fontsavingargs/fontstream/
---
## FontSavingArgs.FontStream property

Ermöglicht die Angabe des Streams, in dem die Schriftart gespeichert wird.

```csharp
public Stream FontStream { get; set; }
```

### Bemerkungen

Mit dieser Eigenschaft können Sie Schriftarten während des HTML-Exports in Streams statt in Dateien speichern.

Der Standardwert ist`Null` . Wenn diese Eigenschaft ist`Null` , wird die Schriftart in einer im angegebenen Datei gespeichert[`FontFileName`](../fontfilename/) Eigentum.

### Beispiele

Zeigt, wie Sie eine benutzerdefinierte Logik für den Export von Schriftarten beim Speichern in HTML definieren.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Konfigurieren Sie ein SaveOptions-Objekt, um Schriftarten in separate Dateien zu exportieren.
    // Legen Sie einen Rückruf fest, der das Speichern von Schriftarten auf benutzerdefinierte Weise übernimmt.
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
/// Druckt Informationen zu exportierten Schriftarten und speichert sie im selben lokalen Systemordner wie ihre Ausgabe-.html.
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

        // 2 – In einem Stream speichern:
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


