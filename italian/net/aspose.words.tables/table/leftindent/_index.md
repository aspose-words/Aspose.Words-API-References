---
title: Table.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Tabella LeftIndent" per personalizzare facilmente il rientro sinistro della tua tabella. Migliora il tuo design con un controllo preciso per layout migliori!
type: docs
weight: 190
url: /it/net/aspose.words.tables/table/leftindent/
---
## Table.LeftIndent property

Ottiene o imposta il valore che rappresenta il rientro sinistro della tabella.

```csharp
public double LeftIndent { get; set; }
```

## Esempi

Mostra come creare una tabella formattata utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Imposta alcune opzioni di formattazione per l'aspetto del testo e della tabella.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// La configurazione delle opzioni di formattazione in un generatore di documenti le applicherà
// alla cella/riga corrente in cui si trova il cursore,
// nonché tutte le nuove celle e righe create utilizzando quel generatore.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Riconfiguriamo gli oggetti di formattazione del builder per le nuove righe e celle che stiamo per creare.
// Il builder non applicherà queste modifiche alla prima riga già creata, in modo che questa risalti come riga di intestazione.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
