---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Tables.AutoFitBehavior per ottimizzare il ridimensionamento delle tabelle con il metodo AutoFit, migliorando il layout e la presentazione del documento.
type: docs
weight: 7080
url: /it/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Determina come Aspose.Words ridimensiona la tabella quando si richiama il[`AutoFit`](../table/autofit/) metodo.

```csharp
public enum AutoFitBehavior
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words abilita l'opzione Adatta automaticamente, rimuove la larghezza preferita dalla tabella e da tutte le celle e quindi aggiorna il layout della tabella. |
| AutoFitToWindow | `1` | Quando si utilizza questo valore, Aspose.Words abilita l'opzione Adatta automaticamente, imposta la larghezza preferita per la tabella al 100%, rimuove le larghezze preferite da tutte le celle e quindi aggiorna il layout della tabella. |
| FixedColumnWidths | `2` | Aspose.Words disabilita l'opzione Adatta automaticamente e rimuove il valore preferito dalla tabella. |

## Esempi

Mostra come creare una nuova tabella applicando uno stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Dobbiamo inserire almeno una riga prima di impostare qualsiasi formattazione della tabella.
builder.InsertCell();

// Imposta lo stile della tabella utilizzato in base all'identificatore di stile.
// Nota che non tutti gli stili di tabella sono disponibili quando si salva in formato .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Applica parzialmente lo stile alle caratteristiche della tabella in base ai predicati, quindi crea la tabella.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

Mostra come creare una tabella formattata 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Durante la creazione della tabella, il generatore di documenti applicherà i valori correnti delle proprietà RowFormat/CellFormat
// alla riga/cella corrente in cui si trova il cursore e a tutte le nuove righe/celle man mano che vengono create.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Le righe e le celle aggiunte in precedenza non vengono retroattivamente influenzate dalle modifiche apportate alla formattazione del builder.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)
