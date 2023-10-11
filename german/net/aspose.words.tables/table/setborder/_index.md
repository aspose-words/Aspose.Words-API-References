---
title: Table.SetBorder
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Setzt den angegebenen Tabellenrand auf den angegebenen Linienstil die angegebene Breite und die angegebene Farbe.
type: docs
weight: 430
url: /de/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Setzt den angegebenen Tabellenrand auf den angegebenen Linienstil, die angegebene Breite und die angegebene Farbe.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderType | BorderType | Der Tabellenrand soll geändert werden. |
| lineStyle | LineStyle | Der anzuwendende Linienstil. |
| lineWidth | Double | Die festzulegende Linienbreite (in Punkt). |
| color | Color | Die für den Rand zu verwendende Farbe. |
| isOverrideCellBorders | Boolean | Wann`WAHR`bewirkt, dass alle vorhandenen expliziten Zellränder entfernt werden. |

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


