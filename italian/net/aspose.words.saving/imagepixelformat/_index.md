---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.ImagePixelFormat per formati pixel ottimali nelle immagini delle pagine dei documenti. Migliora l'aspetto visivo dei tuoi documenti senza sforzo!
type: docs
weight: 5970
url: /it/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Specifica il formato pixel per le immagini generate delle pagine del documento.

```csharp
public enum ImagePixelFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 bit per pixel, RGB. |
| Format16BppRgb565 | `1` | 16 bit per pixel, RGB. |
| Format16BppArgb1555 | `2` | 16 bit per pixel, ARGB. |
| Format24BppRgb | `3` | 24 bit per pixel, RGB. |
| Format32BppRgb | `4` | 32 bit per pixel, RGB. |
| Format32BppArgb | `5` | 32 bit per pixel, ARGB. |
| Format32BppPArgb | `6` | 32 bit per pixel, ARGB, alfa premoltiplicato. |
| Format48BppRgb | `7` | 48 bit per pixel, RGB. |
| Format64BppArgb | `8` | 64 bit per pixel, ARGB. |
| Format64BppPArgb | `9` | 64 bit per pixel, ARGB, alfa premoltiplicato. |
| Format1bppIndexed | `10` | 1 bit per pixel, indicizzato. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
