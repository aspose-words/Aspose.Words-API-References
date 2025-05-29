---
title: Table.RelativeVerticalAlignment
linktitle: RelativeVerticalAlignment
articleTitle: RelativeVerticalAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Table RelativeVerticalAlignment“, um die vertikale Ausrichtung schwebender Tabellen einfach zu verwalten und so die Präzision und das Design Ihres Layouts zu verbessern.
type: docs
weight: 240
url: /de/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Ruft die relative vertikale Ausrichtung der schwebenden Tabelle ab oder legt sie fest.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
