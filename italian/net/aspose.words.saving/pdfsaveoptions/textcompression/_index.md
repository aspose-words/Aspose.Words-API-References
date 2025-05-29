---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextCompression di PdfSaveOptions per ottimizzare i tuoi documenti. Scegli il tipo di compressione migliore per un'archiviazione efficiente del testo e un caricamento più rapido.
type: docs
weight: 310
url: /it/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Specifica il tipo di compressione da utilizzare per tutto il contenuto testuale nel documento.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Osservazioni

Il valore predefinito èFlate.

Aumenta significativamente le dimensioni di output quando si salva un documento senza compressione.

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

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
