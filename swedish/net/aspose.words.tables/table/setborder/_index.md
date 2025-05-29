---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words för .NET
description: Anpassa din tabells utseende med SetBorder-metoden – justera linjestil, bredd och färg för ett professionellt utseende. Förbättra din design idag!
type: docs
weight: 430
url: /sv/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Ställer in den angivna tabellkanten till den angivna linjestilen, bredden och färgen.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| borderType | BorderType | Tabellkanten som ska ändras. |
| lineStyle | LineStyle | Linjestilen som ska tillämpas. |
| lineWidth | Double | Linjebredden som ska ställas in (i punkter). |
| color | Color | Färgen som ska användas för kanten. |
| isOverrideCellBorders | Boolean | När`sann`, gör att alla befintliga explicita cellkanter tas bort. |

## Exempel

Visar hur man tillämpar en konturkantlinje på en tabell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Justera tabellen till mitten av sidan.
table.Alignment = TableAlignment.Center;

// Ta bort alla befintliga ramar och skuggningar från tabellen.
table.ClearBorders();
table.ClearShading();

// Lägg till gröna ramar runt tabellens kontur.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Fyll cellerna med en ljusgrön enfärgad.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Se även

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
