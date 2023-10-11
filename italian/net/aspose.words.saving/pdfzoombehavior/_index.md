---
title: Enum PdfZoomBehavior
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.PdfZoomBehavior enum. Specifica il tipo di zoom applicato a un documento PDF quando viene aperto in un visualizzatore PDF.
type: docs
weight: 5540
url: /it/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Specifica il tipo di zoom applicato a un documento PDF quando viene aperto in un visualizzatore PDF.

```csharp
public enum PdfZoomBehavior
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Il modo in cui viene visualizzato il documento è lasciato al visualizzatore PDF. Di solito il visualizzatore visualizza il documento adattandolo alla larghezza della pagina. |
| ZoomFactor | `1` | Visualizza la pagina utilizzando il fattore di zoom specificato. |
| FitPage | `2` | Visualizza la pagina in modo che sia visibile interamente. |
| FitWidth | `3` | Si adatta alla larghezza della pagina. |
| FitHeight | `4` | Si adatta all'altezza della pagina. |
| FitBox | `5` | Si adatta al riquadro di delimitazione (rettangolo contenente tutti gli elementi visibili sulla pagina). |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


