---
title: RowFormat.ClearFormatting
second_title: Aspose.Words für .NET-API-Referenz
description: RowFormat methode. Setzt auf StandardZeilenformatierung zurück.
type: docs
weight: 60
url: /de/net/aspose.words.tables/rowformat/clearformatting/
---
## RowFormat.ClearFormatting method

Setzt auf Standard-Zeilenformatierung zurück.

```csharp
public void ClearFormatting()
```

### Beispiele

Zeigt, wie eine Tabelle mit benutzerdefinierten Rahmen erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen Dokumentersteller
// wendet sie auf jede Zeile und Zelle an, die wir damit hinzufügen.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Wenn Sie die Formatierung ändern, wird sie auf die aktuelle Zelle angewendet,
// und alle neuen Zellen, die wir danach mit dem Builder erstellen.
// Dies wirkt sich nicht auf die zuvor hinzugefügten Zellen aus.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Erhöhen Sie die Zeilenhöhe, um sie an den vertikalen Text anzupassen.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Siehe auch

* class [RowFormat](../)
* namensraum [Aspose.Words.Tables](../../rowformat/)
* Montage [Aspose.Words](../../../)


