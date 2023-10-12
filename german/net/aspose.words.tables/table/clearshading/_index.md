---
title: Table.ClearShading
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Entfernt alle Schattierungen auf der Tabelle.
type: docs
weight: 400
url: /de/net/aspose.words.tables/table/clearshading/
---
## Table.ClearShading method

Entfernt alle Schattierungen auf der Tabelle.

```csharp
public void ClearShading()
```

### Beispiele

Zeigt, wie man einen Umrissrahmen auf eine Tabelle anwendet.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Richten Sie die Tabelle in der Mitte der Seite aus.
table.Alignment = TableAlignment.Center;

// Alle vorhandenen Ränder und Schattierungen aus der Tabelle löschen.
table.ClearBorders();
table.ClearShading();

// Füge grüne Ränder zum Umriss der Tabelle hinzu.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Füllen Sie die Zellen mit einer hellgrünen Volltonfarbe.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


