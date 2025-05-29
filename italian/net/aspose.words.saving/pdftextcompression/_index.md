---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.PdfTextCompression per una compressione efficiente dei contenuti PDF, migliorando le dimensioni e le prestazioni dei file e preservando la qualità.
type: docs
weight: 6330
url: /it/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Specifica un tipo di compressione applicato a tutto il contenuto del file PDF, ad eccezione delle immagini.

```csharp
public enum PdfTextCompression
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessuna compressione. |
| Flate | `1` | Compressione Flate (ZIP). |

## Esempi

Mostra come applicare la compressione del testo quando si salva un documento in formato PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "TextCompression" su "PdfTextCompression.None" per non applicare alcun
// compressione del testo quando salviamo il documento in PDF.
// Imposta la proprietà "TextCompression" su "PdfTextCompression.Flate" per applicare la compressione ZIP
// in testo quando salviamo il documento in PDF. Più grande è il documento, maggiore sarà l'impatto.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
