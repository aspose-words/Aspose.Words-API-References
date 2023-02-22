---
title: ShapeBase.ZOrder
second_title: Aspose.Words för .NET API Referens
description: ShapeBase fast egendom. Bestämmer visningsordningen för överlappande former.
type: docs
weight: 550
url: /sv/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Bestämmer visningsordningen för överlappande former.

```csharp
public int ZOrder { get; set; }
```

### Anmärkningar

Har effekt endast för former på högsta nivå.

Standardvärdet är 0.

Siffran representerar staplingsprioriteten. En form med ett högre nummer kommer att visas som om den överlappar (framför) en form med ett lägre nummer.

Ordningen på överlappande former är oberoende för former i rubriken och i huvudtexten i dokumentet.

Visningsordningen för underordnade former i en gruppform bestäms av deras order inuti gruppformen.

### Exempel

Visar hur man manipulerar ordningen på formerna.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga tre olika färgade rektanglar som delvis överlappar varandra.
// När vi infogar en form som överlappar en annan form, placerar Aspose.Words den nyare formen ovanpå den gamla.
// Den ljusgröna rektangeln kommer att överlappa den ljusblå rektangeln och delvis skymma den,
// och den ljusblå rektangeln kommer att skymma den orangea rektangeln.
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

// Egenskapen "ZOrder" för en form bestämmer dess staplingsprioritet bland andra överlappande former.
// Om två överlappande former har olika "ZOrder"-värden,
  // Microsoft Word kommer att placera formen med ett högre värde över formen med det lägre värdet.
// Ställ in "ZOrder"-värdena för våra former för att placera den första orangea rektangeln över den andra ljusblå
// och den andra ljusblå rektangeln över den tredje ljusgröna rektangeln.
// Detta kommer att vända deras ursprungliga staplingsordning.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../shapebase/)
* hopsättning [Aspose.Words](../../../)


