---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ShapeBase ZOrder förbättrar din design genom att styra visningsordningen för överlappande former för en tydligare och mer organiserad layout.
type: docs
weight: 650
url: /sv/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Bestämmer visningsordningen för överlappande former.

```csharp
public int ZOrder { get; set; }
```

## Anmärkningar

Har endast effekt för former på översta nivån.

Standardvärdet är 0.

Numret representerar staplingsprioriteten. En form med ett högre nummer kommer att visas som om den överlappade ("framför") en form med ett lägre nummer.

Ordningen på överlappande former är oberoende av former i sidhuvudet och i main -texten i dokumentet.

Visningsordningen för underformer i en gruppform bestäms av deras order inuti gruppformen.

## Exempel

Visar hur man manipulerar ordningen på former.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga tre rektanglar i olika färger som delvis överlappar varandra.
// När vi infogar en form som överlappar en annan form, placerar Aspose.Words den nyare formen ovanpå den gamla.
// Den ljusgröna rektangeln kommer att överlappa den ljusblå rektangeln och delvis skymma den,
// och den ljusblå rektangeln kommer att dölja den orange rektangeln.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// Egenskapen "ZOrder" för en form avgör dess staplingsprioritet bland andra överlappande former.
// Om två överlappande former har olika "ZOrder"-värden,
 // Microsoft Word placerar formen med ett högre värde över formen med det lägre värdet.
// Ställ in "ZOrder"-värdena för våra former så att den första orange rektangeln placeras över den andra ljusblå
// och den andra ljusblå rektangeln över den tredje ljusgröna rektangeln.
// Detta kommer att omvända deras ursprungliga staplingsordning.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
