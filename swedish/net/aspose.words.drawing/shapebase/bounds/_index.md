---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase Bounds för att enkelt hantera din forms placering och storlek, vilket förbättrar din designprecision och effektivitet.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Hämtar eller anger plats och storlek för det block som innehåller formen.

```csharp
public RectangleF Bounds { get; set; }
```

## Anmärkningar

Ignorerar lås för bildförhållande vid inställning.

För en form på översta nivån är värdet i punkter och relativt till formankaret.

För former i en grupp finns värdet i koordinatrummet och enheterna för den överordnade gruppen.

## Exempel

Visar hur man verifierar former som innehåller blockgränser.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Även om själva raden tar upp lite plats på dokumentsidan,
// den upptar ett rektangulärt innehållande block, vars storlek vi kan bestämma med hjälp av egenskaperna "Bounds".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Skapa en gruppform och ange sedan storleken på dess block med hjälp av egenskapen "Bounds".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Skapa en rektangel, verifiera storleken på dess avgränsande block och lägg sedan till den i gruppformen.
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
// Vår gruppform är 250x250pt stor, så var 4:e pt på gruppformens koordinatplan
// översätts till 1pt i dokumentets koordinatplan.
// Varje form som vi infogar kommer också att krympa i storlek med en faktor 4.
// Ändringen i formens egenskap "BoundsInPoints" kommer att återspegla detta.
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

// Gruppformens yta i dokumentets innehåll har ökat, men det innehållande blocket förblir detsamma.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
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
