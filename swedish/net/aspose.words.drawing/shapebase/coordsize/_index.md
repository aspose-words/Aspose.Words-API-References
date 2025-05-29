---
title: ShapeBase.CoordSize
linktitle: CoordSize
articleTitle: CoordSize
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase CoordSize-egenskapen, som definierar koordinatutrymmets bredd och höjd för optimal layoutkontroll i dina designprojekt.
type: docs
weight: 120
url: /sv/net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

Bredden och höjden på koordinatutrymmet inuti det block som innehåller den här formen.

```csharp
public Size CoordSize { get; set; }
```

## Anmärkningar

Standardvärdet är (1000, 1000).

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

Visar hur man skapar och fyller i en gruppform.

```csharp
Document doc = new Document();

// Skapa en gruppform. En gruppform kan visa en samling av underordnade formnoder.
// I Microsoft Word, klickar du inom gruppformens gräns eller på en av gruppformens underformer
// välj alla andra barnformer inom den här gruppen och låt oss skala och flytta alla former samtidigt.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Skapa en gruppform på 400pt x 400pt och placera den vid dokumentets flytande formens koordinatorigo.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Sätt gruppens interna koordinatplanstorlek till 500 x 500pt.
// Det övre vänstra hörnet av gruppen kommer att ha x- och y-koordinaterna (0, 0),
// och det nedre högra hörnet kommer att ha x- och y-koordinaterna (500, 500).
group.CoordSize = new Size(500, 500);

 // Sätt koordinaterna för gruppens övre vänstra hörn till (-250, -250).
// Gruppens centrum kommer nu att ha x- och y-koordinatvärdena (0, 0),
// och det nedre högra hörnet kommer att vara vid (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Skapa en rektangel som visar gränsen för den här gruppformen och lägg till den i gruppen.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// När en form är en del av en gruppform kan vi komma åt den som en underordnad nod och sedan ändra den.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Skapa en liten röd stjärna och sätt in den i gruppen.
// Rikta in formen med gruppens koordinatorigo, som vi har flyttat till mitten.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// Infoga en rektangel och infoga sedan en något mindre rektangel på samma plats med en bild.
// Nyare former som vi lägger till i gruppen överlappar äldre former. Den ljusblå rektangeln kommer delvis att överlappa den röda stjärnan,
// och sedan kommer formen med bilden att överlappa den ljusblå rektangeln och använda den som en ram.
// Vi kan inte använda "ZOrder"-egenskaperna för former för att manipulera deras arrangemang inom en gruppform.
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

// Infoga en textruta i gruppformen. Ställ in egenskapen "Vänster" så att textrutans högra kant
// berör den högra gränsen för gruppformen. Ställ in egenskapen "Överst" så att textrutan sitter utanför
// gruppformens gräns, med dess övre storlek uppradad längs gruppformens nedre marginal.
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

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
