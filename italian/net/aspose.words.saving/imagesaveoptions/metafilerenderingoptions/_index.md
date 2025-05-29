---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words per .NET
description: Scopri la proprietà MetafileRenderingOptions di ImageSaveOptions per controllare la gestione dei metafile nell'output renderizzato, per una migliore qualità dell'immagine.
type: docs
weight: 90
url: /it/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Consente di specificare come vengono trattati i metafile nell'output renderizzato.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Osservazioni

QuandoVector se specificato, Aspose.Words esegue prima il rendering del metafile in grafica vettoriale utilizzando il proprio motore di rendering dei metafile e poi esegue il rendering della grafica vector nell'immagine.

QuandoBitmap se specificato, Aspose.Words esegue il rendering del metafile direttamente nell'immagine utilizzando il motore di rendering dei metafile GDI+.

Il motore di rendering dei metafile GDI+ è più veloce e supporta quasi tutte le funzionalità dei metafile, ma a basse risoluzioni potrebbe produrre risultati incoerenti rispetto al resto della grafica vettoriale (soprattutto per il testo) presente sulla pagina. Il motore di rendering dei metafile Aspose.Words produrrà risultati più coerenti anche a basse risoluzioni, ma è più lento e potrebbe rendere in modo impreciso i metafile complessi.

Il valore predefinito per[`MetafileRenderingMode`](../../metafilerenderingmode/) ÈBitmap.

## Esempi

Mostra come impostare la modalità di rendering quando si salvano documenti con immagini Windows Metafile in altri formati di immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// determina come l'operazione di salvataggio elaborerà i metafile di Windows nel documento.
// Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Vector",
// o "MetafileRenderingMode.VectorWithFallback", renderemo tutti i metafile come grafica vettoriale.
// Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Bitmap", tutti i metafile verranno renderizzati come bitmap.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words utilizza GDI+ per l'emulazione delle operazioni raster, quando il valore è impostato su true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Guarda anche

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
