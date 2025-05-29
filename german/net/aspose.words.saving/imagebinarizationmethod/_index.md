---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.ImageBinarizationMethod für eine effektive Bildbinarisierung. Optimieren Sie Ihre Dokumentverarbeitung mit fortschrittlichen Techniken.
type: docs
weight: 5950
url: /de/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Gibt die Methode an, mit der das Bild binärisiert wird.

```csharp
public enum ImageBinarizationMethod
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Threshold | `0` | Gibt die Schwellenwertmethode an. |
| FloydSteinbergDithering | `1` | Gibt Dithering mit der Floyd-Steinberg-Fehlerdiffusionsmethode an. |

## Beispiele

Zeigt, wie der Schwellenwert für den TIFF-Binarisierungsfehler festgelegt wird, wenn die Floyd-Steinberg-Methode zum Rendern eines TIFF-Bilds verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als TIFF speichern, können wir ein SaveOptions-Objekt übergeben an
// Passen Sie das Dithering an, das Aspose.Words beim Rendern dieses Bildes anwendet.
// Der Standardwert der Eigenschaft „ThresholdForFloydSteinbergDithering“ ist 128.
// Höhere Werte führen tendenziell zu dunkleren Bildern.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
