---
title: Table.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words für .NET
description: Table TopPadding eigendom. Ruft die Menge an Platz in Punkten ab die über dem Inhalt von Zellen hinzugefügt werden soll oder legt diese fest in C#.
type: docs
weight: 330
url: /de/net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

Ruft die Menge an Platz (in Punkten) ab, die über dem Inhalt von Zellen hinzugefügt werden soll, oder legt diese fest.

```csharp
public double TopPadding { get; set; }
```

## Beispiele

Zeigt, wie das Auffüllen von Inhalten in einer Tabelle konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Für jede Zelle in der Tabelle den Abstand zwischen ihrem Inhalt und jedem ihrer Ränder festlegen.
// Diese Tabelle behält den minimalen Füllabstand bei, indem Text umbrochen wird.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
