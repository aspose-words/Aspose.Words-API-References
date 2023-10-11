---
title: Table.TextWrapping
second_title: Aspose.Words für .NET-API-Referenz
description: Table eigendom. Ruft ab oder legt festTextWrapping für Tabelle.
type: docs
weight: 310
url: /de/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Ruft ab oder legt fest`TextWrapping` für Tabelle.

```csharp
public TextWrapping TextWrapping { get; set; }
```

### Beispiele

Zeigt, wie man mit Tabellentextumbrüchen arbeitet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Setzen Sie die Eigenschaft „TextWrapping“ auf „TextWrapping.Around“, damit die Tabelle den Text umbricht.
// und schiebe es nach unten in den Absatz darunter, indem du die Position festlegst.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Siehe auch

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


