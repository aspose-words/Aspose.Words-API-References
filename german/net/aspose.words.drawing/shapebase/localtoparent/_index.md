---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words für .NET
description: ShapeBase LocalToParent methode. Konvertiert einen Wert aus dem lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form in C#.
type: docs
weight: 670
url: /de/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Konvertiert einen Wert aus dem lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form.

```csharp
public PointF LocalToParent(PointF value)
```

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

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
