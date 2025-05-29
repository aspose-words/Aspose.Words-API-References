---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.PdfZoomBehavior per personalizzare le impostazioni di zoom dei PDF. Migliora l'esperienza utente con opzioni di visualizzazione personalizzate nei documenti PDF.
type: docs
weight: 6340
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
| None | `0` | La modalità di visualizzazione del documento è lasciata al visualizzatore PDF. Di solito, il visualizzatore visualizza il documento in modo che si adatti alla larghezza della pagina. |
| ZoomFactor | `1` | Visualizza la pagina utilizzando il fattore di zoom specificato. |
| FitPage | `2` | Visualizza la pagina in modo che sia completamente visibile. |
| FitWidth | `3` | Si adatta alla larghezza della pagina. |
| FitHeight | `4` | Si adatta all'altezza della pagina. |
| FitBox | `5` | Adatta il riquadro di delimitazione (rettangolo contenente tutti gli elementi visibili sulla pagina). |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
