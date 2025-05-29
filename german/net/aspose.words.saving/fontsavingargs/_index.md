---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.FontSavingArgs – verbessern Sie die Dokumentverarbeitung mit detaillierten FontSaving-Ereignisdaten für überlegene Anpassung und Kontrolle.
type: docs
weight: 5780
url: /de/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Liefert Daten für die[`FontSaving`](../ifontsavingcallback/fontsaving/) Ereignis.

Um mehr zu erfahren, besuchen Sie die[Speichern eines Dokuments](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class FontSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Gibt an, ob die aktuelle Schriftart fett ist. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das gespeichert wird. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Gibt den aktuellen Schriftfamiliennamen an. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Ruft den Dateinamen (ohne Pfad) ab oder legt ihn fest, unter dem die Schriftart gespeichert wird. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem die Schriftart gespeichert wird. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Ermöglicht die Angabe, ob die aktuelle Schriftart als Schriftartressource exportiert wird. Standardmäßig ist`WAHR` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Exportieren als Schriftartressource in eine Teilmenge unterteilt wird. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Gibt an, ob die aktuelle Schriftart kursiv ist. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Schriftart geöffnet lassen oder schließen soll. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Ruft den ursprünglichen Schriftartdateinamen mit einer Erweiterung ab. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Ruft die ursprüngliche Schriftdateigröße ab. |

## Bemerkungen

Wenn Aspose.Words ein Dokument in HTML oder verwandten Formaten speichert und[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) ist eingestellt auf`WAHR`, speichert es jedes Schriftartmotiv für den Export in einer separaten Datei.

`FontSavingArgs` steuert, ob und wie bestimmte Schriftartressourcen exportiert werden sollen.

`FontSavingArgs`ermöglicht außerdem die Neudefinition der Generierung von Schriftartdateinamen oder das vollständige Umgehen des Speicherns von Schriftarten in Dateien durch die Bereitstellung eigener Streamobjekte.

Um zu entscheiden, ob eine bestimmte Schriftartressource gespeichert werden soll, verwenden Sie die[`IsExportNeeded`](./isexportneeded/) Eigentum.

Um Schriftarten in Streams statt in Dateien zu speichern, verwenden Sie die[`FontStream`](./fontstream/) Eigentum.

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
