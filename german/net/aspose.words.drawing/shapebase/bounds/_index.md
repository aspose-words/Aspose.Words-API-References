---
title: Bounds
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft die Position und Größe des umgebenden Blocks der Form ab oder legt sie fest.
type: docs
weight: 70
url: /de/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Ruft die Position und Größe des umgebenden Blocks der Form ab oder legt sie fest.

```csharp
public RectangleF Bounds { get; set; }
```

### Bemerkungen

Ignoriert die Sperre des Seitenverhältnisses bei der Einstellung.

Bei einer Form der obersten Ebene wird der Wert in Punkten angegeben und ist relativ zum Formanker.

Bei Formen in einer Gruppe befindet sich der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe.

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

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
