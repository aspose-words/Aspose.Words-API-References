---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase IsInline-egenskapen för att enkelt kontrollera om din form är i linje med texten, vilket förbättrar din design och förbättrar layouteffektiviteten.
type: docs
weight: 310
url: /sv/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Ett snabbt sätt att avgöra om den här formen är placerad i linje med texten.

```csharp
public bool IsInline { get; }
```

## Anmärkningar

Har endast effekt för former på översta nivån.

## Exempel

Visar hur man avgör om en form är inbäddad eller flytande.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två typer av omslag som former kan ha.
// 1 - Inline:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// En inbäddad form sitter inuti ett stycke bland andra styckeelement, till exempel textsekvenser.
// I Microsoft Word kan vi klicka och dra formen till valfritt stycke som om det vore ett tecken.
// Om formen är stor påverkar det det vertikala styckeavståndet.
// Vi kan inte flytta den här formen till en plats utan stycke.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Flytande:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// En flytande form tillhör stycket som vi infogar den i,
// vilket vi kan avgöra med hjälp av en ankarsymbol som visas när vi klickar på formen.
// Om formen inte har en synlig ankarsymbol till vänster,
// vi måste aktivera synliga ankare via "Alternativ" -> "Visa" -> "Objektankare".
// I Microsoft Word kan vi vänsterklicka och dra den här formen fritt till valfri plats.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
