---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà PixelFormat di ImageSaveOptions per personalizzare facilmente il formato pixel delle immagini generate, ottenendo qualità e prestazioni ottimali.
type: docs
weight: 120
url: /it/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Ottiene o imposta il formato pixel per le immagini generate.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Osservazioni

Questa proprietà ha effetto solo quando si salva in formati di immagini raster.

Il valore predefinito èFormat32BppArgb.

Il formato pixel dell'immagine di output potrebbe differire dal valore impostato a causa del lavoro di GDI+.

## Esempi

Mostra come selezionare una velocità bit per pixel con cui trasformare un documento in un'immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// seleziona un formato pixel per l'immagine che verrà generata dall'operazione di salvataggio.
// Diverse velocità di bit per pixel influiranno sulla qualità e sulle dimensioni del file dell'immagine generata.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Possiamo clonare le istanze di ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Guarda anche

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
