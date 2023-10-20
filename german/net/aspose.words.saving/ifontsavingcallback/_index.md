---
title: IFontSavingCallback Interface
linktitle: IFontSavingCallback
articleTitle: IFontSavingCallback
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.IFontSavingCallback koppel. Implementieren Sie diese Schnittstelle wenn Sie Benachrichtigungen erhalten und steuern möchten wie Aspose.Words Schriftarten speichert wenn ein Dokument in das HTMLFormat exportiert wird in C#.
type: docs
weight: 5160
url: /de/net/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten und steuern möchten, wie Aspose.Words Schriftarten speichert, wenn ein Dokument in das HTML-Format exportiert wird.

```csharp
public interface IFontSavingCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [FontSaving](../../aspose.words.saving/ifontsavingcallback/fontsaving/)(*[FontSavingArgs](../fontsavingargs/)*) | Wird aufgerufen, wenn Aspose.Words im Begriff ist, eine Schriftartressource zu speichern. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
