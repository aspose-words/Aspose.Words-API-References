---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words för .NET
description: Förbättra ditt bords utseende med metoden SetShading, så att du kan använda anpassade skuggningsvärden för ett polerat och professionellt utseende.
type: docs
weight: 450
url: /sv/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Ställer in skuggning till de angivna värdena för hela tabellen.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| texture | TextureIndex | Texturen som ska appliceras. |
| foregroundColor | Color | Texturens färg. |
| backgroundColor | Color | Färgen på bakgrundsfyllningen. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
