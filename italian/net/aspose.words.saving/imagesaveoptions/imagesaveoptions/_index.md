---
title: ImageSaveOptions.ImageSaveOptions
second_title: Aspose.Words per .NET API Reference
description: ImageSaveOptions costruttore. Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare le immagini renderizzate in Tiff Png Bmp  Emf Jpeg oSvg formato. Png Bmp Jpeg oSvg formato.
type: docs
weight: 10
url: /it/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare le immagini renderizzate in Tiff ,Png ,Bmp , Emf ,Jpeg oSvg formato. Png ,Bmp ,Jpeg oSvg formato.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | SaveFormat | Può essere Tiff ,Png ,Bmp , Emf ,Jpeg oSvg . Png ,Bmp ,Jpeg oSvg . |

### Esempi

Mostra come configurare la compressione durante il salvataggio di un documento come JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Imposta la proprietà "JpegQuality" su "10" per utilizzare una compressione più forte durante il rendering del documento.
// Ciò ridurrà le dimensioni del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Imposta la proprietà "JpegQuality" su "100" per utilizzare una compressione più debole durante il rendering del documento.
// Ciò migliorerà la qualità dell'immagine al costo di una maggiore dimensione del file.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../imagesaveoptions/)
* assemblea [Aspose.Words](../../../)


