---
title: Enum CellVerticalAlignment
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Tables.CellVerticalAlignment enum. Specifica la giustificazione verticale del testo allinterno di una cella di tabella.
type: docs
weight: 6280
url: /it/net/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enumeration

Specifica la giustificazione verticale del testo all'interno di una cella di tabella.

```csharp
public enum CellVerticalAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Top | `0` | Il testo è allineato nella parte superiore di una cella. |
| Center | `1` | Il testo è allineato al centro di una cella. |
| Bottom | `2` | Il testo è allineato in fondo alla cella. |

### Esempi

Mostra come creare una tabella 2x2 formattata.

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

// Durante la creazione della tabella, il generatore di documenti applicherà i valori correnti della proprietà RowFormat/CellFormat
// alla riga/cella corrente in cui si trova il cursore e a qualsiasi nuova riga/cella mentre le crea.
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

// Le righe e le celle aggiunte in precedenza non vengono influenzate retroattivamente dalle modifiche alla formattazione del builder.
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


