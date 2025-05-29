---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words für .NET
description: Transformieren Sie lokale Koordinaten in den übergeordneten Formraum mit der ShapeBase LocalToParent-Methode. Steigern Sie noch heute die Präzision Ihrer 3D-Modellierungsprojekte!
type: docs
weight: 680
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

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
