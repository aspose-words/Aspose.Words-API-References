---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die PaperColor-Eigenschaft von ImageSaveOptions, um die Hintergrundfarben Ihrer generierten Bilder einfach anzupassen und so die visuelle Attraktivität und Einzigartigkeit zu verbessern.
type: docs
weight: 110
url: /de/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Ruft die Hintergrundfarbe (Papierfarbe) für die generierten Bilder ab oder legt sie fest.

Der Standardwert istWhite.

```csharp
public Color PaperColor { get; set; }
```

## Bemerkungen

Beim Rendern von Seiten eines Dokuments, das seine eigene Hintergrundfarbe angibt, , überschreibt die Hintergrundfarbe des Dokuments die durch diese Eigenschaft angegebene Farbe.

## Beispiele

Rendert eine Seite eines Word-Dokuments in ein Bild mit transparentem oder farbigem Hintergrund.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild umwandelt.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// Setzen Sie die Eigenschaft „PaperColor“ auf eine transparente Farbe, um eine transparente
// Hintergrund des Dokuments, während es in ein Bild gerendert wird.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Setzen Sie die Eigenschaft „PaperColor“ auf eine undurchsichtige Farbe, um diese Farbe anzuwenden
// als Hintergrund des Dokuments, wenn wir es in ein Bild rendern.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
