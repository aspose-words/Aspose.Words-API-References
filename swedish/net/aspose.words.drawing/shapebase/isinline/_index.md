---
title: ShapeBase.IsInline
second_title: Aspose.Words för .NET API Referens
description: ShapeBase fast egendom. Ett snabbt sätt att avgöra om denna form är placerad i linje med text.
type: docs
weight: 280
url: /sv/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Ett snabbt sätt att avgöra om denna form är placerad i linje med text.

```csharp
public bool IsInline { get; }
```

### Anmärkningar

Har effekt endast för former på högsta nivå.

### Exempel

Visar hur man avgör om en form är inline eller flytande.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två typer av omslag som former kan ha.
// 1 - Inline:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// En inline-form sitter inuti ett stycke bland andra styckeelement, som t.ex.
// I Microsoft Word kan vi klicka och dra formen till valfritt stycke som om det vore ett tecken.
// Om formen är stor kommer det att påverka vertikalt styckeavstånd.
// Vi kan inte flytta den här formen till en plats utan stycke.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Flytande:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// En flytande form tillhör stycket som vi infogar den i,
// som vi kan bestämma av en ankarsymbol som dyker upp när vi klickar på formen.
// Om formen inte har en synlig ankarsymbol till vänster,
// vi kommer att behöva aktivera synliga ankare via "Alternativ" -> "Visa" -> "Objektankare".
// I Microsoft Word kan vi vänsterklicka och dra den här formen fritt till valfri plats.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../shapebase/)
* hopsättning [Aspose.Words](../../../)


