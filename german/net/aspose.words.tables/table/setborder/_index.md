---
title: Table.SetBorder
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Setzt den angegebenen Tabellenrahmen auf die angegebene Linienart Breite und Farbe.
type: docs
weight: 410
url: /de/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Setzt den angegebenen Tabellenrahmen auf die angegebene Linienart, Breite und Farbe.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderType | BorderType | Der zu ändernde Tabellenrahmen. |
| lineStyle | LineStyle | Der anzuwendende Linienstil. |
| lineWidth | Double | Die festzulegende Linienbreite (in Punkten). |
| color | Color | Die für den Rahmen zu verwendende Farbe. |
| isOverrideCellBorders | Boolean | Wann`Stimmt`, bewirkt, dass alle vorhandenen expliziten Zellgrenzen entfernt werden. |

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

### Siehe auch

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


