---
title: Bounds
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in platsen och storleken på formens innehållsblock.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Hämtar eller ställer in platsen och storleken på formens innehållsblock.

```csharp
public RectangleF Bounds { get; set; }
```

### Anmärkningar

Ignorerar bildförhållandelås vid inställning.

För en form på toppnivå är värdet i punkter och i förhållande till formankaret.

För former i en grupp finns värdet i koordinatutrymmet och enheterna för den överordnade gruppen.

### Exempel

Visar hur man verifierar form som innehåller blockgränser.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Även om själva raden tar lite plats på dokumentsidan,
// det upptar ett rektangulärt innehållande block, vars storlek vi kan bestämma med "Bounds"-egenskaperna.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Skapa en gruppform och ställ sedan in storleken på dess innehållande block med hjälp av egenskapen "Bounds".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Skapa en rektangel, verifiera storleken på dess begränsningsblock och lägg sedan till den i gruppformen.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Gruppformens koordinatplan har sitt ursprung i det övre vänstra hörnet av dess innehållande block,
// och x- och y-koordinaterna för (1000, 1000) i det nedre högra hörnet.
// Vår gruppform är 250x250pt i storlek, så varje 4pt på gruppformens koordinatplan
// översätts till 1pt i dokumentkroppens koordinatplan.
// Varje form som vi infogar kommer också att krympa i storlek med en faktor 4.
// Ändringen i formens "BoundsInPoints"-egenskap kommer att återspegla detta.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Infoga en form och placera den utanför gränserna för gruppformens innehållsblock.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Gruppformens fotavtryck i dokumentkroppen har ökat, men innehållsblocket förblir detsamma.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
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
