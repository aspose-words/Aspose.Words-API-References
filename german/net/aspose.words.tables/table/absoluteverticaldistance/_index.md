---
title: Table.AbsoluteVerticalDistance
linktitle: AbsoluteVerticalDistance
articleTitle: AbsoluteVerticalDistance
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „AbsoluteVerticalDistance“ für Tabellen – steuern Sie die vertikale Positionierung in Punkten für ein präzises Layout. Der Standardwert ist 0. Optimieren Sie Ihr Design!
type: docs
weight: 30
url: /de/net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

Ruft die absolute vertikale Position der schwebenden Tabelle ab oder legt sie in Punkten fest, die durch die Tabelleneigenschaften angegeben wird. Der Standardwert ist 0.

```csharp
public double AbsoluteVerticalDistance { get; set; }
```

## Beispiele

Zeigt, wie die Position schwebender Tabellen festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Legen Sie die Position der Tabelle auf eine Stelle auf der Seite fest, in diesem Fall beispielsweise auf die untere rechte Ecke.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

    // Wir können auch einen horizontalen und vertikalen Versatz in Punkten von der Position des Absatzes festlegen, an der wir die Tabelle eingefügt haben.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
