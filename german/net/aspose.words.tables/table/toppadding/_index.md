---
title: Table.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words für .NET
description: Entdecken Sie die Table TopPadding-Eigenschaft und passen Sie den Abstand über dem Zelleninhalt einfach in Punkten an, um die Layoutkontrolle und Lesbarkeit zu verbessern.
type: docs
weight: 330
url: /de/net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

Ruft den Abstand (in Punkten) ab, der über dem Inhalt der Zellen hinzugefügt werden soll, oder legt diesen fest.

```csharp
public double TopPadding { get; set; }
```

## Beispiele

Zeigt, wie die Inhaltsauffüllung in einer Tabelle konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

    // Legen Sie für jede Zelle in der Tabelle den Abstand zwischen ihrem Inhalt und ihren jeweiligen Rändern fest.
// Diese Tabelle hält den Mindestabstand durch Umbrechen des Textes ein.
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
