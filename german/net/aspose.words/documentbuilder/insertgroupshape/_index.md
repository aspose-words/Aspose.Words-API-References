---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words für .NET
description: Gruppieren Sie Formen mühelos mit der InsertGroupShape-Methode von DocumentBuilder. Erstellen Sie übersichtliche Designs durch nahtloses Einfügen neuer GroupShape-Knoten.
type: docs
weight: 360
url: /de/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

Gruppiert die als Parameter übergebenen Formen in einem neuen GroupShape-Knoten, der an der aktuellen Position eingefügt wird.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapes | ShapeBase[] | Die Liste der zu gruppierenden Formen. |

## Bemerkungen

Die Position und Dimension der neuen GroupShape werden automatisch berechnet.

VML- und DML-Formen können nicht gruppiert werden.

## Beispiele

Zeigt, wie die Gruppenform mit der Form kombiniert wird.

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

// Kombinieren Sie Formen zu einem GroupShape-Knoten, der an der angegebenen Position eingefügt wird.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// Kombinieren Sie Shape- und GroupShape-Knoten.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

Zeigt, wie eine DML-Gruppenform eingefügt wird.

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

// Abmessungen für den neuen GroupShape-Knoten.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Fügen Sie einen GroupShape-Knoten der angegebenen Größe ein, der an der angegebenen Position eingefügt wird.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Fügen Sie einen GroupShape-Knoten ein, dessen Position und Dimension automatisch berechnet werden.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Siehe auch

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

Gruppiert die als Parameter übergebenen Formen in einem neuen GroupShape-Knoten der angegebenen Größe, der an der angegebenen Position eingefügt wird.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite der Gruppenform. |
| top | Double | Abstand in Punkten vom Ursprung zur Oberseite der Gruppenform. |
| width | Double | Die Breite der Gruppenform in Punkten. Ein negativer Wert ist nicht zulässig. |
| height | Double | Die Höhe der Gruppenform in Punkten. Ein negativer Wert ist nicht zulässig. |
| shapes | ShapeBase[] | Die Liste der zu gruppierenden Formen. |

## Bemerkungen

VML- und DML-Formen können nicht gruppiert werden.

## Beispiele

Zeigt, wie eine DML-Gruppenform eingefügt wird.

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

// Abmessungen für den neuen GroupShape-Knoten.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Fügen Sie einen GroupShape-Knoten der angegebenen Größe ein, der an der angegebenen Position eingefügt wird.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Fügen Sie einen GroupShape-Knoten ein, dessen Position und Dimension automatisch berechnet werden.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Siehe auch

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
