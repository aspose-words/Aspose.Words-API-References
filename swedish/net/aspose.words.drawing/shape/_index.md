---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.Shape klass. Representerar ett objekt i ritskiktet till exempel en AutoShape textbox freeform OLEobjekt ActiveXkontroll eller bild i C#.
type: docs
weight: 1250
url: /sv/net/aspose.words.drawing/shape/
---
## Shape class

Representerar ett objekt i ritskiktet, till exempel en AutoShape, textbox, freeform, OLE-objekt, ActiveX-kontroll eller bild.

För att lära dig mer, besök[Arbeta med former](https://docs.aspose.com/words/net/working-with-shapes/) dokumentationsartikel.

```csharp
public sealed class Shape : ShapeBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | Skapar ett nytt formobjekt. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Hämtar eller ställer in ett värde som anger om denna form kan överlappa andra former. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Definierar alternativ text som ska visas istället för en grafik. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Anger om formens ankare är låst. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Anger om formens bildförhållande är låst. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Anger om formen är under eller över text. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Hämtar positionen för den nedre kanten av det innehållande blocket av formen. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Hämtar eller ställer in platsen och storleken på formens innehållsblock. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Hämtar platsen och storleken på formens innehållande block i punkter, i förhållande till ankaret för den översta formen. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Får den slutliga omfattningen som detta formobjekt har efter applicering av ritningseffekter. Värdet mäts i punkter. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Returnerar`Sann` om formtypen tillåter att formen har en bild. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Ger tillgång till diagramegenskaperna om denna form har en[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Koordinaterna i det övre vänstra hörnet av det innehållande blocket med denna form. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Bredden och höjden på koordinatutrymmet inuti det innehållande blocket med denna form. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Returnerar eller ställer in avståndet (i punkter) mellan dokumenttexten och den nedre kanten av formen. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Returnerar eller ställer in avståndet (i punkter) mellan dokumenttexten och den vänstra kanten av formen. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Returnerar eller ställer in avståndet (i punkter) mellan dokumenttexten och den högra kanten av formen. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Returnerar eller ställer in avståndet (i punkter) mellan dokumenttexten och formens övre kant. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Returnerar`Sann` om en extruderingseffekt är aktiverad. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Får fyllningsformatering för formen. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Definierar penselfärgen som fyller den stängda banan för formen. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Bestämmer om den stängda vägen för formen kommer att fyllas. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Får första stycket i formen. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Ändrar orienteringen för en form. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Ger tillgång till teckensnittsformateringen för detta objekt. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Returnerar`Sann` om det här`Shape` har en[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar`Sann` om denna nod har några undernoder. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Returnerar`Sann` om formen har bildbytes eller länkar en bild. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Returnerar`Sann` om det här`Shape` har ett SmartArt-objekt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Hämtar eller ställer in höjden på formens innehållsblock. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Hämtar eller ställer in värdet som representerar procentandelen av formens relativa höjd. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Anger hur formen placeras horisontellt. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Ger tillgång till egenskaperna för den horisontella regelformen. För en form som inte är en horisontell regel, returnerar`null` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Hämtar eller ställer in den fullständiga hyperlänkadressen för en form. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Ger tillgång till bilden av formen. Returnerar`null` om formen inte kan ha en bild. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar`Sann` eftersom denna nod kan ha underordnade noder. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Hämtar eller ställer in flaggan som anger om formen är dekorativ i dokumentet. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Returnerar sant om detta objekt raderades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Returnerar`Sann` om detta är en gruppform. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Returnerar`Sann` om denna form är en horisontell regel. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Returnerar`Sann` om denna form är en bildform. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Ett snabbt sätt att avgöra om denna form är placerad i linje med text. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Hämtar eller sätter en flagga som indikerar om formen visas inuti en tabell eller utanför den. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Returnerar`Sann` om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Returnerar`Sann` om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indikerar att formen är en[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Returnerar`Sann`om denna form inte är ett underordnat till en gruppform. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Returnerar`Sann` om den här formen är ett WordArt-objekt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Får det sista stycket i formen. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Hämtar eller ställer in positionen för den vänstra kanten av formens innehållsblock. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Hämtar eller ställer in värdet som representerar formens relativa vänstra position i procent. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Får MarkupLanguage som används för detta grafiska objekt. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Hämtar eller ställer in det valfria formnamnet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | ReturnerarShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Ger tillgång till OLE-data för en form. För en form som inte är ett OLE-objekt eller ActiveX-kontroll, returneras`null` . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Returnerar det omedelbara överordnade stycket. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Anger i förhållande till vad formen är placerad horisontellt. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Hämtar eller ställer in värdet på formens relativa storlek i horisontell riktning. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Anger i förhållande till vad formen är placerad vertikalt. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Hämtar eller ställer in värdet på formens relativa storlek i vertikal riktning. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Får positionen för den högra kanten av det innehållande blocket av formen. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Definierar vinkeln (i grader) som en form roteras. Positivt värde motsvarar medurs rotationsvinkel. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Definierar texten som visas när muspekaren rör sig över formen. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Returnerar`Sann` om en skuggeffekt är aktiverad. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Får skuggformatering för formen. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Hämtar formtypen. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Blir[`SignatureLine`](../signatureline/) objekt om formen är en signaturlinje. Returnerar`null` annars. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Får formens storlek i poäng. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | ReturnerarTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Definierar ett streck för en form. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Definierar färgen på ett streck. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Definierar om sökvägen ska streckas. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Definierar penseltjockleken som sträcker banan för en form i punkter. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Hämtar eller ställer in målramen för formhyperlänken. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Definierar attribut som anger hur text visas i en form. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Definierar texten för textsökvägen (för ett WordArt-objekt). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Hämtar eller ställer in titeln (bildtexten) för det aktuella formobjektet. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Hämtar eller ställer in positionen för den övre kanten av formens innehållsblock. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Hämtar eller ställer in värdet som representerar formens relativa topposition i procent. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Anger hur formen är placerad vertikalt. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Hämtar eller ställer in bredden på formens innehållsblock. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Hämtar eller ställer in värdet som representerar procentandelen av formens relativa bredd. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Anger hur texten lindas runt formen. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Definierar om formen är inline eller flytande. För flytande former definierar lindningsläget för text runt formen. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Bestämmer visningsordningen för överlappande former. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Lägger till källrektangelvärdena för effektomfattningen och returnerar den sista rektangeln. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar navigator som kan användas för att korsa och läsa noder. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(*int*) | Reserverad för systemanvändning. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(*int*) | Reserverad för systemanvändning. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(*int*) | Reserverad för systemanvändning. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Skapar och returnerar ett objekt som kan användas för att återge denna form till en bild. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Konverterar ett värde från det lokala koordinatutrymmet till koordinatutrymmet för den överordnade formen. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Tar bort den angivna underordnade noden. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | Reserverad för systemanvändning. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/)underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../../aspose.words/node/) som matchar XPath-uttrycket. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | Reserverad för systemanvändning. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Uppdaterar SmartArt förrenderad ritning genom att använda Aspose.Words SmartArt kall renderingsmotor. |

## Anmärkningar

Använda`Shape` klass kan du skapa eller ändra former i ett Microsoft Word-dokument.

En viktig egenskap hos en form är dess[`ShapeType`](../shapebase/shapetype/)Former av olika -typer kan ha olika möjligheter i ett Word-dokument. Till exempel kan endast bild och OLE shapes ha bilder inuti dem. De flesta formerna kan ha text, men inte alla.

Former som kan ha text, kan innehålla[`Paragraph`](../../aspose.words/paragraph/) och [`Table`](../../aspose.words.tables/table/) noder som barn.

## Exempel

Visar hur man infogar en flytande bild i mitten av en sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en flytande bild som kommer att visas bakom den överlappande texten och justera den mot sidans mitt.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Visar hur man extraherar bilder från ett dokument och sparar dem i det lokala filsystemet som enskilda filer.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Hämta samlingen av former från dokumentet,
// och spara bilddata för varje form med en bild som en fil till det lokala filsystemet.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Bilddata för former kan innehålla bilder av många möjliga bildformat.
        // Vi kan bestämma en filtillägg för varje bild automatiskt, baserat på dess format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Visar hur man tar bort alla former från ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga två former tillsammans med en gruppform med en annan form inuti.
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// Ta bort alla Shape-noder från dokumentet.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Alla former är borta, men gruppformen finns kvar i dokumentet.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Ta bort alla gruppformer separat.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Se även

* class [ShapeBase](../shapebase/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
