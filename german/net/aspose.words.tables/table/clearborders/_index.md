---
title: Table.ClearBorders
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Entfernt alle Tabellen und Zellränder dieser Tabelle.
type: docs
weight: 370
url: /de/net/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method

Entfernt alle Tabellen- und Zellränder dieser Tabelle.

```csharp
public void ClearBorders()
```

### Beispiele

Zeigt, wie Sie einen Gliederungsrahmen auf eine Tabelle anwenden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Richten Sie die Tabelle an der Mitte der Seite aus.
table.Alignment = TableAlignment.Center;

// Löschen Sie alle vorhandenen Rahmen und Schattierungen aus der Tabelle.
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

// Farbe und Dicke des oberen Randes ändern.
Border topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];
table.SetBorder(BorderType.Top, LineStyle.Double, 1.5, Color.Red, true);

Assert.AreEqual(1.5d, topBorder.LineWidth);
Assert.AreEqual(Color.Red.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.Double, topBorder.LineStyle);

// Löschen Sie die Ränder aller Zellen in der Tabelle und speichern Sie dann das Dokument.
table.ClearBorders();
doc.Save(ArtifactsDir + "Table.ClearBorders.docx");

// Überprüfen Sie die Werte der Eigenschaften der Tabelle nach dem erneuten Öffnen des Dokuments.
doc = new Document(ArtifactsDir + "Table.ClearBorders.docx");
table = doc.FirstSection.Body.Tables[0];
topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];

Assert.AreEqual(0.0d, topBorder.LineWidth);
Assert.AreEqual(Color.Empty.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.None, topBorder.LineStyle);
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


