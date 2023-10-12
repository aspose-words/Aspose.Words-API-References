---
title: Table.SetShading
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Setzt die Schattierung auf die angegebenen Werte für die gesamte Tabelle.
type: docs
weight: 450
url: /de/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Setzt die Schattierung auf die angegebenen Werte für die gesamte Tabelle.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| texture | TextureIndex | Die anzuwendende Textur. |
| foregroundColor | Color | Die Farbe der Textur. |
| backgroundColor | Color | Die Farbe der Hintergrundfüllung. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


