---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words per .NET
description: Ottimizza il salvataggio EMF con ImageSaveOptions. Controlla le impostazioni del rendering GDI o Aspose.Words per migliorare la qualità e le prestazioni delle immagini.
type: docs
weight: 190
url: /it/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Ottiene o imposta un valore che determina se utilizzare il renderer metafile GDI+ o Aspose.Words durante il salvataggio in EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Osservazioni

Se impostato su`VERO` Viene utilizzato il renderer GDI+ metafile. Il contenuto viene scritto nell'oggetto graphics GDI+ e salvato nel metafile.

Se impostato su`falso` Viene utilizzato il renderer di metafile Aspose.Words. Il contenuto viene scritto direttamente nel formato metafile con Aspose.Words.

Ha effetto solo se si salva in EMF.

Il salvataggio GDI+ funziona solo su .NET.

Il valore predefinito è`VERO`.

## Esempi

Mostra come scegliere un renderer quando si converte un documento in .emf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine EMF, possiamo passare un oggetto SaveOptions per selezionare un renderer per l'immagine.
// Se impostiamo il flag "UseGdiEmfRenderer" su "true", Aspose.Words utilizzerà il rendering GDI+.
// Se impostiamo il flag "UseGdiEmfRenderer" su "false", Aspose.Words utilizzerà il proprio metafile renderer.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
