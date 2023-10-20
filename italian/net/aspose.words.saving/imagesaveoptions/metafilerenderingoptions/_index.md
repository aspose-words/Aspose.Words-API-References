---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words per .NET
description: ImageSaveOptions MetafileRenderingOptions proprietà. Permette di specificare come vengono trattati i metafile nelloutput renderizzato in C#.
type: docs
weight: 90
url: /it/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Permette di specificare come vengono trattati i metafile nell'output renderizzato.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Osservazioni

QuandoVector è specificato, Aspose.Words esegue il rendering del metafile in grafica vettoriale utilizzando prima il proprio motore di rendering del metafile, quindi esegue il rendering della grafica vettoriale nell'immagine.

QuandoBitmap è specificato, Aspose.Words renders metafile direttamente nell'immagine utilizzando il motore di rendering dei metafile GDI+.

Il motore di rendering dei metafile GDI+ funziona più velocemente, supporta quasi tutte le funzionalità dei metafile ma a risoluzioni basse potrebbe produrre risultati incoerenti rispetto al resto della grafica vettoriale (specialmente per il testo) sulla pagina. Il motore di rendering dei metafile Aspose.Words produrrà risultati più coerenti even su risoluzioni basse ma funziona più lentamente e potrebbe eseguire il rendering in modo impreciso di metafile complessi.

Il valore predefinito per[`MetafileRenderingMode`](../../metafilerenderingmode/) ÈBitmap.

## Esempi

Mostra come impostare la modalità di rendering quando si salvano documenti con immagini Windows Metafile in altri formati di immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// determina in che modo l'operazione di salvataggio elaborerà i metafile di Windows nel documento.
// Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Vector",
// o "MetafileRenderingMode.VectorWithFallback", eseguiremo il rendering di tutti i metafile come grafica vettoriale.
// Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Bitmap", renderemo tutti i metafile come bitmap.
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
