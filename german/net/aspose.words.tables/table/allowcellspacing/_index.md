---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words für .NET
description: Table AllowCellSpacing eigendom. Ruft die Option Abstand zwischen Zellen zulassen ab oder legt diese fest in C#.
type: docs
weight: 60
url: /de/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Ruft die Option „Abstand zwischen Zellen zulassen“ ab oder legt diese fest.

```csharp
public bool AllowCellSpacing { get; set; }
```

## Beispiele

Zeigt, wie der Abstand zwischen einzelnen Zellen in einer Tabelle aktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Setzen Sie die Eigenschaft „AllowCellSpacing“ auf „true“, um den Abstand zwischen Zellen zu ermöglichen
// mit einer Größe, die dem Wert der Eigenschaft „CellSpacing“ entspricht, in Punkten.
// Setzen Sie die Eigenschaft „AllowCellSpacing“ auf „false“, um den Zellenabstand zu deaktivieren
// und ignoriere den Wert der Eigenschaft „CellSpacing“.
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Durch Anpassen der Eigenschaft „CellSpacing“ wird der Zellenabstand automatisch aktiviert.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
