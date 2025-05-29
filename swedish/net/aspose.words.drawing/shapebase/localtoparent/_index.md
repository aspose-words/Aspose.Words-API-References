---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words för .NET
description: Omvandla lokala koordinater till överordnade formutrymmen med ShapeBase LocalToParent-metoden. Förbättra precisionen i dina 3D-modelleringsprojekt idag!
type: docs
weight: 680
url: /sv/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Konverterar ett värde från det lokala koordinatrummet till koordinatrummet för den överordnade formen.

```csharp
public PointF LocalToParent(PointF value)
```

## Exempel

Visar hur man översätter x- och y-koordinaternas position på en forms koordinatplan till en position på den överordnade formens koordinatplan.

```csharp
Document doc = new Document();

// Infoga en gruppform och placera den 100 punkter under och till höger om
// dokumentets x- och Y-koordinatutgångspunkt.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Använd metoden "LocalToParent" för att bestämma att (0, 0) på gruppens interna x- och y-koordinater
// ligger på (100, 100) i dess överordnade forms koordinatsystem. Gruppformens överordnade element är själva dokumentet.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Som standard har en forms interna koordinatplan det övre vänstra hörnet vid (0, 0),
// och det nedre högra hörnet vid (1000, 1000). På grund av sin storlek täcker vår gruppform en yta på 500pt x 500pt
// i dokumentets plan. Detta innebär att en förflyttning på 1 pt på dokumentets koordinatplan kommer att förskjutas
// till en förflyttning på 2 punkter på gruppformens koordinatplan.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Flytta gruppformens x- och y-axelorigo från det övre vänstra hörnet till mitten.
// Detta kommer att förskjuta gruppens interna koordinater i förhållande till dokumentets koordinater ytterligare.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Att ändra skalan på koordinatplanet påverkar också relativa positioner.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Om vi vill lägga till en form till den här gruppen samtidigt som vi definierar dess plats baserat på en plats i dokumentet,
// vi måste först bekräfta en plats i gruppformen som matchar dokumentets plats.
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

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
