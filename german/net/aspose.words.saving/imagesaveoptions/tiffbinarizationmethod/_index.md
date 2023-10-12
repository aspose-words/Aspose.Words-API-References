---
title: ImageSaveOptions.TiffBinarizationMethod
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions eigendom. Ruft die beim Konvertieren von Bildern in das 1bppFormat verwendete Methode ab oder legt diese fest. wannSaveFormat IstTiff and TiffCompression ist gleichCcitt3 oderCcitt4 .
type: docs
weight: 170
url: /de/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Ruft die beim Konvertieren von Bildern in das 1-bpp-Format verwendete Methode ab oder legt diese fest. wann[`SaveFormat`](../saveformat/) IstTiff and [`TiffCompression`](../tiffcompression/) ist gleichCcitt3 oderCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

### Bemerkungen

Der Standardwert istThreshold.

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

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


