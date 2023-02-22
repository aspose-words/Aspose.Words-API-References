---
title: RowFormat.HeadingFormat
second_title: Aspose.Words für .NET-API-Referenz
description: RowFormat eigendom. Wahr wenn die Zeile als Tabellenüberschrift auf jeder Seite wiederholt wird wenn die Tabelle mehr als eine Seite umfasst.
type: docs
weight: 30
url: /de/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

Wahr, wenn die Zeile als Tabellenüberschrift auf jeder Seite wiederholt wird, wenn die Tabelle mehr als eine Seite umfasst.

```csharp
public bool HeadingFormat { get; set; }
```

### Beispiele

Zeigt, wie eine Tabelle mit Zeilen erstellt wird, die sich auf jeder Seite wiederholen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Alle eingefügten Zeilen, während das "HeadingFormat"-Flag auf "true" gesetzt ist
// wird oben in der Tabelle auf jeder Seite angezeigt, die sie umfasst.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// Fügen Sie genügend Zeilen hinzu, damit die Tabelle zwei Seiten umfasst.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### Siehe auch

* class [RowFormat](../)
* namensraum [Aspose.Words.Tables](../../rowformat/)
* Montage [Aspose.Words](../../../)


