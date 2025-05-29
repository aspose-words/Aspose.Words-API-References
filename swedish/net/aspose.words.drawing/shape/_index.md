---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Shape för att enkelt skapa mångsidiga ritobjekt som autoformer, textrutor och bilder i dina projekt.
type: docs
weight: 1640
url: /sv/net/aspose.words.drawing/shape/
---
## Shape class

Representerar ett objekt i ritlagret, till exempel en autofigur, textruta, frihandsformat, OLE-objekt, ActiveX-kontroll eller bild.

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
| [Adjustments](../../aspose.words.drawing/shape/adjustments/) { get; } | Ger åtkomst till justeringsrådvärdena för en form. För en form som inte innehåller några justeringsrådvärden returnerar den en tom samling. |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Hämtar eller anger ett värde som anger om denna form kan överlappa andra former. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Definierar alternativ text som ska visas istället för grafik. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Anger om formens ankare är låst. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Anger om formens bildförhållande är låst. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Anger om formen är under eller ovanför texten. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Hämtar positionen för den nedre kanten av det block som innehåller formen. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Hämtar eller anger plats och storlek för det block som innehåller formen. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Hämtar platsen och storleken på det block som innehåller formen i punkter, i förhållande till ankaret för den översta formen. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Hämtar den slutliga utsträckningen som detta formobjekt har efter att riteffekter har tillämpats. Värdet mäts i punkter. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Returer`sann` om formtypen tillåter att formen har en bild. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Ger åtkomst till diagrammets egenskaper om den här formen har en[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Koordinaterna i det övre vänstra hörnet av det block som innehåller den här formen. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Bredden och höjden på koordinatutrymmet inuti det block som innehåller den här formen. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens nedre kant. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens vänstra kant. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens högra kant. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens övre kant. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Returer`sann` om en extruderingseffekt är aktiverad. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Hämtar fyllningsformatering för formen. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Definierar penselfärgen som fyller formens slutna bana. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Avgör om den stängda banan för formen ska fyllas. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Hämtar det första stycket i formen. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Växlar orienteringen på en form. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Ger åtkomst till teckensnittsformateringen för detta objekt. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Hämtar glödformatering för formen. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Returer`sann` om detta`Shape` har en[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Returer`sann` om formen har bildbyte eller länkar en bild. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Returer`sann` om detta`Shape` har ett SmartArt-objekt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Hämtar eller ställer in höjden på det block som innehåller formen. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Hämtar eller ställer in värdet som representerar procentandelen av formens relativa höjd. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om formen är synlig. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Anger hur formen placeras horisontellt. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Ger åtkomst till egenskaperna för den horisontella regelformen. För en form som inte är en horisontell regel returneras`null` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Hämtar eller anger den fullständiga hyperlänkadressen för en form. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Ger åtkomst till bilden av formen. Returnerar`null` om formen inte kan ha en bild. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Hämtar eller ställer in flaggan som anger om formen är dekorativ i dokumentet. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Returnerar sant om det här objektet togs bort i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Returer`sann` om detta är en gruppform. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Returer`sann` om denna form är en horisontell linje. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Returer`sann` om den här formen är en bildform. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Ett snabbt sätt att avgöra om den här formen är placerad i linje med texten. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Hämtar eller anger en flagga som anger om formen visas inuti en tabell eller utanför den. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Returer`sann` om det här objektet flyttades (raderades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Returer`sann` om det här objektet flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indikerar att formen är en[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Returer`sann` om den här formen inte är underordnad en gruppform. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Returer`sann` om den här formen är ett WordArt-objekt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Hämtar det sista stycket i formen. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Hämtar eller anger positionen för den vänstra kanten av det block som formen innehåller. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Hämtar eller ställer in värdet som representerar formens relativa vänstra position i procent. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Hämtar MarkupLanguage som används för detta grafikobjekt. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Hämtar eller anger det valfria formnamnet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | ReturerShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Ger åtkomst till OLE-data för en form. För en form som inte är ett OLE-objekt eller en ActiveX-kontroll returneras`null` . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Returnerar det omedelbara överordnade stycket. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | Hämtar reflektionsformatering för formen. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Anger i förhållande till vad formen är placerad horisontellt. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Hämtar eller ställer in värdet för formens relativa storlek i horisontell riktning. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Anger i förhållande till vad formen är placerad vertikalt. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Hämtar eller ställer in värdet för formens relativa storlek i vertikal riktning. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Hämtar positionen för den högra kanten av det block som innehåller formen. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Definierar vinkeln (i grader) som en form roteras med. Positivt värde motsvarar medurs rotationsvinkel. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Definierar texten som visas när muspekaren flyttas över formen. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Returer`sann` om en skuggeffekt är aktiverad. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Hämtar skuggformatering för formen. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Hämtar formtypen. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Får[`SignatureLine`](../signatureline/) objekt om formen är en signaturrad. Returnerar`null` annars. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Hämtar formens storlek i punkter. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | Hämtar mjuka kanter för formen. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | ReturerTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Definierar ett streck för en form. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Definierar färgen på ett streck. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Definierar om banan ska vara linjerad. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Definierar penselns tjocklek som stryker längs en forms bana i punkter. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Hämtar eller ställer in målramen för formens hyperlänk. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Definierar attribut som anger hur text visas i en form. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Definierar texten i textbanan (för ett WordArt-objekt). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Hämtar eller anger titeln (bildtexten) för det aktuella formobjektet. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Hämtar eller anger positionen för den övre kanten av det block som formen innehåller. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Hämtar eller ställer in värdet som representerar formens relativa toppposition i procent. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Anger hur formen placeras vertikalt. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Hämtar eller ställer in bredden på det block som innehåller formen. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Hämtar eller ställer in värdet som representerar procentandelen av formens relativa bredd. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Anger hur texten radbryts runt formen. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Definierar om formen är inbäddad eller flytande. För flytande former definieras radbrytningsläget för text runt formen. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Bestämmer visningsordningen för överlappande former. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words.drawing/shape/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka slutet av formen. |
| override [AcceptStart](../../aspose.words.drawing/shape/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka början av formen. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Lägger till värdena för effektens omfattning i källrektangeln och returnerar den slutliga rektangeln. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Skapar och returnerar ett objekt som kan användas för att rendera denna form till en bild. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Konverterar ett värde från det lokala koordinatrummet till koordinatrummet för den överordnade formen. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../../aspose.words/node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Uppdaterar SmartArt-förrenderade teckningar med hjälp av Aspose.Words SmartArt-kallrenderingsmotor. |

## Anmärkningar

Använda`Shape` I klassen kan du skapa eller ändra former i ett Microsoft Word-dokument.

En viktig egenskap hos en form är dess[`ShapeType`](../shapebase/shapetype/)Former av olika typer av kan ha olika funktioner i ett Word-dokument. Till exempel kan endast bild- och OLE-former innehålla bilder. De flesta former kan innehålla text, men inte alla.

Former som kan ha text, kan innehålla[`Paragraph`](../../aspose.words/paragraph/) och [`Table`](../../aspose.words.tables/table/) noder som barn.

## Exempel

Visar hur man infogar en flytande bild i mitten av en sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den mot sidans mitt.
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
         // Bilddata för former kan innehålla bilder i många möjliga bildformat.
        // Vi kan automatiskt bestämma filändelsen för varje bild, baserat på dess format.
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

// Ta bort alla formnoder från dokumentet.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Alla former är borta, men gruppformen finns fortfarande kvar i dokumentet.
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
