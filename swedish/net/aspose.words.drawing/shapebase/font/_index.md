---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: ShapeBase Font fast egendom. Ger tillgång till teckensnittsformateringen för detta objekt i C#.
type: docs
weight: 190
url: /sv/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Ger tillgång till teckensnittsformateringen för detta objekt.

```csharp
public Font Font { get; }
```

## Exempel

Visar hur man infogar en textruta och ställer in teckensnittet för dess innehåll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Ställ in egenskapen "Hidden" för formens "Font"-objekt till "true" för att dölja textrutan.
// och kollapsa utrymmet som det normalt skulle uppta.
// Ställ in egenskapen "Hidden" för formens "Font"-objekt till "false" för att lämna textrutan synlig.
shape.Font.Hidden = hideShape;

// Om formen är synlig kommer vi att ändra dess utseende via teckensnittsobjektet.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Flytta byggaren från textrutan tillbaka till huvuddokumentet.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Se även

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
