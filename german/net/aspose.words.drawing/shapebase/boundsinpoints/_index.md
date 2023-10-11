---
title: ShapeBase.BoundsInPoints
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ruft die Position und Größe des enthaltenden Blocks der Form in Punkten ab relativ zum Anker der obersten Form.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Ruft die Position und Größe des enthaltenden Blocks der Form in Punkten ab, relativ zum Anker der obersten Form.

```csharp
public RectangleF BoundsInPoints { get; }
```

### Beispiele

Zeigt, wie eine Form überprüft wird, die Blockgrenzen enthält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Obwohl die Zeile selbst nur wenig Platz auf der Dokumentseite einnimmt,
// es belegt einen rechteckigen enthaltenden Block, dessen Größe wir mithilfe der „Bounds“-Eigenschaften bestimmen können.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Erstellen Sie eine Gruppenform und legen Sie dann die Größe des enthaltenden Blocks mithilfe der Eigenschaft „Bounds“ fest.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Erstellen Sie ein Rechteck, überprüfen Sie die Größe seines Begrenzungsblocks und fügen Sie ihn dann der Gruppenform hinzu.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Die Koordinatenebene der Gruppenform hat ihren Ursprung in der oberen linken Ecke des enthaltenden Blocks.
// und die x- und y-Koordinaten von (1000, 1000) in der unteren rechten Ecke.
// Unsere Gruppenform ist 250 x 250 Punkte groß, also alle 4 Punkte auf der Koordinatenebene der Gruppenform
// übersetzt in 1pt in der Koordinatenebene des Dokumentkörpers.
// Jede Form, die wir einfügen, wird ebenfalls um den Faktor 4 verkleinert.
// Die Änderung in der Eigenschaft „BoundsInPoints“ der Form wird dies widerspiegeln.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Eine Form einfügen und außerhalb der Grenzen des enthaltenden Blocks der Gruppenform platzieren.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Der Platzbedarf der Gruppenform im Dokumentkörper hat zugenommen, aber der enthaltende Block bleibt gleich.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


