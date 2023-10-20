---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words per .NET
description: OutlineOptions CreateOutlinesForHeadingsInTables proprietà. Specifica se creare o meno i contorni delle intestazioni paragrafi formattati con gli stili Intestazione allinterno delle tabelle in C#.
type: docs
weight: 40
url: /it/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Specifica se creare o meno i contorni delle intestazioni (paragrafi formattati con gli stili Intestazione) all'interno delle tabelle.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

## Esempi

Mostra come creare voci di struttura del documento PDF per le intestazioni all'interno delle tabelle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella con tre righe. La prima fila,
// il cui testo formatteremo in uno stile di tipo intestazione, fungerà da intestazione di colonna.
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

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Il documento PDF di output conterrà una struttura, ovvero un sommario che elenca le intestazioni nel corpo del documento.
// Facendo clic su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "1" per ottenere la struttura
// per registrare solo le intestazioni con livelli di intestazione non superiori a 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Imposta la proprietà "CreateOutlinesForHeadingsInTables" su "false" per escludere tutte le intestazioni all'interno delle tabelle,
// come quello che abbiamo creato sopra dallo schema.
// Imposta la proprietà "CreateOutlinesForHeadingsInTables" su "true" per includere tutte le intestazioni all'interno delle tabelle
// nella struttura, a condizione che abbiano un livello di intestazione non maggiore del valore della proprietà "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Guarda anche

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
