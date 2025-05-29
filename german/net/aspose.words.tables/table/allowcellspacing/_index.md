---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words für .NET
description: Entdecken Sie die Tabelleneigenschaft AllowCellSpacing, um den Zellenabstand in Ihren Layouts einfach zu verwalten. Verbessern Sie Ihr Design mit anpassbaren Optionen!
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

Zeigt, wie Sie den Abstand zwischen einzelnen Zellen in einer Tabelle aktivieren.

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

// Setzen Sie die Eigenschaft „AllowCellSpacing“ auf „true“, um den Abstand zwischen den Zellen zu ermöglichen
// mit einer Größe, die dem Wert der Eigenschaft „CellSpacing“ in Punkten entspricht.
// Setzen Sie die Eigenschaft „AllowCellSpacing“ auf „false“, um den Zellenabstand zu deaktivieren
// und ignorieren Sie den Wert der Eigenschaft „CellSpacing“.
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
