---
title: Class FontSavingArgs
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.FontSavingArgs klas. Stellt Daten für die bereitFontSaving event.
type: docs
weight: 5030
url: /de/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Stellt Daten für die bereit[`FontSaving`](../ifontsavingcallback/fontsaving/) event.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class FontSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Gibt an, ob die aktuelle Schriftart fett ist. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das gespeichert wird. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Gibt den aktuellen Namen der Schriftfamilie an. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Ruft den Dateinamen (ohne Pfad) ab, unter dem die Schriftart gespeichert wird, oder legt diesen fest. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem die Schriftart gespeichert wird. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Ermöglicht die Angabe, ob die aktuelle Schriftart als Schriftartressource exportiert wird. Standard ist`WAHR` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftartressource in Teilmengen unterteilt wird. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Gibt an, ob die aktuelle Schriftart kursiv ist. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream offen halten oder schließen soll, nachdem eine Schriftart gespeichert wurde. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Ruft den ursprünglichen Namen der Schriftartdatei mit einer Erweiterung ab. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Ruft die ursprüngliche Schriftdateigröße ab. |

### Bemerkungen

Wenn Aspose.Words ein Dokument in HTML oder verwandten Formaten speichert und[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) ist eingestellt auf`WAHR`, speichert es jedes Schriftartthema für den Export in einer separaten Datei.

`FontSavingArgs` Steuert, ob und wie eine bestimmte Schriftartressource exportiert werden soll.

`FontSavingArgs`Ermöglicht auch die Neudefinition der Generierung von Schriftartdateinamen oder die vollständige Umgehung des Speicherns von Schriftarten in Dateien durch die Bereitstellung eigener Stream-Objekte.

Um zu entscheiden, ob eine bestimmte Schriftartressource gespeichert werden soll, verwenden Sie die[`IsExportNeeded`](./isexportneeded/) Eigentum.

Um Schriftarten in Streams statt in Dateien zu speichern, verwenden Sie die[`FontStream`](./fontstream/) Eigentum.

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


