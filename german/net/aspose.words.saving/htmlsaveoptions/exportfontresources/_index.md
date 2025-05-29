---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlSaveOptions ExportFontResources-Eigenschaft, um den Export von Schriftressourcen für HTML, MHTML oder EPUB zu steuern. Maximieren Sie die visuelle Attraktivität Ihres Dokuments!
type: docs
weight: 140
url: /de/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Gibt an, ob Schriftressourcen in HTML, MHTML oder EPUB exportiert werden sollen. Standard ist`FALSCH` .

```csharp
public bool ExportFontResources { get; set; }
```

## Bemerkungen

Durch das Exportieren von Schriftartressourcen ist eine konsistente Dokumentwiedergabe unabhängig von den in der Umgebung eines bestimmten Benutzers verfügbaren Schriftarten möglich.

Wenn`ExportFontResources` ist eingestellt auf`WAHR` , Haupt-HTML-Dokument wird auf jede Schriftart über die CSS 3 verweisen**@Schriftart** at-rule und Schriftarten werden als separate Dateien ausgegeben. Beim Export in die Formate IDPF EPUB oder MHTML werden Schriftarten zusammen mit anderen Zusatzdateien in das entsprechende Paket eingebettet.

Wenn[`ExportFontsAsBase64`](../exportfontsasbase64/) ist eingestellt auf`WAHR` , werden Schriftarten nicht in separaten Dateien gespeichert. Stattdessen werden sie eingebettet in**@Schriftart** at-Regeln in Base64-Kodierung.

**Wichtig!**Beim Exportieren von Schriftressourcen sollten Sie die Lizenzierung von Schriften berücksichtigen. Autoren, die bestimmte Schriften über einen Download-Mechanismus verwenden möchten, müssen stets sorgfältig prüfen, ob die beabsichtigte Verwendung im Rahmen der Lizenz liegt. Viele kommerzielle Schriften erlauben derzeit keinen Download über das Internet. Lizenzvereinbarungen für bestimmte Schriften weisen ausdrücklich darauf hin, dass die Verwendung über**@Schriftart** Regeln in CSS-Stylesheets sind nicht zulässig. Font-Subsetting kann auch gegen Lizenzbedingungen verstoßen.

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

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
