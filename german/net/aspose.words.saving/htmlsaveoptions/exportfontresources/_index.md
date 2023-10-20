---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ExportFontResources eigendom. Gibt an ob Schriftartressourcen nach HTML MHTML oder EPUB exportiert werden sollen. Die Standardeinstellung istFALSCH  in C#.
type: docs
weight: 140
url: /de/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Gibt an, ob Schriftartressourcen nach HTML, MHTML oder EPUB exportiert werden sollen. Die Standardeinstellung ist`FALSCH` .

```csharp
public bool ExportFontResources { get; set; }
```

## Bemerkungen

Das Exportieren von Schriftartressourcen ermöglicht eine konsistente Dokumentwiedergabe unabhängig von den verfügbaren Schriftarten in der Umgebung eines bestimmten Benutzers.

Wenn`ExportFontResources` ist eingestellt auf`WAHR` Das Haupt-HTML-Dokument verweist über CSS 3 auf jede Schriftart**@Schriftart** at-rule und Schriftarten werden als separate Dateien ausgegeben. Beim Exportieren in die Formate IDPF EPUB oder MHTML werden Schriftarten zusammen mit anderen Tochterdateien in das entsprechende Paket eingebettet.

Wenn[`ExportFontsAsBase64`](../exportfontsasbase64/) ist eingestellt auf`WAHR` Schriftarten werden nicht in separaten Dateien gespeichert. Stattdessen werden sie eingebettet**@Schriftart** at-Regeln in Base64-Kodierung.

**Wichtig!** Beim Exportieren von Schriftartressourcen sollten Aspekte der Schriftartlizenzierung berücksichtigt werden. Autoren, die bestimmte Schriftarten über einen herunterladbaren -Schriftartenmechanismus verwenden möchten, müssen stets sorgfältig prüfen, ob ihre beabsichtigte Verwendung im Rahmen der Schriftartenlizenz liegt. Bei vielen kommerziellen Schriftarten ist das Herunterladen ihrer Schriftarten aus dem Internet in irgendeiner Form derzeit nicht möglich. In Lizenzvereinbarungen, die einige Schriftarten abdecken, wird ausdrücklich darauf hingewiesen, dass die Verwendung durch erfolgt**@Schriftart** Rules in CSS-Stylesheets ist nicht zulässig. Unterteilung von Schriftarten kann ebenfalls gegen Lizenzbedingungen verstoßen.

## Beispiele

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

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
