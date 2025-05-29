---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Bilder mit ImageSaveOptions! Steuern Sie die horizontale und vertikale Auflösung in DPI für beeindruckende Qualität und Klarheit. Verbessern Sie Ihre Bilder noch heute!
type: docs
weight: 130
url: /de/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Legt sowohl die horizontale als auch die vertikale Auflösung für die generierten Bilder in Punkten pro Zoll fest.

```csharp
public float Resolution { set; }
```

## Bemerkungen

Diese Eigenschaft wirkt sich nur beim Speichern in Rasterbildformaten aus.

## Beispiele

Zeigt, wie Sie beim Rendern eines Dokuments in PNG eine Auflösung angeben.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild umwandelt.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Setzen Sie die Eigenschaft „Auflösung“ auf „72“, um das Dokument in 72 dpi zu rendern.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Setzen Sie die Eigenschaft „Auflösung“ auf „300“, um das Dokument in 300 dpi zu rendern.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
