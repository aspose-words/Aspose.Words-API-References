---
title: ImageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSet-Eigenschaft von ImageSaveOptions, um die Darstellung Ihres Dokuments anzupassen. Steuern Sie, welche Seiten für eine optimierte Ausgabe gespeichert werden sollen. Jetzt entdecken!
type: docs
weight: 100
url: /de/net/aspose.words.saving/imagesaveoptions/pageset/
---
## ImageSaveOptions.PageSet property

Ruft die zu rendernden Seiten ab oder legt sie fest. Standardmäßig sind alle Seiten im Dokument dargestellt.

```csharp
public PageSet PageSet { get; set; }
```

## Bemerkungen

Diese Eigenschaft wirkt sich nur beim Rendern von Dokumentseiten aus. Beim Rendern von Formen in Bilder wird diese Eigenschaft ignoriert.

## Beispiele

Zeigt, wie Seiten basierend auf genauen Seitenbereichen extrahiert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

Zeigt, wie Sie angeben, welche Seite in einem Dokument als Bild gerendert werden soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world! This is page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 3.");

Assert.AreEqual(3, doc.PageCount);

// Wenn wir das Dokument als Bild speichern, rendert Aspose.Words standardmäßig nur die erste Seite.
// Wir können ein SaveOptions-Objekt übergeben, um eine andere zu rendernde Seite anzugeben.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Gif);
// Jede Seite des Dokuments in eine separate Bilddatei rendern.
for (int i = 1; i <= doc.PageCount; i++)
{
    saveOptions.PageSet = new PageSet(1);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageIndex.Page {i}.gif", saveOptions);
}
```

Zeigt, wie jede Seite eines Dokuments in ein separates TIFF-Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild umwandelt.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Setze die Eigenschaft "PageSet" auf die Nummer der ersten Seite von
    // von wo aus mit dem Rendern des Dokuments begonnen werden soll.
    options.PageSet = new PageSet(i);
    // Seite mit 2325 x 5325 Pixeln und 600 dpi exportieren.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Zeigt, wie eine Seite aus einem Dokument in ein JPEG-Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild umwandelt.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Setze das "PageSet" auf "1", um die zweite Seite auszuwählen über
// der nullbasierte Index, ab dem mit der Darstellung des Dokuments begonnen werden soll.
options.PageSet = new PageSet(1);

// Wenn wir das Dokument im JPEG-Format speichern, rendert Aspose.Words nur eine Seite.
// Dieses Bild enthält eine Seite ab Seite zwei,
// Dies ist lediglich die zweite Seite des Originaldokuments.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Siehe auch

* class [PageSet](../../pageset/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
