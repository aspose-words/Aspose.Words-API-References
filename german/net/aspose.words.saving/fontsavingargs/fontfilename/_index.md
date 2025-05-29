---
title: FontSavingArgs.FontFileName
linktitle: FontFileName
articleTitle: FontFileName
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontFileName-Eigenschaft von FontSavingArgs, verwalten Sie ganz einfach Schriftdateinamen und verbessern Sie Ihren Design-Workflow mit nahtlosen Speicherfunktionen.
type: docs
weight: 40
url: /de/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Ruft den Dateinamen (ohne Pfad) ab oder legt ihn fest, unter dem die Schriftart gespeichert wird.

```csharp
public string FontFileName { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie neu definieren, wie die Schriftartdateinamen beim Export nach HTML generiert werden .

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den Dateinamen, der von Aspose.Words generiert wurde. Sie können den Wert dieser Eigenschaft ändern, um die Schriftart in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words generiert beim Export ins HTML-Format automatisch einen eindeutigen Dateinamen für jede eingebettete Schriftart. Wie der Schriftartdateiname generiert wird, hängt davon ab, ob Sie das Dokument in einer Datei oder einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der generierte Schriftartdateiname wie folgt aus: &lt;Name der Basisdatei des Dokuments&gt;.&lt;ursprünglicher Dateiname&gt;&lt;optionales Suffix&gt;.&lt;Erweiterung&gt;.

Beim Speichern eines Dokuments in einem Stream sieht der generierte Schriftartdateiname wie folgt aus: Aspose.Words.&lt;Dokument-GUID&gt;.&lt;ursprünglicher Dateiname&gt;&lt;optionales Suffix&gt;.&lt;Erweiterung&gt;.

`FontFileName` darf nur den Dateinamen ohne Pfad enthalten. Aspose.Words ermittelt den Pfad zum Speichern anhand des Dokumentdateinamens, der[`FontsFolder`](../../htmlsaveoptions/fontsfolder/) und [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) Eigenschaften.

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
