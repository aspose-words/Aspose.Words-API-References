---
title: Enum ShapeType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.ShapeType uppräkning. Anger typen av form i ett Microsoft Worddokument.
type: docs
weight: 1140
url: /sv/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Anger typen av form i ett Microsoft Word-dokument.

```csharp
public enum ShapeType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Image | `75` | Formen är en bild. |
| TextBox | `202` | Formen är en textruta. Observera att former av många andra typer också kan ha text i sig. En form behöver inte ha den här typen för att innehålla text. |
| Group | `-1` | Formen är en gruppform. |
| OleObject | `-2` | Formen är ett OLE-objekt. |
| OleControl | `201` | Formen är en ActiveX-kontroll. |
| NonPrimitive | `0` | En form ritad av användaren och som består av flera segment och/eller hörn (kurva, friform eller klotter). |
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
| CustomShape | `100` | Den här formtypen verkar vara inställd för former som inte ingår i standarduppsättningen av de automatiska formerna i Microsoft Word. Till exempel, om du infogar en ny automatisk form från ClipArt. |
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
| TextPlainText | `136` | WordArt-objekt. |
| TextStop | `137` | WordArt-objekt. |
| TextTriangle | `138` | WordArt-objekt. |
| TextTriangleInverted | `139` | WordArt-objekt. |
| TextChevron | `140` | WordArt-objekt. |
| TextChevronInverted | `141` | WordArt-objekt. |
| TextRingInside | `142` | WordArt-objekt. |
| TextRingOutside | `143` | WordArt-objekt. |
| TextArchUpCurve | `144` | WordArt-objekt. |
| TextArchDownCurve | `145` | WordArt-objekt. |
| TextCircleCurve | `146` | WordArt-objekt. |
| TextButtonCurve | `147` | WordArt-objekt. |
| TextArchUpPour | `148` | WordArt-objekt. |
| TextArchDownPour | `149` | WordArt-objekt. |
| TextCirclePour | `150` | WordArt-objekt. |
| TextButtonPour | `151` | WordArt-objekt. |
| TextCurveUp | `152` | WordArt-objekt. |
| TextCurveDown | `153` | WordArt-objekt. |
| TextCascadeUp | `154` | WordArt-objekt. |
| TextCascadeDown | `155` | WordArt-objekt. |
| TextWave1 | `156` | WordArt-objekt. |
| TextWave2 | `157` | WordArt-objekt. |
| TextWave3 | `158` | WordArt-objekt. |
| TextWave4 | `159` | WordArt-objekt. |
| TextInflate | `160` | WordArt-objekt. |
| TextDeflate | `161` | WordArt-objekt. |
| TextInflateBottom | `162` | WordArt-objekt. |
| TextDeflateBottom | `163` | WordArt-objekt. |
| TextInflateTop | `164` | WordArt-objekt. |
| TextDeflateTop | `165` | WordArt-objekt. |
| TextDeflateInflate | `166` | WordArt-objekt. |
| TextDeflateInflateDeflate | `167` | WordArt-objekt. |
| TextFadeRight | `168` | WordArt-objekt. |
| TextFadeLeft | `169` | WordArt-objekt. |
| TextFadeUp | `170` | WordArt-objekt. |
| TextFadeDown | `171` | WordArt-objekt. |
| TextSlantUp | `172` | WordArt-objekt. |
| TextSlantDown | `173` | WordArt-objekt. |
| TextCanUp | `174` | WordArt-objekt. |
| TextCanDown | `175` | WordArt-objekt. |
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
| SingleCornerSnipped | `203` | Klipp ett enda hörn rektangelobjekt. |
| TopCornersSnipped | `204` | Klipp samma sidohörnrektangel. |
| DiagonalCornersSnipped | `205` | Klipp diagonal hörnrektangel. |
| TopCornersOneRoundedOneSnipped | `206` | Klipp och rund rektangel i ett hörn. |
| SingleCornerRounded | `207` | Rund enkelhörnrektangel. |
| TopCornersRounded | `208` | Runda samma sidohörnrektangel. |
| DiagonalCornersRounded | `209` | Rund diagonal hörnrektangel. |
| Heptagon | `210` | Heptagon. |
| Cloud | `211` | Moln. |
| Seal6 | `212` | Sexuddig stjärna. |
| Seal7 | `213` | Sjuuddig stjärna. |
| Seal10 | `214` | Tiouddig stjärna. |
| Seal12 | `215` | Tolvuddig stjärna. |
| SwooshArrow | `216` | Swoosh arrow. |
| Teardrop | `217` | Teardrop. |
| SquareTabs | `218` | Fyrkantiga flikar. |
| PlaqueTabs | `219` | Plaque tabs. |
| Pie | `220` | Pie. |
| WedgePie | `221` | Kilpaj. |
| InverseLine | `222` | Omvänd linje. |
| MathPlus | `223` | Math plus. |
| MathMinus | `224` | Matematik minus. |
| MathMultiply | `225` | Math multiplicera. |
| MathDivide | `226` | Math divide. |
| MathEqual | `227` | Math lika. |
| MathNotEqual | `228` | Math inte lika. |
| NonIsoscelesTrapezoid | `229` | Icke-likbent trapets. |
| LeftRightCircularArrow | `230` | Vänster-höger cirkulär pil. |
| LeftRightRibbon | `231` | Vänster-höger band. |
| LeftCircularArrow | `232` | Vänster cirkulär pil. |
| Frame | `233` | Ram. |
| HalfFrame | `234` | Halv ram. |
| Funnel | `235` | Tratt. |
| Gear6 | `236` | Sextands växel. |
| Gear9 | `237` | Niotands växel. |
| Decagon | `238` | Decagon. |
| Dodecagon | `239` | Dodecagon. |
| DiagonalStripe | `240` | Diagonal rand. |
| Corner | `241` | Hörn. |
| CornerTabs | `242` | Hörnflikar. |
| Chord | `243` | Ackord. |
| ChartPlus | `244` | Diagram plus. |
| ChartStar | `245` | Sjökortsstjärna. |
| ChartX | `246` | Diagram X. |
| MinValue | `-2` | Reserverad för systemanvändning. |

### Exempel

Visar hur man infogar en form med en bild från det lokala filsystemet i ett dokument.

```csharp
Document doc = new Document();

// "Shape"-klassens offentliga konstruktor kommer att skapa en form med "ShapeMarkupLanguage.Vml"-typ.
// Om du behöver skapa en form av en icke-primitiv typ, till exempel SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded eller DiagonalCornersRounded,
// använd DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Visar hur Aspose.Words identifierar former.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// För att korrigera identifiera formtyper måste du arbeta med former som DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // "Strikt" eller "Övergångsöverensstämmelse" gör det möjligt att spara form som DML.
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

### Se även

* property [ShapeType](../shapebase/shapetype/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)


