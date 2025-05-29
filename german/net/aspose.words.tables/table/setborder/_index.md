---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words für .NET
description: Passen Sie das Erscheinungsbild Ihrer Tabelle mit der SetBorder-Methode an – passen Sie Linienstil, Breite und Farbe für ein professionelles Erscheinungsbild an. Verbessern Sie Ihr Design noch heute!
type: docs
weight: 430
url: /de/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Legt für den angegebenen Tabellenrahmen den angegebenen Linienstil, die angegebene Breite und Farbe fest.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderType | BorderType | Der zu ändernde Tabellenrand. |
| lineStyle | LineStyle | Der anzuwendende Linienstil. |
| lineWidth | Double | Die einzustellende Linienbreite (in Punkten). |
| color | Color | Die für den Rahmen zu verwendende Farbe. |
| isOverrideCellBorders | Boolean | Wann`WAHR`, bewirkt, dass alle vorhandenen expliziten Zellränder entfernt werden. |

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

### Siehe auch

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
