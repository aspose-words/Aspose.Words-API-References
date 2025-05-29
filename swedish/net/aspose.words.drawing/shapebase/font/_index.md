---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase Font-egenskapen för enkel åtkomst till teckensnittsformatering. Förbättra dina designer med anpassningsbara textstilar och unika typografiska alternativ.
type: docs
weight: 190
url: /sv/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Ger åtkomst till teckensnittsformateringen för detta objekt.

```csharp
public Font Font { get; }
```

## Exempel

Visar hur man infogar en textruta och anger teckensnittet för dess innehåll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Sätt egenskapen "Hidden" för formens "Font"-objekt till "true" för att dölja textrutan
// och komprimera det utrymme som den normalt skulle uppta.
// Sätt egenskapen "Hidden" för formens "Font"-objekt till "false" för att lämna textrutan synlig.
shape.Font.Hidden = hideShape;

// Om formen är synlig kommer vi att ändra dess utseende via font-objektet.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Flytta verktyget ut ur textrutan tillbaka till huvuddokumentet.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Se även

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
