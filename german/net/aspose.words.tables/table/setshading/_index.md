---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words für .NET
description: Verbessern Sie das Erscheinungsbild Ihrer Tabelle mit der SetShading-Methode, indem Sie benutzerdefinierte Schattierungswerte anwenden und so ein elegantes, professionelles Erscheinungsbild erzielen.
type: docs
weight: 450
url: /de/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Legt die Schattierung für die gesamte Tabelle auf die angegebenen Werte fest.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| texture | TextureIndex | Die anzuwendende Textur. |
| foregroundColor | Color | Die Farbe der Textur. |
| backgroundColor | Color | Die Farbe der Hintergrundfüllung. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
