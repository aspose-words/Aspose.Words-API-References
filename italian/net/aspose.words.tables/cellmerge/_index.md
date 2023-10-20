---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words per .NET
description: Aspose.Words.Tables.CellMerge enum. Specifica il modo in cui una cella in una tabella viene unita ad altre celle in C#.
type: docs
weight: 6270
url: /it/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Specifica il modo in cui una cella in una tabella viene unita ad altre celle.

```csharp
public enum CellMerge
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | La cella non è unita. |
| First | `1` | La cella è la prima cella in un intervallo di celle unite. |
| Previous | `2` | La cella viene unita alla cella precedente orizzontalmente o verticalmente. |

## Esempi

Mostra come unire le celle della tabella orizzontalmente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una cella nella prima colonna della prima riga.
// Questa cella sarà la prima di un intervallo di celle unite orizzontalmente.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Inserisci una cella nella seconda colonna della prima riga. Invece di aggiungere contenuti di testo,
// uniremo questa cella con la prima cella che abbiamo aggiunto direttamente a sinistra.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Inserisci altre due celle non unite nella seconda riga.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Stampa il tipo di unione orizzontale e verticale di una cella.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows.OfType<Row>())
        foreach (Cell cell in row.Cells.OfType<Cell>())
            Console.WriteLine(PrintCellMergeType(cell));
}

public string PrintCellMergeType(Cell cell)
{
    bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
    bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
    string cellLocation =
        $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";

    if (isHorizontallyMerged && isVerticallyMerged)
        return $"The cell at {cellLocation} is both horizontally and vertically merged";
    if (isHorizontallyMerged)
        return $"The cell at {cellLocation} is horizontally merged.";

    return isVerticallyMerged ? $"The cell at {cellLocation} is vertically merged" : $"The cell at {cellLocation} is not merged";
}
```

Mostra come unire verticalmente le celle della tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una cella nella prima colonna della prima riga.
// Questa cella sarà la prima di un intervallo di celle unite verticalmente.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Inserisci una cella nella seconda colonna della prima riga, quindi termina la riga.
// Inoltre, configura il builder per disabilitare l'unione verticale nelle celle create.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Inserisci una cella nella prima colonna della seconda riga.
// Invece di aggiungere contenuti di testo, uniremo questa cella con la prima cella che abbiamo aggiunto direttamente sopra.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Inserisci un'altra cella indipendente nella seconda colonna della seconda riga.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)
