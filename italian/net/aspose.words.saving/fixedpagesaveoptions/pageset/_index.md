---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words per .NET
description: Controlla il rendering dei tuoi documenti con FixedPageSaveOptions PageSet. Seleziona facilmente pagine specifiche o sceglile tutte per un output fluido. Ottimizza il tuo flusso di lavoro!
type: docs
weight: 70
url: /it/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Ottiene o imposta le pagine da visualizzare. L'impostazione predefinita è tutte le pagine del documento.

```csharp
public PageSet PageSet { get; set; }
```

## Esempi

Mostra come estrarre le pagine in base agli indici di pagina esatti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungere cinque pagine al documento.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Creiamo un oggetto "XpsSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilizzare la proprietà "PageSet" per selezionare un set di pagine del documento da salvare in output XPS.
// In questo caso, sceglieremo, tramite un indice a partire da zero, solo tre pagine: pagina 1, pagina 2 e pagina 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Mostra come convertire solo alcune pagine di un documento in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui quel metodo converte il documento in .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Impostare "PageIndex" su "1" per eseguire il rendering di una parte del documento a partire dalla seconda pagina.
    options.PageSet = new PageSet(1);

    // Questo documento conterrà una pagina a partire da pagina due, che conterrà solo la seconda pagina.
    doc.Save(stream, options);
}
```

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

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
