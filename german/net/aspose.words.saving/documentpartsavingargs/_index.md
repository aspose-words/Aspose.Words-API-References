---
title: DocumentPartSavingArgs Class
linktitle: DocumentPartSavingArgs
articleTitle: DocumentPartSavingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.DocumentPartSavingArgs, die für die Verbesserung der Dokumentverarbeitung mit anpassbaren Speicheroptionen und effizienten Rückrufen unerlässlich ist.
type: docs
weight: 5690
url: /de/net/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class

Liefert Daten für die[`DocumentPartSaving`](../idocumentpartsavingcallback/documentpartsaving/) Rückruf.

Um mehr zu erfahren, besuchen Sie die[Speichern eines Dokuments](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class DocumentPartSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.saving/documentpartsavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das gespeichert wird. |
| [DocumentPartFileName](../../aspose.words.saving/documentpartsavingargs/documentpartfilename/) { get; set; } | Ruft den Dateinamen (ohne Pfad) ab oder legt ihn fest, unter dem der Dokumentteil gespeichert wird. |
| [DocumentPartStream](../../aspose.words.saving/documentpartsavingargs/documentpartstream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem der Dokumentteil gespeichert wird. |
| [KeepDocumentPartStreamOpen](../../aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream nach dem Speichern eines Dokumentteils geöffnet halten oder schließen soll. |

## Bemerkungen

Wenn Aspose.Words ein Dokument in HTML oder verwandten Formaten speichert und[`DocumentSplitCriteria`](../htmlsaveoptions/documentsplitcriteria/)Wenn angegeben ist, wird das Dokument in Teile aufgeteilt und standardmäßig wird jeder Dokumentteil in einer separaten Datei gespeichert.

Klasse`DocumentPartSavingArgs` ermöglicht Ihnen die Steuerung, wie die einzelnen Dokumentteile gespeichert werden. Es ermöglicht Ihnen, die Generierung von Dateinamen neu zu definieren oder das Speichern von Dokumentteilen in -Dateien vollständig zu umgehen, indem Sie Ihre eigenen Stream-Objekte bereitstellen.

Um Dokumentteile in Streams statt in Dateien zu speichern, verwenden Sie die[`DocumentPartStream`](./documentpartstream/) Eigentum.

## Beispiele

Zeigt, wie ein Dokument in Teile aufgeteilt und gespeichert wird.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Erstellen Sie ein "HtmlFixedSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Wenn wir das Dokument normal speichern, gibt es eine Ausgabe-HTML
    // Dokument mit dem gesamten Inhalt des Quelldokuments.
    // Setzen Sie die Eigenschaft "DocumentSplitCriteria" auf "DocumentSplitCriteria.SectionBreak" auf
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
/// Legt benutzerdefinierte Dateinamen für Ausgabedokumente fest, in die beim Speichern ein Dokument aufgeteilt wird.
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
        // Über die Eigenschaft „Dokument“ können wir auf das gesamte Quelldokument zugreifen.
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

        // Unten finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jeden Teil des Dokuments speichern soll.
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

        // Unten finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jeden Teil des Dokuments speichern soll.
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
