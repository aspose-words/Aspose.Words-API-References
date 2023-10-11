---
title: PdfSaveOptions.InterpolateImages
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Un flag che indica se linterpolazione dellimmagine deve essere eseguita da un lettore conforme. Quandofalso è specificato il flag non viene scritto nel documento di output e al suo posto viene utilizzato il comportamento predefinito del lettore.
type: docs
weight: 210
url: /it/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Un flag che indica se l'interpolazione dell'immagine deve essere eseguita da un lettore conforme. Quando`falso` è specificato, il flag non viene scritto nel documento di output e al suo posto viene utilizzato il comportamento predefinito del lettore.

```csharp
public bool InterpolateImages { get; set; }
```

### Osservazioni

Quando la risoluzione di un'immagine sorgente è significativamente inferiore a quella del dispositivo di output, ciascun campione sorgente copre molti pixel del dispositivo. Di conseguenza, le immagini possono apparire frastagliate o squadrate. Questi artefatti visivi possono essere ridotti applicando un algoritmo di interpolazione dell'immagine durante il rendering. Invece di dipingere tutti i pixel coperti da un campione sorgente con lo stesso colore, l'interpolazione dell'immagine tenta di produrre un'immagine uniforme transizione tra valori campione adiacenti.

Un lettore conforme può scegliere di non implementare questa funzionalità del PDF, o può utilizzare qualsiasi implementazione specifica di interpolazione che desidera.

Il valore predefinito è`falso`.

Il flag di interpolazione è vietato dalla conformità PDF/A.`falso` il valore verrà utilizzato automaticamente durante il salvataggio in PDF/A.

### Esempi

Mostra come eseguire l'interpolazione sulle immagini durante il salvataggio di un documento in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "InterpolateImages" su "true" per fare in modo che il lettore che apre questo documento interpoli le immagini.
// La loro risoluzione dovrebbe essere inferiore a quella del dispositivo che visualizza il documento.
// Imposta la proprietà "InterpolateImages" su "false" per fare in modo che il lettore non applichi alcuna interpolazione.
saveOptions.InterpolateImages = interpolateImages;

// Quando apriamo questo documento con un lettore come Adobe Acrobat, dovremo ingrandire l'immagine
// per vedere l'effetto dell'interpolazione se salvassimo il documento con questa opzione abilitata.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

Mostra come migliorare la qualità di un'immagine nei documenti renderizzati (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "InterpolateImages" su "true" per fare in modo che il lettore che apre questo documento interpoli le immagini.
// La loro risoluzione dovrebbe essere inferiore a quella del dispositivo che visualizza il documento.
// Imposta la proprietà "InterpolateImages" su "false" per fare in modo che il lettore non applichi alcuna interpolazione.
saveOptions.InterpolateImages = interpolateImages;

// Quando apriamo questo documento con un lettore come Adobe Acrobat, dovremo ingrandire l'immagine
// per vedere l'effetto dell'interpolazione se salvassimo il documento con questa opzione abilitata.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


