---
title: DocumentPartSavingArgs.DocumentPartStream
linktitle: DocumentPartStream
articleTitle: DocumentPartStream
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der DocumentPartStream-Eigenschaft in DocumentPartSavingArgs ganz einfach angeben können, wo Ihre Dokumentteile gespeichert werden sollen, um eine nahtlose Verwaltung zu gewährleisten.
type: docs
weight: 30
url: /de/net/aspose.words.saving/documentpartsavingargs/documentpartstream/
---
## DocumentPartSavingArgs.DocumentPartStream property

Ermöglicht die Angabe des Streams, in dem der Dokumentteil gespeichert wird.

```csharp
public Stream DocumentPartStream { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie beim HTML-Export Dokumentteile in Streams statt in Dateien speichern.

Der Standardwert ist`null` Wenn diese Eigenschaft`null` wird der Dokumentteil in einer Datei gespeichert, die in der[`DocumentPartFileName`](../documentpartfilename/) Eigentum.

Beim Speichern in einen Stream im HTML-Format wird angefordert von[`Save`](../../../aspose.words/document/save/) oder[`Save`](../../../aspose.words/document/save/) und der erste Dokumentteil soll gespeichert werden. Aspose.Words schlägt hier den Hauptausgabestream vor, der ursprünglich vom Anrufer übergeben wurde.

Beim Speichern im EPUB-Format, einem auf HTML basierenden Containerformat,`DocumentPartStream` kann nicht angegeben werden, da alle untergeordneten Teile in einem einzigen Ausgabepaket gekapselt werden.

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

* class [DocumentPartSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
