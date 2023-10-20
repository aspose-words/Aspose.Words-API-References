---
title: ShapeBase.CoordOrigin
linktitle: CoordOrigin
articleTitle: CoordOrigin
second_title: Aspose.Words für .NET
description: ShapeBase CoordOrigin eigendom. Die Koordinaten in der oberen linken Ecke des enthaltenden Blocks dieser Form in C#.
type: docs
weight: 110
url: /de/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Die Koordinaten in der oberen linken Ecke des enthaltenden Blocks dieser Form.

```csharp
public Point CoordOrigin { get; set; }
```

## Bemerkungen

Der Standardwert ist (0,0).

## Beispiele

Zeigt, wie die x- und y-Koordinatenposition auf der Koordinatenebene einer Form in eine Position auf der Koordinatenebene der übergeordneten Form übersetzt wird.

```csharp
Document doc = new Document();

// Fügen Sie eine Gruppenform ein und platzieren Sie sie 100 Punkte unterhalb und rechts davon
// der X- und Y-Koordinatenursprungspunkt des Dokuments.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Verwenden Sie die Methode „LocalToParent“, um (0, 0) für die internen X- und Y-Koordinaten der Gruppe zu bestimmen
// liegt auf (100, 100) des Koordinatensystems seiner übergeordneten Form. Das übergeordnete Element der Gruppenform ist das Dokument selbst.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Standardmäßig hat die interne Koordinatenebene einer Form die obere linke Ecke bei (0, 0),
// und die untere rechte Ecke bei (1000, 1000). Aufgrund seiner Größe umfasst unsere Gruppenform eine Fläche von 500pt x 500pt
// in der Dokumentebene. Dies bedeutet, dass eine Bewegung von 1 Punkt auf der Koordinatenebene des Dokuments übersetzt wird
// zu einer Bewegung von 2 Punkten auf der Koordinatenebene der Gruppenform.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Verschiebe den Ursprung der x- und y-Achse der Gruppenform von der oberen linken Ecke in die Mitte.
// Dadurch werden die internen Koordinaten der Gruppe relativ zu den Koordinaten des Dokuments noch weiter versetzt.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Das Ändern des Maßstabs der Koordinatenebene wirkt sich auch auf relative Standorte aus.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Wenn wir dieser Gruppe eine Form hinzufügen möchten, während wir ihre Position basierend auf einer Position im Dokument definieren,
// Wir müssen zunächst eine Position in der Gruppenform bestätigen, die mit der Position des Dokuments übereinstimmt.
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

Zeigt, wie eine Gruppenform erstellt und gefüllt wird.

```csharp
Document doc = new Document();

// Eine Gruppenform erstellen. Eine Gruppenform kann eine Sammlung untergeordneter Formknoten anzeigen.
// Klicken Sie in Microsoft Word innerhalb der Begrenzung der Gruppenform oder auf eine der untergeordneten Formen der Gruppenform
// Wählen Sie alle anderen untergeordneten Formen innerhalb dieser Gruppe aus und erlauben Sie uns, alle Formen gleichzeitig zu skalieren und zu verschieben.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Erstellen Sie eine 400 x 400 Punkt große Gruppenform und platzieren Sie sie am Koordinatenursprung der schwebenden Form des Dokuments.
group.Bounds = new RectangleF(0, 0, 400, 400);

// Legen Sie die Größe der internen Koordinatenebene der Gruppe auf 500 x 500 pt fest. 
// Die obere linke Ecke der Gruppe hat eine x- und y-Koordinate von (0, 0),
// und die untere rechte Ecke hat eine x- und y-Koordinate von (500, 500).
group.CoordSize = new Size(500, 500);

// Setze die Koordinaten der oberen linken Ecke der Gruppe auf (-250, -250). 
// Das Zentrum der Gruppe hat jetzt einen x- und y-Koordinatenwert von (0, 0),
// und die untere rechte Ecke wird bei (250, 250) sein.
group.CoordOrigin = new Point(-250, -250);

// Erstelle ein Rechteck, das die Grenze dieser Gruppenform anzeigt, und füge es der Gruppe hinzu.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Sobald eine Form Teil einer Gruppenform ist, können wir als untergeordneter Knoten darauf zugreifen und sie dann ändern.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Erstelle einen kleinen roten Stern und füge ihn in die Gruppe ein.
// Richten Sie die Form am Koordinatenursprung der Gruppe aus, den wir in die Mitte verschoben haben.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// Ein Rechteck einfügen und dann ein etwas kleineres Rechteck an derselben Stelle mit einem Bild einfügen. 
// Neuere Formen, die wir der Gruppe hinzufügen, überlappen ältere Formen. Das hellblaue Rechteck überlappt teilweise den roten Stern.
// und dann überlappt die Form mit dem Bild das hellblaue Rechteck und verwendet es als Rahmen.
// Wir können die „ZOrder“-Eigenschaften von Formen nicht verwenden, um ihre Anordnung innerhalb einer Gruppenform zu manipulieren. 
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

// Ein Textfeld in die Gruppenform einfügen. Stellen Sie die Eigenschaft „Links“ so ein, dass der rechte Rand des Textfelds angezeigt wird
// berührt die rechte Grenze der Gruppenform. Legen Sie die Eigenschaft „Oben“ so fest, dass das Textfeld außen liegt
// die Grenze der Gruppenform, wobei ihre obere Größe am unteren Rand der Gruppenform ausgerichtet ist.
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

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
