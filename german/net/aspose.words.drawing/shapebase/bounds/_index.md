---
title: ShapeBase.Bounds
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ruft die Position und Größe des enthaltenden Blocks der Form ab oder legt diese fest.
type: docs
weight: 70
url: /de/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Ruft die Position und Größe des enthaltenden Blocks der Form ab oder legt diese fest.

```csharp
public RectangleF Bounds { get; set; }
```

### Bemerkungen

Ignoriert die Sperre des Seitenverhältnisses bei der Einstellung.

Für eine Form der obersten Ebene wird der Wert in Punkten und relativ zum Formanker angegeben.

Für Formen in einer Gruppe liegt der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe.

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
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


