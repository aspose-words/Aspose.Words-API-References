---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Eigenschaft „BoundsInPoints“, um einfach auf die Größe und Position einer Form in Punkten zuzugreifen und so die Präzision Ihres Designs und die Kontrolle über das Layout zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Ruft die Position und Größe des umgebenden Blocks der Form in Punkten relativ zum Anker der obersten Form ab.

```csharp
public RectangleF BoundsInPoints { get; }
```

## Bemerkungen

Die zurückgegebenen Grenzen beinhalten nicht die Drehung dieser Form oder die Drehung der übergeordneten Gruppenform, falls vorhanden.

## Beispiele

Zeigt, wie die Form mit Blockgrenzen überprüft wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Auch wenn die Zeile selbst wenig Platz auf der Dokumentseite einnimmt,
// es belegt einen rechteckigen Block, dessen Größe wir mithilfe der „Bounds“-Eigenschaften bestimmen können.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Erstellen Sie eine Gruppenform und legen Sie dann die Größe des enthaltenen Blocks mithilfe der Eigenschaft „Grenzen“ fest.
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

// Die Koordinatenebene der Gruppenform hat ihren Ursprung in der oberen linken Ecke des enthaltenen Blocks.
// und die x- und y-Koordinaten von (1000, 1000) in der unteren rechten Ecke.
// Unsere Gruppenform ist 250x250pt groß, also alle 4pt auf der Koordinatenebene der Gruppenform
// wird in 1pt in der Koordinatenebene des Dokumentkörpers übersetzt.
// Jede Form, die wir einfügen, wird ebenfalls um den Faktor 4 verkleinert.
// Die Änderung der Eigenschaft „BoundsInPoints“ der Form wird dies widerspiegeln.
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

// Der Platzbedarf der Gruppenform im Dokumenttext wurde vergrößert, der enthaltene Block bleibt jedoch derselbe.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
