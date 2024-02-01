---
title: ShapeType Enum
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ShapeType enum. Specifies the type of shape in a Microsoft Word document in C#.
type: docs
weight: 1390
url: /net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Specifies the type of shape in a Microsoft Word document.

```csharp
public enum ShapeType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Image | `75` | The shape is an image. |
| TextBox | `202` | The shape is a textbox. Note that shapes of many other types can also have text inside them too. A shape does not have to have this type to contain text. |
| Group | `-1` | The shape is a group shape. |
| OleObject | `-2` | The shape is an OLE object. |
| OleControl | `201` | The shape is an ActiveX control. |
| NonPrimitive | `0` | A shape drawn by user and consisting of multiple segments and/or vertices (curve, freeform or scribble). |
| Rectangle | `1` | Rectangle. |
| RoundRectangle | `2` | Round rectangle. |
| Ellipse | `3` | Ellipse. |
| Diamond | `4` | Diamond. |
| Triangle | `5` | Triangle. |
| RightTriangle | `6` | Right triangle. |
| Parallelogram | `7` | Parallelogram. |
| Trapezoid | `8` | Trapezoid. |
| Hexagon | `9` | Hexagon. |
| Octagon | `10` | Octagon. |
| Plus | `11` | Plus. |
| Star | `12` | Star. |
| Arrow | `13` | Arrow. |
| ThickArrow | `14` | Thick arrow. |
| HomePlate | `15` | Home plate. |
| Cube | `16` | Cube. |
| Balloon | `17` | Balloon. |
| Seal | `18` | Seal. |
| Arc | `19` | Arc. |
| Line | `20` | Line. |
| Plaque | `21` | Plaque. |
| Can | `22` | Can. |
| Donut | `23` | Donut. |
| TextSimple | `24` | Text simple. |
| TextOctagon | `25` | Text octagon. |
| TextHexagon | `26` | Text hexagon. |
| TextCurve | `27` | Text curve. |
| TextWave | `28` | Text wave. |
| TextRing | `29` | Text ring. |
| TextOnCurve | `30` | Text on curve. |
| TextOnRing | `31` | Text on ring. |
| StraightConnector1 | `32` | A straight connector shape. |
| BentConnector2 | `33` | A bent connector shape with two segments. |
| BentConnector3 | `34` | A bent connector shape with three segments. |
| BentConnector4 | `35` | A bent connector shape with four segments. |
| BentConnector5 | `36` | A bent connector shape with five segments. |
| CurvedConnector2 | `37` | A curved connector shape with two segments. |
| CurvedConnector3 | `38` | A curved connector shape with three segments. |
| CurvedConnector4 | `39` | A curved connector shape with four segments. |
| CurvedConnector5 | `40` | A curved connector shape with five segments. |
| Callout1 | `41` | A callout shape with one arrow. |
| Callout2 | `42` | A callout shape with two arrows. |
| Callout3 | `43` | A callout shape with three arrows. |
| AccentCallout1 | `44` | An accent callout shape with one arrow. |
| AccentCallout2 | `45` | An accent callout shape with two arrows. |
| AccentCallout3 | `46` | An accent callout shape with three arrows. |
| BorderCallout1 | `47` | Border callout 1. |
| BorderCallout2 | `48` | Border callout 2. |
| BorderCallout3 | `49` | Border callout 3. |
| AccentBorderCallout1 | `50` | Accent border callout 1. |
| AccentBorderCallout2 | `51` | Accent border callout 2. |
| AccentBorderCallout3 | `52` | Accent border callout 3. |
| Ribbon | `53` | Ribbon. |
| Ribbon2 | `54` | Ribbon 2. |
| Chevron | `55` | Chevron. |
| Pentagon | `56` | Pentagon. |
| NoSmoking | `57` | NoSmoking. |
| Seal8 | `58` | Eight-pointed star. |
| Seal16 | `59` | 16-pointed star. |
| Seal32 | `60` | 32-pointed star. |
| WedgeRectCallout | `61` | Wedge rect callout. |
| WedgeRRectCallout | `62` | Wedge R rect callout. |
| WedgeEllipseCallout | `63` | Wedge ellipse callout. |
| Wave | `64` | Wave. |
| FoldedCorner | `65` | Folded corner. |
| LeftArrow | `66` | Left arrow. |
| DownArrow | `67` | Down arrow. |
| UpArrow | `68` | Up arrow. |
| LeftRightArrow | `69` | Left right arrow. |
| UpDownArrow | `70` | Up down arrow. |
| IrregularSeal1 | `71` | Irregular seal 1. |
| IrregularSeal2 | `72` | Irregular seal 2. |
| LightningBolt | `73` | Lightning bolt. |
| Heart | `74` | Heart. |
| QuadArrow | `76` | Quad arrow. |
| LeftArrowCallout | `77` | Left arrow callout. |
| RightArrowCallout | `78` | Right arrow callout |
| UpArrowCallout | `79` | Up arrow callout. |
| DownArrowCallout | `80` | Down arrow callout. |
| LeftRightArrowCallout | `81` | Left right arrow callout. |
| UpDownArrowCallout | `82` | Up down arrow callout. |
| QuadArrowCallout | `83` | Quad arrow callout. |
| Bevel | `84` | Bevel. |
| LeftBracket | `85` | Left bracket. |
| RightBracket | `86` | Right bracket. |
| LeftBrace | `87` | Left brace. |
| RightBrace | `88` | Right brace. |
| LeftUpArrow | `89` | Left up arrow. |
| BentUpArrow | `90` | Bent up arrow. |
| BentArrow | `91` | Bent arrow. |
| Seal24 | `92` | 24-pointed star. |
| StripedRightArrow | `93` | Striped right arrow. |
| NotchedRightArrow | `94` | Notched right arrow. |
| BlockArc | `95` | Block arc. |
| SmileyFace | `96` | Smiley face. |
| VerticalScroll | `97` | Vertical scroll. |
| HorizontalScroll | `98` | Horizontal scroll. |
| CircularArrow | `99` | Circular arrow. |
| CustomShape | `100` | This shape type seems to be set for shapes that are not part of the standard set of the auto shapes in Microsoft Word. For example, if you insert a new auto shape from ClipArt. |
| UturnArrow | `101` | Uturn arrow. |
| CurvedRightArrow | `102` | Curved right arrow. |
| CurvedLeftArrow | `103` | Curved left arrow. |
| CurvedUpArrow | `104` | Curved up arrow |
| CurvedDownArrow | `105` | Curved down arrow. |
| CloudCallout | `106` | Cloud callout. |
| EllipseRibbon | `107` | Ellipse ribbon. |
| EllipseRibbon2 | `108` | Ellipse ribbon 2. |
| FlowChartProcess | `109` | Flow chart process. |
| FlowChartDecision | `110` | Flow chart decision. |
| FlowChartInputOutput | `111` | Flow chart input output. |
| FlowChartPredefinedProcess | `112` | Flow chart predefined process |
| FlowChartInternalStorage | `113` | Flow chart internal storage. |
| FlowChartDocument | `114` | Flow chart document. |
| FlowChartMultidocument | `115` | Flow chart multi document. |
| FlowChartTerminator | `116` | Flow chart terminator. |
| FlowChartPreparation | `117` | Flow chart preparation. |
| FlowChartManualInput | `118` | Flow chart manual input. |
| FlowChartManualOperation | `119` | Flow chart manual operation. |
| FlowChartConnector | `120` | Flow chart connector. |
| FlowChartPunchedCard | `121` | Flow chart punched card. |
| FlowChartPunchedTape | `122` | Flow chart punched tape. |
| FlowChartSummingJunction | `123` | Flow chart summing junction. |
| FlowChartOr | `124` | Flow chart or. |
| FlowChartCollate | `125` | Flow chart collate. |
| FlowChartSort | `126` | Flow chart sort. |
| FlowChartExtract | `127` | Flow chart extract. |
| FlowChartMerge | `128` | Flow chart merge. |
| FlowChartOfflineStorage | `129` | Flow chart off-line storage. |
| FlowChartOnlineStorage | `130` | Flow chart on-line storage. |
| FlowChartMagneticTape | `131` | Flow char magnetic tape. |
| FlowChartMagneticDisk | `132` | Flow chart magnetic disk. |
| FlowChartMagneticDrum | `133` | Flow chart magnetic drum. |
| FlowChartDisplay | `134` | Flow chart display. |
| FlowChartDelay | `135` | Flow chart delay. |
| TextPlainText | `136` | Plain-text, WordArt object. |
| TextStop | `137` | Stop, WordArt object. |
| TextTriangle | `138` | Triangle, WordArt object. |
| TextTriangleInverted | `139` | Triangle inverted, WordArt object. |
| TextChevron | `140` | Chevron, WordArt object. |
| TextChevronInverted | `141` | Chevron inverted, WordArt object. |
| TextRingInside | `142` | Ring inside, WordArt object. |
| TextRingOutside | `143` | Ring outside, WordArt object. |
| TextArchUpCurve | `144` | Arch up curve, WordArt object. |
| TextArchDownCurve | `145` | Arch down curve, WordArt object. |
| TextCircleCurve | `146` | Circle curve, WordArt object. |
| TextButtonCurve | `147` | Button curve, WordArt object. |
| TextArchUpPour | `148` | Arch up pour, WordArt object. |
| TextArchDownPour | `149` | Arch down pour, WordArt object. |
| TextCirclePour | `150` | Circle pour, WordArt object. |
| TextButtonPour | `151` | Button pour, WordArt object. |
| TextCurveUp | `152` | Curve up, WordArt object. |
| TextCurveDown | `153` | Curve down, WordArt object. |
| TextCascadeUp | `154` | Cascade up, WordArt object. |
| TextCascadeDown | `155` | Cascade down, WordArt object. |
| TextWave1 | `156` | Wave 1, WordArt object. |
| TextWave2 | `157` | Wave 2, WordArt object. |
| TextWave3 | `158` | Wave 3, WordArt object. |
| TextWave4 | `159` | Wave 4, WordArt object. |
| TextInflate | `160` | Inflate, WordArt object. |
| TextDeflate | `161` | Deflate, WordArt object. |
| TextInflateBottom | `162` | Inflate bottom, WordArt object. |
| TextDeflateBottom | `163` | Deflate bottom, WordArt object. |
| TextInflateTop | `164` | Inflate top, WordArt object. |
| TextDeflateTop | `165` | Deflate top, WordArt object. |
| TextDeflateInflate | `166` | Deflate inflate, WordArt object. |
| TextDeflateInflateDeflate | `167` | Deflate inflate deflate, WordArt object. |
| TextFadeRight | `168` | Fade right, WordArt object. |
| TextFadeLeft | `169` | Fade left, WordArt object. |
| TextFadeUp | `170` | Fade up, WordArt object. |
| TextFadeDown | `171` | Fade down, WordArt object. |
| TextSlantUp | `172` | Slant up, WordArt object. |
| TextSlantDown | `173` | Slant down, WordArt object. |
| TextCanUp | `174` | Can up, WordArt object. |
| TextCanDown | `175` | Can down, WordArt object. |
| FlowChartAlternateProcess | `176` | Flow chart alternate process. |
| FlowChartOffpageConnector | `177` | Flow chart off page connector. |
| Callout90 | `178` | Callout 90. |
| AccentCallout90 | `179` | Accent callout 90. |
| BorderCallout90 | `180` | Border callout 90. |
| AccentBorderCallout90 | `181` | Accent border callout 90. |
| LeftRightUpArrow | `182` | Left right up arrow. |
| Sun | `183` | Sun. |
| Moon | `184` | Moon. |
| BracketPair | `185` | Bracket pair. |
| BracePair | `186` | Brace pair |
| Seal4 | `187` | Four-pointed star. |
| DoubleWave | `188` | Double wave. |
| ActionButtonBlank | `189` | Action button blank. |
| ActionButtonHome | `190` | Action button home. |
| ActionButtonHelp | `191` | Action button help. |
| ActionButtonInformation | `192` | Action button information. |
| ActionButtonForwardNext | `193` | Action button forward next. |
| ActionButtonBackPrevious | `194` | Action button back previous. |
| ActionButtonEnd | `195` | Action button end. |
| ActionButtonBeginning | `196` | Action button beginning. |
| ActionButtonReturn | `197` | Action button return. |
| ActionButtonDocument | `198` | Action button document. |
| ActionButtonSound | `199` | Action button sound. |
| ActionButtonMovie | `200` | Action button movie. |
| SingleCornerSnipped | `203` | Snip single corner rectangle object. |
| TopCornersSnipped | `204` | Snip same side corner rectangle. |
| DiagonalCornersSnipped | `205` | Snip diagonal corner rectangle. |
| TopCornersOneRoundedOneSnipped | `206` | Snip and round single corner rectangle. |
| SingleCornerRounded | `207` | Round single corner rectangle. |
| TopCornersRounded | `208` | Round same side corner rectangle. |
| DiagonalCornersRounded | `209` | Round diagonal corner rectangle. |
| Heptagon | `210` | Heptagon. |
| Cloud | `211` | Cloud. |
| Seal6 | `212` | Six-pointed star. |
| Seal7 | `213` | Seven-pointed star. |
| Seal10 | `214` | Ten-pointed star. |
| Seal12 | `215` | Twelve-pointed star. |
| SwooshArrow | `216` | Swoosh arrow. |
| Teardrop | `217` | Teardrop. |
| SquareTabs | `218` | Square tabs. |
| PlaqueTabs | `219` | Plaque tabs. |
| Pie | `220` | Pie. |
| WedgePie | `221` | Wedge pie. |
| InverseLine | `222` | Inverse line. |
| MathPlus | `223` | Math plus. |
| MathMinus | `224` | Math minus. |
| MathMultiply | `225` | Math multiply. |
| MathDivide | `226` | Math divide. |
| MathEqual | `227` | Math equal. |
| MathNotEqual | `228` | Math not equal. |
| NonIsoscelesTrapezoid | `229` | Non-isosceles trapezoid. |
| LeftRightCircularArrow | `230` | Left-right circular arrow. |
| LeftRightRibbon | `231` | Left-right ribbon. |
| LeftCircularArrow | `232` | Left circular arrow. |
| Frame | `233` | Frame. |
| HalfFrame | `234` | Half frame. |
| Funnel | `235` | Funnel. |
| Gear6 | `236` | Six-tooth gear. |
| Gear9 | `237` | Nine-tooth gear. |
| Decagon | `238` | Decagon. |
| Dodecagon | `239` | Dodecagon. |
| DiagonalStripe | `240` | Diagonal stripe. |
| Corner | `241` | Corner. |
| CornerTabs | `242` | Corner tabs. |
| Chord | `243` | Chord. |
| ChartPlus | `244` | Chart plus. |
| ChartStar | `245` | Chart star. |
| ChartX | `246` | Chart X. |
| MinValue | `-2` | Reserved for the system use. |

## Examples

Shows how to insert a shape with an image from the local file system into a document.

```csharp
Document doc = new Document();

// The "Shape" class's public constructor will create a shape with "ShapeMarkupLanguage.Vml" markup type.
// If you need to create a shape of a non-primitive type, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// please use DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Shows how Aspose.Words identify shapes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// To correct identify shape types you need to work with shapes as DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // "Strict" or "Transitional" compliance allows to save shape as DML.
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

doc.Save(ArtifactsDir + "Shape.ShapeTypes.docx", saveOptions);
doc = new Document(ArtifactsDir + "Shape.ShapeTypes.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

foreach (Shape shape in shapes)
{
    Console.WriteLine(shape.ShapeType);
}
```

### See Also

* property [ShapeType](../shapebase/shapetype/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
