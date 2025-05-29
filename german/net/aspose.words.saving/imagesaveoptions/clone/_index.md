---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageSaveOptions-Klonmethode, um mühelos einen tiefen Klon Ihrer Objekte zu erstellen und so Ihre Codierungseffizienz und Flexibilität zu verbessern.
type: docs
weight: 210
url: /de/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Erstellt einen tiefen Klon dieses Objekts.

```csharp
public ImageSaveOptions Clone()
```

## Beispiele

Zeigt, wie Sie eine Bit-pro-Pixel-Rate auswählen, mit der ein Dokument in ein Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Wählen Sie ein Pixelformat für das Bild aus, das beim Speichern generiert wird.
// Verschiedene Bit-pro-Pixel-Raten wirken sich auf die Qualität und Dateigröße des generierten Bildes aus.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Wir können ImageSaveOptions-Instanzen klonen.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
