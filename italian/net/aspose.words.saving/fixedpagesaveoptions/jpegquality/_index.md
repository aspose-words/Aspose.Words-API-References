---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words per .NET
description: Ottimizza la qualità JPEG nei tuoi documenti HTML con FixedPageSaveOptions. Regola facilmente la proprietà JpegQuality per una nitidezza delle immagini straordinaria.
type: docs
weight: 20
url: /it/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento HTML.

```csharp
public int JpegQuality { get; set; }
```

## Osservazioni

Ha effetto solo se un documento contiene immagini JPEG.

Utilizzare questa proprietà per ottenere o impostare la qualità delle immagini all'interno di un documento quando si salva in formato di pagina fisso. Il valore può variare da 0 a 100, dove 0 indica la qualità peggiore ma la massima compressione e 100 indica la qualità migliore ma la minima compressione.

Il valore predefinito è 95.

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

* class [FixedPageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
