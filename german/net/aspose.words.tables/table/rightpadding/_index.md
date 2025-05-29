---
title: Table.RightPadding
linktitle: RightPadding
articleTitle: RightPadding
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Table RightPadding“, um den Zellenabstand anzupassen. Passen Sie den rechten Rand ganz einfach an, um das Layout und die Lesbarkeit Ihrer Designs zu verbessern.
type: docs
weight: 250
url: /de/net/aspose.words.tables/table/rightpadding/
---
## Table.RightPadding property

Ruft den Abstand (in Punkten) ab, der rechts vom Zelleninhalt hinzugefügt werden soll, oder legt diesen fest.

```csharp
public double RightPadding { get; set; }
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
