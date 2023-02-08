---
title: Enum ShapeType
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.ShapeType enum. Specifies the type of shape in a Microsoft Word document in C#
type: docs
weight: 1140
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
| Rectangle | `1` |  |
| RoundRectangle | `2` |  |
| Ellipse | `3` |  |
| Diamond | `4` |  |
| Triangle | `5` |  |
| RightTriangle | `6` |  |
| Parallelogram | `7` |  |
| Trapezoid | `8` |  |
| Hexagon | `9` |  |
| Octagon | `10` |  |
| Plus | `11` |  |
| Star | `12` |  |
| Arrow | `13` |  |
| ThickArrow | `14` |  |
| HomePlate | `15` |  |
| Cube | `16` |  |
| Balloon | `17` |  |
| Seal | `18` |  |
| Arc | `19` |  |
| Line | `20` |  |
| Plaque | `21` |  |
| Can | `22` |  |
| Donut | `23` |  |
| TextSimple | `24` |  |
| TextOctagon | `25` |  |
| TextHexagon | `26` |  |
| TextCurve | `27` |  |
| TextWave | `28` |  |
| TextRing | `29` |  |
| TextOnCurve | `30` |  |
| TextOnRing | `31` |  |
| StraightConnector1 | `32` |  |
| BentConnector2 | `33` |  |
| BentConnector3 | `34` |  |
| BentConnector4 | `35` |  |
| BentConnector5 | `36` |  |
| CurvedConnector2 | `37` |  |
| CurvedConnector3 | `38` |  |
| CurvedConnector4 | `39` |  |
| CurvedConnector5 | `40` |  |
| Callout1 | `41` |  |
| Callout2 | `42` |  |
| Callout3 | `43` |  |
| AccentCallout1 | `44` |  |
| AccentCallout2 | `45` |  |
| AccentCallout3 | `46` |  |
| BorderCallout1 | `47` |  |
| BorderCallout2 | `48` |  |
| BorderCallout3 | `49` |  |
| AccentBorderCallout1 | `50` |  |
| AccentBorderCallout2 | `51` |  |
| AccentBorderCallout3 | `52` |  |
| Ribbon | `53` |  |
| Ribbon2 | `54` |  |
| Chevron | `55` |  |
| Pentagon | `56` |  |
| NoSmoking | `57` |  |
| Seal8 | `58` |  |
| Seal16 | `59` |  |
| Seal32 | `60` |  |
| WedgeRectCallout | `61` |  |
| WedgeRRectCallout | `62` |  |
| WedgeEllipseCallout | `63` |  |
| Wave | `64` |  |
| FoldedCorner | `65` |  |
| LeftArrow | `66` |  |
| DownArrow | `67` |  |
| UpArrow | `68` |  |
| LeftRightArrow | `69` |  |
| UpDownArrow | `70` |  |
| IrregularSeal1 | `71` |  |
| IrregularSeal2 | `72` |  |
| LightningBolt | `73` |  |
| Heart | `74` |  |
| QuadArrow | `76` |  |
| LeftArrowCallout | `77` |  |
| RightArrowCallout | `78` |  |
| UpArrowCallout | `79` |  |
| DownArrowCallout | `80` |  |
| LeftRightArrowCallout | `81` |  |
| UpDownArrowCallout | `82` |  |
| QuadArrowCallout | `83` |  |
| Bevel | `84` |  |
| LeftBracket | `85` |  |
| RightBracket | `86` |  |
| LeftBrace | `87` |  |
| RightBrace | `88` |  |
| LeftUpArrow | `89` |  |
| BentUpArrow | `90` |  |
| BentArrow | `91` |  |
| Seal24 | `92` |  |
| StripedRightArrow | `93` |  |
| NotchedRightArrow | `94` |  |
| BlockArc | `95` |  |
| SmileyFace | `96` |  |
| VerticalScroll | `97` |  |
| HorizontalScroll | `98` |  |
| CircularArrow | `99` |  |
| CustomShape | `100` | This shape type seems to be set for shapes that are not part of the standard set of the auto shapes in Microsoft Word. For example, if you insert a new auto shape from ClipArt. |
| UturnArrow | `101` |  |
| CurvedRightArrow | `102` |  |
| CurvedLeftArrow | `103` |  |
| CurvedUpArrow | `104` |  |
| CurvedDownArrow | `105` |  |
| CloudCallout | `106` |  |
| EllipseRibbon | `107` |  |
| EllipseRibbon2 | `108` |  |
| FlowChartProcess | `109` |  |
| FlowChartDecision | `110` |  |
| FlowChartInputOutput | `111` |  |
| FlowChartPredefinedProcess | `112` |  |
| FlowChartInternalStorage | `113` |  |
| FlowChartDocument | `114` |  |
| FlowChartMultidocument | `115` |  |
| FlowChartTerminator | `116` |  |
| FlowChartPreparation | `117` |  |
| FlowChartManualInput | `118` |  |
| FlowChartManualOperation | `119` |  |
| FlowChartConnector | `120` |  |
| FlowChartPunchedCard | `121` |  |
| FlowChartPunchedTape | `122` |  |
| FlowChartSummingJunction | `123` |  |
| FlowChartOr | `124` |  |
| FlowChartCollate | `125` |  |
| FlowChartSort | `126` |  |
| FlowChartExtract | `127` |  |
| FlowChartMerge | `128` |  |
| FlowChartOfflineStorage | `129` |  |
| FlowChartOnlineStorage | `130` |  |
| FlowChartMagneticTape | `131` |  |
| FlowChartMagneticDisk | `132` |  |
| FlowChartMagneticDrum | `133` |  |
| FlowChartDisplay | `134` |  |
| FlowChartDelay | `135` |  |
| TextPlainText | `136` | WordArt object. |
| TextStop | `137` | WordArt object. |
| TextTriangle | `138` | WordArt object. |
| TextTriangleInverted | `139` | WordArt object. |
| TextChevron | `140` | WordArt object. |
| TextChevronInverted | `141` | WordArt object. |
| TextRingInside | `142` | WordArt object. |
| TextRingOutside | `143` | WordArt object. |
| TextArchUpCurve | `144` | WordArt object. |
| TextArchDownCurve | `145` | WordArt object. |
| TextCircleCurve | `146` | WordArt object. |
| TextButtonCurve | `147` | WordArt object. |
| TextArchUpPour | `148` | WordArt object. |
| TextArchDownPour | `149` | WordArt object. |
| TextCirclePour | `150` | WordArt object. |
| TextButtonPour | `151` | WordArt object. |
| TextCurveUp | `152` | WordArt object. |
| TextCurveDown | `153` | WordArt object. |
| TextCascadeUp | `154` | WordArt object. |
| TextCascadeDown | `155` | WordArt object. |
| TextWave1 | `156` | WordArt object. |
| TextWave2 | `157` | WordArt object. |
| TextWave3 | `158` | WordArt object. |
| TextWave4 | `159` | WordArt object. |
| TextInflate | `160` | WordArt object. |
| TextDeflate | `161` | WordArt object. |
| TextInflateBottom | `162` | WordArt object. |
| TextDeflateBottom | `163` | WordArt object. |
| TextInflateTop | `164` | WordArt object. |
| TextDeflateTop | `165` | WordArt object. |
| TextDeflateInflate | `166` | WordArt object. |
| TextDeflateInflateDeflate | `167` | WordArt object. |
| TextFadeRight | `168` | WordArt object. |
| TextFadeLeft | `169` | WordArt object. |
| TextFadeUp | `170` | WordArt object. |
| TextFadeDown | `171` | WordArt object. |
| TextSlantUp | `172` | WordArt object. |
| TextSlantDown | `173` | WordArt object. |
| TextCanUp | `174` | WordArt object. |
| TextCanDown | `175` | WordArt object. |
| FlowChartAlternateProcess | `176` |  |
| FlowChartOffpageConnector | `177` |  |
| Callout90 | `178` |  |
| AccentCallout90 | `179` |  |
| BorderCallout90 | `180` |  |
| AccentBorderCallout90 | `181` |  |
| LeftRightUpArrow | `182` |  |
| Sun | `183` |  |
| Moon | `184` |  |
| BracketPair | `185` |  |
| BracePair | `186` |  |
| Seal4 | `187` |  |
| DoubleWave | `188` |  |
| ActionButtonBlank | `189` |  |
| ActionButtonHome | `190` |  |
| ActionButtonHelp | `191` |  |
| ActionButtonInformation | `192` |  |
| ActionButtonForwardNext | `193` |  |
| ActionButtonBackPrevious | `194` |  |
| ActionButtonEnd | `195` |  |
| ActionButtonBeginning | `196` |  |
| ActionButtonReturn | `197` |  |
| ActionButtonDocument | `198` |  |
| ActionButtonSound | `199` |  |
| ActionButtonMovie | `200` |  |
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
