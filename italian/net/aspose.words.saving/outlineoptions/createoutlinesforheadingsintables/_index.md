---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words per .NET
description: Scopri come la proprietà CreateOutlinesForHeadingsInTables ottimizza l'organizzazione delle tabelle abilitando le strutture per gli stili dei titoli, migliorando così la chiarezza del documento.
type: docs
weight: 40
url: /it/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Specifica se creare o meno strutture per i titoli (paragrafi formattati con gli stili di titolo) all'interno delle tabelle.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

## Esempi

Mostra come creare voci di struttura di documenti PDF per le intestazioni all'interno delle tabelle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella con tre righe. La prima riga,
// il cui testo formatteremo in uno stile di tipo titolo, servirà come intestazione di colonna.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Il documento PDF di output conterrà una struttura, ovvero un indice che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema verremo indirizzati alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "1" per ottenere lo schema
// per registrare solo le intestazioni con livelli di intestazione non maggiori di 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Imposta la proprietà "CreateOutlinesForHeadingsInTables" su "false" per escludere tutte le intestazioni all'interno delle tabelle,
// come quello che abbiamo creato sopra partendo dallo schema.
// Imposta la proprietà "CreateOutlinesForHeadingsInTables" su "true" per includere tutte le intestazioni nelle tabelle
// nello schema, a condizione che abbiano un livello di intestazione non maggiore del valore della proprietà "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Guarda anche

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
