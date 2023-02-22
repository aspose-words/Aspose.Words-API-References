---
title: ShapeBase.BoundsInPoints
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ruft die Position und Größe des umgebenden Blocks der Form in Punkt relativ zum Anker der obersten Form ab.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Ruft die Position und Größe des umgebenden Blocks der Form in Punkt relativ zum Anker der obersten Form ab.

```csharp
public RectangleF BoundsInPoints { get; }
```

### Beispiele

Zeigt, wie Form überprüft wird, die Blockgrenzen enthält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Auch wenn die Zeile selbst wenig Platz auf der Dokumentseite einnimmt,
// es belegt einen rechteckigen umgebenden Block, dessen Größe wir mit den "Bounds"-Eigenschaften bestimmen können.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Erstellen Sie eine Gruppenform und legen Sie dann die Größe des umgebenden Blocks mit der Eigenschaft "Grenzen" fest.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Erstellen Sie ein Rechteck, überprüfen Sie die Größe seines Begrenzungsblocks und fügen Sie es dann der Gruppenform hinzu.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Die Koordinatenebene der Gruppenform hat ihren Ursprung in der oberen linken Ecke des umgebenden Blocks,
// und die x- und y-Koordinaten von (1000, 1000) in der unteren rechten Ecke.
// Unsere Gruppenform hat eine Größe von 250 x 250 pt, also alle 4 pt auf der Koordinatenebene der Gruppenform
// übersetzt in 1pt in der Koordinatenebene des Dokumentkörpers.
// Jede Form, die wir einfügen, wird ebenfalls um den Faktor 4 verkleinert.
// Die Änderung der "BoundsInPoints"-Eigenschaft der Form wird dies widerspiegeln.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Fügen Sie eine Form ein und platzieren Sie sie außerhalb der Grenzen des umschließenden Blocks der Gruppenform.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Der Fußabdruck der Gruppenform im Dokumentkörper hat zugenommen, aber der umgebende Block bleibt gleich.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


