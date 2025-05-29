---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words per .NET
description: Scopri la proprietà ZoomFactor di PdfSaveOptions per regolare facilmente i livelli di zoom del documento in percentuale, migliorando così l'esperienza di visualizzazione dei PDF.
type: docs
weight: 360
url: /it/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Ottiene o imposta un valore che determina il fattore di zoom (in percentuale) per un documento.

```csharp
public int ZoomFactor { get; set; }
```

## Osservazioni

Questo valore viene utilizzato solo se[`ZoomBehavior`](../zoombehavior/) è impostato suZoomFactor .

## Esempi

Mostra come impostare lo zoom predefinito che un lettore applica quando apre un documento PDF renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
// Imposta la proprietà "ZoomBehavior" su "PdfZoomBehavior.ZoomFactor" per ottenere un lettore PDF
// applichiamo un fattore di zoom percentuale quando apriamo il documento con esso.
// Impostare la proprietà "ZoomFactor" su "25" per assegnare al fattore di zoom un valore del 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Quando apriamo questo documento utilizzando un lettore come Adobe Acrobat, lo vedremo ridimensionato a 1/4 delle sue dimensioni reali.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
