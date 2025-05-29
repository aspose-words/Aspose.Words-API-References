---
title: PageSet.All
linktitle: All
articleTitle: All
second_title: Aspose.Words per .NET
description: Accedi a tutte le pagine del documento nel loro ordine originale con la proprietà PageSet All. Semplifica il tuo flusso di lavoro e migliora la gestione dei documenti senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words.saving/pageset/all/
---
## PageSet.All property

Ottiene un set con tutte le pagine del documento nel loro ordine originale.

```csharp
public static PageSet All { get; }
```

## Esempi

Mostra come esportare le pagine dispari dal documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Di seguito sono riportate tre proprietà PageSet che possiamo utilizzare per filtrare un insieme di pagine da
// il nostro documento da salvare in un documento PDF di output in base alla parità dei numeri di pagina.
// 1 - Salva solo le pagine pari:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Salva solo le pagine dispari:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Salva ogni pagina:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Guarda anche

* class [PageSet](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
