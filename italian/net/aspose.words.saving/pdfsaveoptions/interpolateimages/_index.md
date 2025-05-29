---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words per .NET
description: Scopri la proprietà InterpolateImages di PdfSaveOptions, una funzionalità chiave che migliora la qualità delle immagini nei tuoi documenti. Ottimizza i tuoi PDF senza sforzo!
type: docs
weight: 210
url: /it/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Un flag che indica se l'interpolazione dell'immagine deve essere eseguita da un lettore conforme. Quando`falso` è specificato, il flag non viene scritto nel documento di output e al suo posto viene utilizzato il comportamento predefinito del lettore.

```csharp
public bool InterpolateImages { get; set; }
```

## Osservazioni

Quando la risoluzione di un'immagine sorgente è significativamente inferiore a quella del dispositivo di output, ogni campione sorgente copre molti pixel del dispositivo. Di conseguenza, le immagini possono apparire irregolari o a blocchi. Questi artefatti visivi possono essere ridotti applicando un algoritmo di interpolazione dell'immagine durante il rendering. Invece di colorare tutti i pixel coperti da un campione sorgente con lo stesso colore, l'interpolazione dell'immagine tenta di produrre una transizione graduale tra i valori dei campioni adiacenti.

Un lettore conforme può scegliere di non implementare questa funzionalità del PDF, oppure può utilizzare qualsiasi implementazione specifica di interpolazione che desidera.

Il valore predefinito è`falso`.

L'uso del flag di interpolazione è vietato dalla conformità PDF/A.`falso` il valore verrà utilizzato automaticamente quando si salva in PDF/A.

## Esempi

Mostra come eseguire l'interpolazione sulle immagini durante il salvataggio di un documento in formato PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Impostare la proprietà "InterpolateImages" su "true" per far sì che il lettore che apre questo documento interpoli le immagini.
// La loro risoluzione dovrebbe essere inferiore a quella del dispositivo che visualizza il documento.
// Impostare la proprietà "InterpolateImages" su "false" per fare in modo che il lettore non applichi alcuna interpolazione.
saveOptions.InterpolateImages = interpolateImages;

// Quando apriamo questo documento con un lettore come Adobe Acrobat, dovremo ingrandire l'immagine
// per vedere l'effetto dell'interpolazione se salviamo il documento con questa opzione abilitata.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
