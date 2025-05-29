---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words för .NET
description: Gruppera former enkelt med DocumentBuilders InsertGroupShape-metod. Skapa organiserade designer genom att sömlöst infoga nya GroupShape-noder.
type: docs
weight: 360
url: /sv/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

Grupperar de former som skickas som en parameter till en ny GroupShape-nod som infogas i den aktuella positionen.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| shapes | ShapeBase[] | Listan över former som ska grupperas. |

## Anmärkningar

Positionen och dimensionen för den nya gruppformen beräknas automatiskt.

VML- och DML-former kan inte grupperas tillsammans.

## Exempel

Visar hur man kombinerar gruppform med formen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Kombinera former till en GroupShape-nod som infogas på den angivna positionen.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// Kombinera noderna Form och Gruppform.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

Visar hur man infogar en DML-gruppform.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Dimensioner för den nya GroupShape-noden.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Infoga GroupShape-nod för den angivna storleken som infogas i den angivna positionen.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Infoga GroupShape-noden vars position och dimension beräknas automatiskt.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Se även

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

Grupperar de former som skickas som en parameter till en ny GroupShape-nod med den angivna storleken som infogas på den angivna positionen.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| left | Double | Avstånd i punkter från origo till vänster sida av gruppformen. |
| top | Double | Avstånd i punkter från origo till gruppformens översida. |
| width | Double | Gruppformens bredd i punkter. Ett negativt värde är inte tillåtet. |
| height | Double | Höjden på gruppformen i punkter. Ett negativt värde är inte tillåtet. |
| shapes | ShapeBase[] | Listan över former som ska grupperas. |

## Anmärkningar

VML- och DML-former kan inte grupperas tillsammans.

## Exempel

Visar hur man infogar en DML-gruppform.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Dimensioner för den nya GroupShape-noden.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Infoga GroupShape-nod för den angivna storleken som infogas i den angivna positionen.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Infoga GroupShape-noden vars position och dimension beräknas automatiskt.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Se även

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
