---
title: Table.ClearBorders
linktitle: ClearBorders
articleTitle: ClearBorders
second_title: Aspose.Words für .NET
description: Entdecken Sie die Table ClearBorders-Methode, um mühelos alle Tabellen- und Zellenränder zu entfernen und so die Klarheit und Attraktivität Ihres Designs zu verbessern.
type: docs
weight: 390
url: /de/net/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method

Entfernt alle Tabellen- und Zellenränder dieser Tabelle.

```csharp
public void ClearBorders()
```

## Beispiele

Zeigt, wie Sie einer Tabelle einen Gliederungsrahmen hinzufügen.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Richten Sie die Tabelle an der Seitenmitte aus.
table.Alignment = TableAlignment.Center;

// Alle vorhandenen Ränder und Schattierungen aus der Tabelle löschen.
table.ClearBorders();
table.ClearShading();

// Fügen Sie dem Umriss der Tabelle grüne Ränder hinzu.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Füllen Sie die Zellen mit einer hellgrünen Volltonfarbe.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

Zeigt, wie alle Rahmen aus einer Tabelle entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

// Ändern Sie die Farbe und Dicke des oberen Rahmens.
Border topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];
table.SetBorder(BorderType.Top, LineStyle.Double, 1.5, Color.Red, true);

Assert.AreEqual(1.5d, topBorder.LineWidth);
Assert.AreEqual(Color.Red.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.Double, topBorder.LineStyle);

// Löschen Sie die Ränder aller Zellen in der Tabelle und speichern Sie dann das Dokument.
table.ClearBorders();
doc.Save(ArtifactsDir + "Table.ClearBorders.docx");

// Überprüfen Sie die Werte der Tabelleneigenschaften, nachdem Sie das Dokument erneut geöffnet haben.
doc = new Document(ArtifactsDir + "Table.ClearBorders.docx");
table = doc.FirstSection.Body.Tables[0];
topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];

Assert.AreEqual(0.0d, topBorder.LineWidth);
Assert.AreEqual(Color.Empty.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.None, topBorder.LineStyle);
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
