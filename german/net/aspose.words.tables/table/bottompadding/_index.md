---
title: Table.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words für .NET
description: Table BottomPadding eigendom. Ruft den Abstand in Punkten ab der unterhalb des Zellinhalts hinzugefügt werden soll oder legt diesen fest in C#.
type: docs
weight: 90
url: /de/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

Ruft den Abstand (in Punkten) ab, der unterhalb des Zellinhalts hinzugefügt werden soll, oder legt diesen fest.

```csharp
public double BottomPadding { get; set; }
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
