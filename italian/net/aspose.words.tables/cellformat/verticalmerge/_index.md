---
title: CellFormat.VerticalMerge
linktitle: VerticalMerge
articleTitle: VerticalMerge
second_title: Aspose.Words per .NET
description: Scopri la proprietà CellFormat VerticalMerge per unire le celle verticali in modo fluido nei fogli di calcolo. Migliora l'organizzazione e la presentazione dei dati senza sforzo!
type: docs
weight: 130
url: /it/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

Specifica come la cella viene unita verticalmente con altre celle.

```csharp
public CellMerge VerticalMerge { get; set; }
```

## Osservazioni

Le celle possono essere unite verticalmente solo se i loro limiti sinistro e destro sono identici.

Quando le celle vengono unite verticalmente, le aree di visualizzazione delle celle unite vengono consolidate. L'area consolidata viene utilizzata per visualizzare il contenuto della prima cella unita verticalmente e tutte le altre celle unite verticalmente devono essere vuote.

## Esempi

Stampa il tipo di unione orizzontale e verticale di una cella.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows)
        foreach (Cell cell in row.Cells)
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

Mostra come unire verticalmente le celle di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce una cella nella prima colonna della prima riga.
// Questa cella sarà la prima di un intervallo di celle unite verticalmente.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Inserisce una cella nella seconda colonna della prima riga, quindi termina la riga.
// Inoltre, configurare il builder per disabilitare l'unione verticale nelle celle create.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Inserisce una cella nella prima colonna della seconda riga.
// Invece di aggiungere contenuto di testo, uniremo questa cella con la prima cella che abbiamo aggiunto direttamente sopra.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Inserisce un'altra cella indipendente nella seconda colonna della seconda riga.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Guarda anche

* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
