---
title: Enum ImageBinarizationMethod
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.ImageBinarizationMethod opsomming. Gibt die Methode an die zum Binarisieren des Bildes verwendet wird.
type: docs
weight: 5200
url: /de/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Gibt die Methode an, die zum Binarisieren des Bildes verwendet wird.

```csharp
public enum ImageBinarizationMethod
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Threshold | `0` | Gibt die Schwellenwertmethode an. |
| FloydSteinbergDithering | `1` | Gibt Dithering mit der Floyd-Steinberg-Fehlerdiffusionsmethode an. |

### Beispiele

Zeigt, wie der TIFF-Binarisierungsfehlerschwellenwert festgelegt wird, wenn die Floyd-Steinberg-Methode zum Rendern eines TIFF-Bilds verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als TIFF speichern, können wir ein SaveOptions-Objekt an übergeben
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


