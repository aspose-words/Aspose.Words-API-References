---
title: FontSavingArgs.IsSubsettingNeeded
linktitle: IsSubsettingNeeded
articleTitle: IsSubsettingNeeded
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FontSavingArgs IsSubsettingNeeded“ zur Steuerung der Schrift-Subsettings für optimierte Schriftressourcenexporte. Verbessern Sie noch heute Ihren Design-Workflow!
type: docs
weight: 70
url: /de/net/aspose.words.saving/fontsavingargs/issubsettingneeded/
---
## FontSavingArgs.IsSubsettingNeeded property

Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Exportieren als Schriftartressource in eine Teilmenge unterteilt wird.

```csharp
public bool IsSubsettingNeeded { get; set; }
```

## Bemerkungen

Schriftarten können als vollständige Originaldateien exportiert oder in Teilmengen aufgeteilt werden, sodass nur die im Dokument verwendeten Zeichen enthalten sind. Durch die Teilmengenauswertung kann die Größe der resultierenden Schriftartressourcen reduziert werden.

Standardmäßig entscheidet Aspose.Words, ob eine Teilmenge erstellt werden soll oder nicht, indem die ursprüngliche Schriftdateigröße mit der in[`FontResourcesSubsettingSizeThreshold`](../../htmlsaveoptions/fontresourcessubsettingsizethreshold/) . Sie können dieses Verhalten für einzelne Schriftarten überschreiben, indem Sie die`IsSubsettingNeeded` Eigentum.

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

* class [FontSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
