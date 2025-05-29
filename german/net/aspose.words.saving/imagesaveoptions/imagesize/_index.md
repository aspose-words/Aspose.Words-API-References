---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageSize-Eigenschaft von ImageSaveOptions, um die Bildabmessungen in Pixeln einfach zu verwalten und anzupassen und so optimale Ergebnisse zu erzielen.
type: docs
weight: 70
url: /de/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Ruft die Größe eines generierten Bildes in Pixeln ab oder legt sie fest.

```csharp
public Size ImageSize { get; set; }
```

## Bemerkungen

Diese Eigenschaft wirkt sich nur beim Speichern in Rasterbildformaten aus.

Der Standardwert ist (0 x 0), was bedeutet, dass die Größe des generierten Bildes entsprechend der Größe des Bildes in Punkten, der angegebenen Auflösung und Skalierung berechnet wird .

## Beispiele

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

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
