---
title: Class ImageSavingArgs
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.ImageSavingArgs klas. Stellt Daten für die bereitImageSaving event.
type: docs
weight: 5240
url: /de/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Stellt Daten für die bereit[`ImageSaving`](../iimagesavingcallback/imagesaving/) event.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class ImageSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Ruft die ab[`ShapeBase`](../../aspose.words.drawing/shapebase/) Objekt, das der Form oder Gruppenform entspricht, die gespeichert werden soll. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das gerade gespeichert wird. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Ruft den Dateinamen (ohne Pfad) ab, unter dem das Bild gespeichert wird, oder legt diesen fest. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem das Bild gespeichert wird. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Gibt zurück`WAHR` ob das aktuelle Bild für den Export verfügbar ist. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream offen halten oder schließen soll, nachdem ein Bild gespeichert wurde. |

### Bemerkungen

Wenn Aspose.Words ein Dokument im HTML-Format speichert, speichert es standardmäßig jedes Bild in einer separaten Datei . Aspose.Words verwendet den Dateinamen des Dokuments und eine eindeutige Nummer, um für jedes im Dokument gefundene Bild einen eindeutigen Dateinamen zu generieren.

`ImageSavingArgs`Ermöglicht die Neudefinition der Generierung von Bilddateinamen oder die vollständige Umgehung des Speicherns von Bildern in Dateien durch die Bereitstellung eigener Stream-Objekte.

Um Ihre eigene Logik zum Generieren von Bilddateinamen anzuwenden, verwenden Sie [`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) Und[`IsImageAvailable`](./isimageavailable/) Eigenschaften.

Um Bilder in Streams statt in Dateien zu speichern, verwenden Sie die[`ImageStream`](./imagestream/) Eigentum.

### Beispiele

Zeigt, wie man ein Dokument in Teile aufteilt und diese speichert.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Erstellen Sie ein „HtmlFixedSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Wenn wir das Dokument normal speichern, gibt es ein Ausgabe-HTML
    // Dokument mit dem gesamten Inhalt des Quelldokuments.
    // Setzen Sie die Eigenschaft „DocumentSplitCriteria“ auf „DocumentSplitCriteria.SectionBreak“.
    // unser Dokument in mehreren HTML-Dateien speichern: eine für jeden Abschnitt.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Weisen Sie der Eigenschaft „DocumentPartSavingCallback“ einen benutzerdefinierten Rückruf zu, um die Logik zum Speichern von Dokumentteilen zu ändern.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Wenn wir ein Dokument, das Bilder enthält, in HTML konvertieren, erhalten wir am Ende eine HTML-Datei, die auf mehrere Bilder verweist.
    // Jedes Bild liegt in Form einer Datei im lokalen Dateisystem vor.
    // Es gibt auch einen Rückruf, mit dem der Name und der Dateisystemspeicherort jedes Bildes angepasst werden können.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Legt benutzerdefinierte Dateinamen für Ausgabedokumente fest, in die der Speichervorgang ein Dokument aufteilt.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Über die Eigenschaft „Document“ können wir auf das gesamte Quelldokument zugreifen.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Nachfolgend finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jeden Teil des Dokuments speichert.
        // 1 – Legen Sie einen Dateinamen für die Ausgabeteildatei fest:
        args.DocumentPartFileName = partFileName;

        // 2 – Erstellen Sie einen benutzerdefinierten Stream für die Ausgabeteildatei:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Legt benutzerdefinierte Dateinamen für Bilddateien fest, die bei einer HTML-Konvertierung erstellt werden.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Nachfolgend finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jeden Teil des Dokuments speichert.
        // 1 – Legen Sie einen Dateinamen für die Ausgabebilddatei fest:
        args.ImageFileName = imageFileName;

        // 2 – Erstellen Sie einen benutzerdefinierten Stream für die Ausgabebilddatei:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


