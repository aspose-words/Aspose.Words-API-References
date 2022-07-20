---
title: CoordSize
second_title: Aspose.Words für .NET-API-Referenz
description: Die Breite und Höhe des Koordinatenraums innerhalb des umgebenden Blocks dieser Form.
type: docs
weight: 120
url: /de/net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

Die Breite und Höhe des Koordinatenraums innerhalb des umgebenden Blocks dieser Form.

```csharp
public Size CoordSize { get; set; }
```

### Bemerkungen

Der Standardwert ist (1000, 1000).

### Beispiele

Zeigt, wie die x- und y-Koordinatenposition auf der Koordinatenebene einer Form in eine Position auf der Koordinatenebene der übergeordneten Form übertragen wird.

```csharp
Document doc = new Document();

// Fügen Sie eine Gruppenform ein und platzieren Sie sie 100 Punkte unterhalb und rechts davon
// der x- und y-Koordinatenursprungspunkt des Dokuments.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Verwenden Sie die "LocalToParent"-Methode, um zu bestimmen, dass (0, 0) auf den internen x- und y-Koordinaten der Gruppe
// liegt auf (100, 100) des Koordinatensystems der übergeordneten Form. Das übergeordnete Element des Gruppen-Shapes ist das Dokument selbst.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Standardmäßig hat die interne Koordinatenebene einer Form die obere linke Ecke bei (0, 0),
// und die untere rechte Ecke bei (1000, 1000). Unsere Gruppenform deckt aufgrund ihrer Größe eine Fläche von 500pt x 500pt ab
// in der Ebene des Dokuments. Dies bedeutet, dass eine Bewegung von 1pt auf der Koordinatenebene des Dokuments verschoben wird
// zu einer Bewegung von 2 Punkten auf der Koordinatenebene der Gruppenform.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Den Ursprung der x- und y-Achse der Gruppenform von der oberen linken Ecke in die Mitte verschieben.
// Dadurch werden die internen Koordinaten der Gruppe relativ zu den Koordinaten des Dokuments noch weiter versetzt.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Das Ändern des Maßstabs der Koordinatenebene wirkt sich auch auf die relativen Positionen aus.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Wenn wir dieser Gruppe eine Form hinzufügen möchten, während wir ihre Position basierend auf einer Position im Dokument definieren,
// Wir müssen zuerst einen Ort in der Gruppenform bestätigen, der mit dem Ort des Dokuments übereinstimmt.
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

Zeigt, wie ein Gruppen-Shape erstellt und ausgefüllt wird.

```csharp
Document doc = new Document();

// Erstellen Sie eine Gruppenform. Ein Gruppen-Shape kann eine Sammlung untergeordneter Shape-Knoten anzeigen.
// In Microsoft Word wird das Klicken innerhalb der Begrenzung der Gruppenform oder auf eine der untergeordneten Formen der Gruppenform
// wähle alle anderen untergeordneten Formen innerhalb dieser Gruppe aus und erlaube uns, alle Formen auf einmal zu skalieren und zu verschieben.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Erstellen Sie eine Gruppenform von 400 pt x 400 pt und platzieren Sie sie am Koordinatenursprung der schwebenden Form des Dokuments.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Legen Sie die Größe der internen Koordinatenebene der Gruppe auf 500 x 500pt fest.
// Die obere linke Ecke der Gruppe hat eine x- und y-Koordinate von (0, 0),
// und die untere rechte Ecke hat eine x- und y-Koordinate von (500, 500).
group.CoordSize = new Size(500, 500);

 // Setze die Koordinaten der oberen linken Ecke der Gruppe auf (-250, -250).
// Das Zentrum der Gruppe hat jetzt einen x- und y-Koordinatenwert von (0, 0),
// und die untere rechte Ecke wird bei (250, 250) sein.
group.CoordOrigin = new Point(-250, -250);

// Erstellen Sie ein Rechteck, das die Grenze dieser Gruppenform anzeigt, und fügen Sie es der Gruppe hinzu.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Sobald eine Form Teil einer Gruppenform ist, können wir darauf als untergeordneten Knoten zugreifen und sie dann ändern.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Erstellen Sie einen kleinen roten Stern und fügen Sie ihn in die Gruppe ein.
// Richten Sie die Form am Koordinatenursprung der Gruppe aus, den wir in die Mitte verschoben haben.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

 // Fügen Sie ein Rechteck ein und fügen Sie dann ein etwas kleineres Rechteck an derselben Stelle mit einem Bild ein.
// Neuere Shapes, die wir der Gruppe hinzufügen, überlappen ältere Shapes. Das hellblaue Rechteck wird den roten Stern teilweise überlappen,
// und dann überlappt die Form mit dem Bild das hellblaue Rechteck und verwendet es als Rahmen.
 // Wir können die "ZOrder"-Eigenschaften von Formen nicht verwenden, um ihre Anordnung innerhalb einer Gruppenform zu manipulieren.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Fügen Sie ein Textfeld in die Gruppenform ein. Stellen Sie die Eigenschaft „Links“ so ein, dass der rechte Rand des Textfelds angezeigt wird
// berührt die rechte Grenze der Gruppenform. Stellen Sie die Eigenschaft "Oben" so ein, dass das Textfeld außen sitzt
// die Grenze der Gruppenform, wobei die obere Größe am unteren Rand der Gruppenform ausgerichtet ist.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Siehe auch

* class [ShapeBase](../../shapebase)
* namensraum [Aspose.Words.Drawing](../../shapebase)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
