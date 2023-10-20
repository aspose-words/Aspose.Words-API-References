---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words för .NET
description: ShapeBase BoundsInPoints fast egendom. Hämtar platsen och storleken på formens innehållande block i punkter i förhållande till ankaret för den översta formen i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Hämtar platsen och storleken på formens innehållande block i punkter, i förhållande till ankaret för den översta formen.

```csharp
public RectangleF BoundsInPoints { get; }
```

## Exempel

Visar hur man verifierar form som innehåller blockgränser.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Även om själva raden tar lite plats på dokumentsidan,
// det upptar ett rektangulärt innehållande block, vars storlek vi kan bestämma med "Bounds"-egenskaperna.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Skapa en gruppform och ställ sedan in storleken på dess innehållande block med hjälp av egenskapen "Bounds".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Skapa en rektangel, verifiera storleken på dess begränsningsblock och lägg sedan till den i gruppformen.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Gruppformens koordinatplan har sitt ursprung i det övre vänstra hörnet av dess innehållande block,
// och x- och y-koordinaterna för (1000, 1000) i det nedre högra hörnet.
// Vår gruppform är 250x250pt i storlek, så varje 4pt på gruppformens koordinatplan
// översätts till 1pt i dokumentkroppens koordinatplan.
// Varje form som vi infogar kommer också att krympa i storlek med en faktor 4.
// Ändringen i formens "BoundsInPoints"-egenskap kommer att återspegla detta.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Infoga en form och placera den utanför gränserna för gruppformens innehållsblock.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Gruppformens fotavtryck i dokumentkroppen har ökat, men innehållsblocket förblir detsamma.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
