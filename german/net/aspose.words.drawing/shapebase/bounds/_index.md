---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase Bounds-Eigenschaft, um die Position und Größe Ihrer Form mühelos zu verwalten und so die Präzision und Effizienz Ihres Designs zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Ruft die Position und Größe des umgebenden Blocks der Form ab oder legt diese fest.

```csharp
public RectangleF Bounds { get; set; }
```

## Bemerkungen

Ignoriert die Seitenverhältnissperre beim Einstellen.

Bei einer Form der obersten Ebene wird der Wert in Punkten angegeben und ist relativ zum Formanker.

Bei Formen in einer Gruppe liegt der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe vor.

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

Zeigt, wie eine Gruppenform erstellt und ausgefüllt wird.

```csharp
Document doc = new Document();

// Erstellen Sie eine Gruppenform. Eine Gruppenform kann eine Sammlung untergeordneter Formknoten anzeigen.
// In Microsoft Word führt ein Klick innerhalb der Grenzen der Gruppenform oder auf eine der untergeordneten Formen der Gruppenform dazu,
// Wählen Sie alle anderen untergeordneten Formen innerhalb dieser Gruppe aus und ermöglichen Sie uns, alle Formen gleichzeitig zu skalieren und zu verschieben.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Erstellen Sie eine 400pt x 400pt große Gruppenform und platzieren Sie sie am Koordinatenursprung der schwebenden Form des Dokuments.
group.Bounds = new RectangleF(0, 0, 400, 400);

    // Stellen Sie die Größe der internen Koordinatenebene der Gruppe auf 500 x 500 pt ein.
// Die obere linke Ecke der Gruppe hat eine x- und y-Koordinate von (0, 0),
// und die untere rechte Ecke hat eine x- und y-Koordinate von (500, 500).
group.CoordSize = new Size(500, 500);

    // Setze die Koordinaten der oberen linken Ecke der Gruppe auf (-250, -250).
// Der Mittelpunkt der Gruppe hat jetzt einen x- und y-Koordinatenwert von (0, 0),
// und die untere rechte Ecke befindet sich bei (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Erstellen Sie ein Rechteck, das die Grenze dieser Gruppenform anzeigt, und fügen Sie es der Gruppe hinzu.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// Sobald eine Form Teil einer Gruppenform ist, können wir darauf als untergeordneten Knoten zugreifen und sie dann ändern.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Erstelle einen kleinen roten Stern und füge ihn in die Gruppe ein.
// Richten Sie die Form am Koordinatenursprung der Gruppe aus, den wir in die Mitte verschoben haben.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// Fügen Sie ein Rechteck ein und fügen Sie dann an derselben Stelle ein etwas kleineres Rechteck mit einem Bild ein.
// Neuere Formen, die wir der Gruppe hinzufügen, überlappen ältere Formen. Das hellblaue Rechteck überlappt teilweise den roten Stern.
// und dann überlappt die Form mit dem Bild das hellblaue Rechteck und verwendet es als Rahmen.
// Wir können die „ZOrder“-Eigenschaften von Formen nicht verwenden, um ihre Anordnung innerhalb einer Gruppenform zu manipulieren.
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Fügen Sie ein Textfeld in die Gruppenform ein. Setzen Sie die Eigenschaft "Left" so, dass der rechte Rand des Textfelds
// berührt die rechte Grenze der Gruppenform. Setzen Sie die Eigenschaft "Top" so, dass das Textfeld außerhalb
// die Grenze der Gruppenform, wobei ihre obere Größe am unteren Rand der Gruppenform ausgerichtet ist.
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
