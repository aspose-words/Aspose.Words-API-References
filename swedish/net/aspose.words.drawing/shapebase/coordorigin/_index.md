---
title: CoordOrigin
second_title: Aspose.Words för .NET API Referens
description: Koordinaterna i det övre vänstra hörnet av det innehållande blocket med denna form.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Koordinaterna i det övre vänstra hörnet av det innehållande blocket med denna form.

```csharp
public Point CoordOrigin { get; set; }
```

### Anmärkningar

Standardvärdet är (0,0).

### Exempel

Visar hur man översätter x- och y-koordinatpositionen på en forms koordinatplan till en plats på den överordnade formens koordinatplan.

```csharp
Document doc = new Document();

// Infoga en gruppform och placera den 100 punkter under och till höger om
// dokumentets ursprungspunkt för x- och Y-koordinater.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Använd metoden "LocalToParent" för att bestämma att (0, 0) på gruppens interna x- och y-koordinater
// ligger på (100, 100) av sin överordnade forms koordinatsystem. Gruppformens överordnade är själva dokumentet.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Som standard har en forms interna koordinatplan det övre vänstra hörnet vid (0, 0),
// och det nedre högra hörnet vid (1000, 1000). På grund av sin storlek täcker vår gruppform ett område på 500pt x 500pt
// i dokumentets plan. Detta innebär att en rörelse på 1pt på dokumentets koordinatplan kommer att översättas
// till en rörelse av 2pts på gruppformens koordinatplan.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Flytta gruppformens x- och y-axelursprung från det övre vänstra hörnet till mitten.
// Detta kommer att förskjuta gruppens interna koordinater i förhållande till dokumentets koordinater ytterligare.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Ändring av skalan på koordinatplanet kommer också att påverka relativa platser.
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
// I Microsoft Word klickar du inom gruppformens gräns eller på en av gruppformens underordnade former
// välj alla andra underordnade former inom den här gruppen och låt oss skala och flytta alla former på en gång.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Skapa en 400pt x 400pt gruppform och placera den vid dokumentets flytande formkoordinatursprung.
group.Bounds = new RectangleF(0, 0, 400, 400);

  // Ställ in gruppens interna koordinatplansstorlek till 500 x 500pt.
// Det övre vänstra hörnet av gruppen kommer att ha en x- och y-koordinater av (0, 0),
// och det nedre högra hörnet kommer att ha en x- och y-koordinater på (500, 500).
group.CoordSize = new Size(500, 500);

  // Ställ in koordinaterna för gruppens övre vänstra hörn till (-250, -250).
// Gruppens centrum kommer nu att ha ett x- och y-koordinatvärde på (0, 0),
// och det nedre högra hörnet kommer att vara på (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Skapa en rektangel som visar gränsen för denna gruppform och lägg till den i gruppen.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// När en form är en del av en gruppform kan vi komma åt den som en undernod och sedan ändra den.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Skapa en liten röd stjärna och infoga den i gruppen.
// Rikta upp formen med gruppens koordinatursprung, som vi har flyttat till mitten.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

  // Infoga en rektangel, och sedan infoga en lite mindre rektangel på samma plats med en bild.
// Nyare former som vi lägger till i gruppen överlappar äldre former. Den ljusblå rektangeln kommer delvis att överlappa den röda stjärnan,
// och sedan kommer formen med bilden att överlappa den ljusblå rektangeln och använda den som en ram.
  // Vi kan inte använda "ZOrder"-egenskaperna för former för att manipulera deras arrangemang inom en gruppform.
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

// Infoga en textruta i gruppformen. Ställ in egenskapen "Vänster" så att textrutans högra kant
// vidrör den högra gränsen för gruppformen. Ställ in egenskapen "Top" så att textrutan sitter utanför
// gränsen för gruppformen, med dess övre storlek uppradad längs gruppformens nedre marginal.
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

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../shapebase/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
