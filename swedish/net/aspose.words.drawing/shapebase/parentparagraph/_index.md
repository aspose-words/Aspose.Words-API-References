---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase ParentParagraph-egenskapen – få effektiv åtkomst till det omedelbara överordnade stycket för effektiv innehållshantering och förbättrad organisation.
type: docs
weight: 430
url: /sv/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Returnerar det omedelbara överordnade stycket.

```csharp
public Paragraph ParentParagraph { get; }
```

## Anmärkningar

För underformer till en gruppform och underformer till ett Office Math-objekt returneras alltid`null`.

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
