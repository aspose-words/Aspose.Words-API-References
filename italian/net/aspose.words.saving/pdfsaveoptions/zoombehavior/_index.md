---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words per .NET
description: Scopri PdfSaveOptions ZoomBehavior, controlla le impostazioni di zoom per una visualizzazione ottimale nei visualizzatori PDF. Migliora l'esperienza utente con una visualizzazione personalizzata dei documenti!
type: docs
weight: 350
url: /it/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Ottiene o imposta un valore che determina quale tipo di zoom deve essere applicato quando un documento viene aperto con un visualizzatore PDF.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Osservazioni

Il valore predefinito èNone , ovvero non viene applicato alcun adattamento.

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
