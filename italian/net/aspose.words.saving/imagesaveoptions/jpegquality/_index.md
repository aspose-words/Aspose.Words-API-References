---
title: ImageSaveOptions.JpegQuality
second_title: Aspose.Words per .NET API Reference
description: ImageSaveOptions proprietà. Ottiene o imposta un valore che determina la qualità delle immagini JPEG generate.
type: docs
weight: 80
url: /it/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Ottiene o imposta un valore che determina la qualità delle immagini JPEG generate.

```csharp
public int JpegQuality { get; set; }
```

### Osservazioni

Ha effetto solo quando si salva in JPEG.

Utilizzare questa proprietà per ottenere o impostare la qualità delle immagini generate durante il salvataggio in formato JPEG. Il valore può variare da 0 a 100 dove 0 significa qualità peggiore ma compressione massima e 100 significa qualità migliore ma compressione minima.

Il valore predefinito è 95.

### Esempi

Mostra come configurare la compressione durante il salvataggio di un documento come JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo trasforma il documento in un'immagine.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Imposta la proprietà "JpegQuality" su "10" per utilizzare una compressione più forte durante il rendering del documento.
// Ciò ridurrà la dimensione del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Imposta la proprietà "JpegQuality" su "100" per utilizzare una compressione più debole durante il rendering del documento.
// Ciò migliorerà la qualità dell'immagine al costo di un aumento delle dimensioni del file.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../imagesaveoptions/)
* assemblea [Aspose.Words](../../../)


