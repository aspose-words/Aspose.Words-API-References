---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words per .NET
description: Scopri la proprietà UseGdiRasterOperationsEmulation di MetafileRenderingOptions per ottimizzare le operazioni raster con GDI. Migliora prestazioni e flessibilità oggi stesso!
type: docs
weight: 80
url: /it/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Ottiene o imposta un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Osservazioni

La libreria GDI+ di Windows può essere utilizzata per emulare le operazioni raster. Supporta tutte le operazioni raster rispetto all'emulazione di Aspose.Words, ma in alcuni casi le prestazioni potrebbero essere inferiori.

Quando questo valore è impostato su`VERO`Aspose.Words utilizza GDI+ per l'emulazione delle operazioni raster.

Quando questo valore è impostato su`falso`Aspose.Words utilizza la propria implementazione di emulazione delle operazioni raster.

Questa opzione viene utilizzata solo quando il metafile viene renderizzato come grafica vettoriale.

Il valore predefinito è`falso`.

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

* class [MetafileRenderingOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
