---
title: DeleteRow
second_title: Aspose.Words för .NET API Referens
description: Tar bort en rad från en tabell.
type: docs
weight: 180
url: /sv/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Tar bort en rad från en tabell.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableIndex | Int32 | Tabellens index. |
| rowIndex | Int32 | Indexet för raden i tabellen. |

### Returvärde

Radnoden som just togs bort.

### Anmärkningar

Om markören är inuti raden som tas bort, flyttas markören ut till nästa rad eller till nästa stycke efter tabellen.

Om du tar bort en rad från en tabell som bara innehåller en rad tas tabellen whole bort.

För indexparametrarna, när index är större än eller lika med 0, anger det ett index from början med 0 som det första elementet. När index är mindre än 0, specificerade det ett index från slutet med -1 som det sista elementet.

### Exempel

Visar hur man tar bort en rad från en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// Ta bort den första raden i den första tabellen i dokumentet.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Se även

* class [Row](../../../aspose.words.tables/row)
* class [DocumentBuilder](../../documentbuilder)
* namnutrymme [Aspose.Words](../../documentbuilder)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
