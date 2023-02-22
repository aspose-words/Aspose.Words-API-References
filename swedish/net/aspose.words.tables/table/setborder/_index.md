---
title: Table.SetBorder
second_title: Aspose.Words för .NET API Referens
description: Table metod. Ställer in den angivna tabellkanten till angiven linjestil bredd och färg.
type: docs
weight: 410
url: /sv/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Ställer in den angivna tabellkanten till angiven linjestil, bredd och färg.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| borderType | BorderType | Bordskanten att ändra. |
| lineStyle | LineStyle | Linjestilen som ska tillämpas. |
| lineWidth | Double | Linjebredden som ska ställas in (i punkter). |
| color | Color | Färgen som ska användas för bården. |
| isOverrideCellBorders | Boolean | När`Sann`, gör att alla befintliga explicita cellgränser tas bort. |

### Exempel

Visar hur man tillämpar en konturram på en tabell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Rikta in tabellen mot mitten av sidan.
table.Alignment = TableAlignment.Center;

// Rensa alla befintliga kanter och skuggningar från tabellen.
table.ClearBorders();
table.ClearShading();

// Lägg till gröna kanter till tabellens konturer.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Fyll cellerna med en ljusgrön solid färg.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Se även

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)


