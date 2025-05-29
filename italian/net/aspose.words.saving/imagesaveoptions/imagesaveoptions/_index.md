---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore ImageSaveOptions per salvare le immagini in formati versatili come TIFF, PNG, BMP, JPEG, EMF, EPS, WebP e SVG. Ottimizza la gestione delle tue immagini!
type: docs
weight: 10
url: /it/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare le immagini renderizzate in Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps , WebP OSvg formato.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | SaveFormat | Può essere Tiff ,Png ,Bmp , Jpeg ,Emf ,EpsWebP OSvg formato. |

## Esempi

Mostra come configurare la compressione durante il salvataggio di un documento in formato JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Creiamo un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo trasforma il documento in un'immagine.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Impostare la proprietà "JpegQuality" su "10" per utilizzare una compressione più forte durante il rendering del documento.
// Ciò ridurrà le dimensioni del file del documento, ma l'immagine presenterà artefatti di compressione più evidenti.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Impostare la proprietà "JpegQuality" su "100" per utilizzare una compressione più debole durante il rendering del documento.
// Ciò migliorerà la qualità dell'immagine a scapito delle dimensioni del file.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
