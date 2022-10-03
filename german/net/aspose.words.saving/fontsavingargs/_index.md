---
title: FontSavingArgs
second_title: Aspose.Words für .NET-API-Referenz
description: Liefert Daten für dieFontSaving./ifontsavingcallback/fontsaving/ Ereignis.
type: docs
weight: 4770
url: /de/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Liefert Daten für die[`FontSaving`](../ifontsavingcallback/fontsaving/) Ereignis.

```csharp
public class FontSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Gibt an, ob die aktuelle Schriftart fett ist. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das gespeichert wird. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Gibt den Namen der aktuellen Schriftfamilie an. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Ermittelt oder setzt den Dateinamen (ohne Pfad), in dem die Schriftart gespeichert wird. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem die Schriftart gespeichert wird. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Ermöglicht die Angabe, ob die aktuelle Schriftart als Schriftartressource exportiert wird. Standard ist`Stimmt` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Exportieren als Schriftartressource in Untergruppen aufgeteilt wird. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Gibt an, ob die aktuelle Schriftart kursiv ist. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream offen halten oder nach dem Speichern einer Schriftart schließen soll. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Ruft den ursprünglichen Schriftartdateinamen mit einer Erweiterung ab. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Ruft die ursprüngliche Schriftdateigröße ab. |

### Bemerkungen

Wenn Aspose.Words ein Dokument in HTML oder verwandten Formaten speichert und[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) ist eingestellt auf **Stimmt**, speichert es jedes Schriftartthema für den Export in einer separaten Datei.

[`FontSavingArgs`](./fontsavingargs/) steuert, ob bestimmte Font-Ressourcen exportiert werden sollen und wie.

[`FontSavingArgs`](./fontsavingargs/)erlaubt auch, neu zu definieren, wie Schriftdateinamen generiert werden, oder das Speichern von Schriften in Dateien vollständig zu umgehen, indem eigene Stream-Objekte bereitgestellt werden.

Um zu entscheiden, ob eine bestimmte Schriftartressource gespeichert werden soll, verwenden Sie die[`IsExportNeeded`](./isexportneeded/) Eigentum.

Um Schriftarten in Streams statt in Dateien zu speichern, verwenden Sie die[`FontStream`](./fontstream/) Eigentum.

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
