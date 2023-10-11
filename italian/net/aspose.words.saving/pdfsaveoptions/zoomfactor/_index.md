---
title: PdfSaveOptions.ZoomFactor
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Ottiene o imposta un valore che determina il fattore di zoom in percentuale per un documento.
type: docs
weight: 330
url: /it/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Ottiene o imposta un valore che determina il fattore di zoom (in percentuale) per un documento.

```csharp
public int ZoomFactor { get; set; }
```

### Osservazioni

Questo valore viene utilizzato solo se[`ZoomBehavior`](../zoombehavior/) è impostato perZoomFactor .

### Esempi

Mostra come impostare lo zoom predefinito applicato da un lettore all'apertura di un documento PDF sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
// Imposta la proprietà "ZoomBehavior" su "PdfZoomBehavior.ZoomFactor" per ottenere un lettore PDF
// applica un fattore di zoom basato su percentuale quando apriamo il documento con esso.
// Imposta la proprietà "ZoomFactor" su "25" per assegnare al fattore di zoom un valore del 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Quando apriamo questo documento utilizzando un lettore come Adobe Acrobat, vedremo il documento ridimensionato a 1/4 della sua dimensione effettiva.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


