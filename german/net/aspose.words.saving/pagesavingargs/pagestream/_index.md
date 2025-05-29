---
title: PageSavingArgs.PageStream
linktitle: PageStream
articleTitle: PageStream
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageStream-Eigenschaft von PageSavingArgs, die das nahtlose Speichern von Dokumentseiten in Ihrem gewünschten Stream für eine effiziente Dateiverwaltung ermöglicht.
type: docs
weight: 50
url: /de/net/aspose.words.saving/pagesavingargs/pagestream/
---
## PageSavingArgs.PageStream property

Ermöglicht die Angabe des Streams, in dem die Dokumentseite gespeichert wird.

```csharp
public Stream PageStream { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie Dokumentseiten in Streams statt in Dateien speichern.

Der Standardwert ist`null` Wenn diese Eigenschaft`null` wird die Dokumentseite in einer Datei gespeichert, die im[`PageFileName`](../pagefilename/) Eigentum.

Wenn beide`PageStream` Und[`PageFileName`](../pagefilename/) gesetzt sind, wird PageStream verwendet.

## Beispiele

Zeigt, wie Sie mithilfe eines Rückrufs ein Dokument seitenweise im HTML-Format speichern.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Erstellen Sie ein "HtmlFixedSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Wir speichern jede Seite dieses Dokuments in einer separaten HTML-Datei im lokalen Dateisystem.
    // Legen Sie einen Rückruf fest, der es uns ermöglicht, jedes ausgegebene HTML-Dokument zu benennen.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Speichert alle Seiten in einer darin angegebenen Datei und einem angegebenen Verzeichnis.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Unten finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jede Seite des Dokuments speichert.
        // 1 – Legen Sie einen Dateinamen für die Ausgabeseitendatei fest:
        args.PageFileName = outFileName;

        // 2 – Erstellen Sie einen benutzerdefinierten Stream für die Ausgabeseitendatei:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Siehe auch

* class [PageSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
