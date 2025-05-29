---
title: ShapeBase.CoordOrigin
linktitle: CoordOrigin
articleTitle: CoordOrigin
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase CoordOrigin-Eigenschaft zur Optimierung Ihrer Designs. Greifen Sie auf die genauen Koordinaten der oberen linken Ecke des Blocks zu, der Ihre Form enthält.
type: docs
weight: 110
url: /de/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Die Koordinaten in der oberen linken Ecke des umschließenden Blocks dieser Form.

```csharp
public Point CoordOrigin { get; set; }
```

## Bemerkungen

Der Standardwert ist (0,0).

## Beispiele

Zeigt, wie die x- und y-Koordinatenposition auf der Koordinatenebene einer Form in eine Position auf der Koordinatenebene der übergeordneten Form übersetzt wird.

```csharp
Document doc = new Document();

// Fügen Sie eine Gruppenform ein und platzieren Sie sie 100 Punkte unterhalb und rechts von
// der Ursprungspunkt der X- und Y-Koordinaten des Dokuments.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Verwenden Sie die Methode "LocalToParent", um zu bestimmen, dass (0, 0) auf den internen x- und y-Koordinaten der Gruppe
// liegt auf (100, 100) des Koordinatensystems der übergeordneten Form. Das übergeordnete Element der Gruppenform ist das Dokument selbst.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Standardmäßig liegt die obere linke Ecke der internen Koordinatenebene einer Form bei (0, 0),
// und die untere rechte Ecke bei (1000, 1000). Aufgrund seiner Größe deckt unsere Gruppenform eine Fläche von 500pt x 500pt ab
// in der Ebene des Dokuments. Das bedeutet, dass eine Bewegung von 1pt auf der Koordinatenebene des Dokuments
// zu einer Bewegung von 2 Punkten auf der Koordinatenebene der Gruppenform.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Verschieben Sie den Ursprung der X- und Y-Achse der Gruppenform von der oberen linken Ecke in die Mitte.
// Dadurch werden die internen Koordinaten der Gruppe im Verhältnis zu den Koordinaten des Dokuments noch weiter verschoben.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Das Ändern des Maßstabs der Koordinatenebene wirkt sich auch auf die relativen Positionen aus.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Wenn wir dieser Gruppe eine Form hinzufügen möchten und dabei ihre Position basierend auf einer Position im Dokument definieren,
// Wir müssen zuerst einen Speicherort in der Gruppenform bestätigen, der mit dem Speicherort des Dokuments übereinstimmt.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
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
