---
title: ShapeType
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt den Formtyp in einem Microsoft WordDokument an.
type: docs
weight: 1140
url: /de/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Gibt den Formtyp in einem Microsoft Word-Dokument an.

```csharp
public enum ShapeType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Image | `75` | Die Form ist ein Bild. |
| TextBox | `202` | Die Form ist ein Textfeld. Beachten Sie, dass Formen vieler anderer Typen auch Text enthalten können. Eine Form muss diesen Typ nicht haben, um Text zu enthalten. |
| Group | `-1` | Die Form ist eine Gruppenform. |
| OleObject | `-2` | Die Form ist ein OLE-Objekt. |
| OleControl | `201` | Die Form ist ein ActiveX-Steuerelement. |
| NonPrimitive | `0` | Eine vom Benutzer gezeichnete Form, die aus mehreren Segmenten und/oder Scheitelpunkten besteht (Kurve, Freiform oder Scribble). |
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
| CustomShape | `100` | Dieser Formtyp scheint für Formen eingestellt zu sein, die nicht Teil des Standardsatzes der automatischen Formen in Microsoft Word sind. Wenn Sie beispielsweise eine neue automatische Form aus ClipArt. einfügen |
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
| TextPlainText | `136` | WordArt-Objekt. |
| TextStop | `137` | WordArt-Objekt. |
| TextTriangle | `138` | WordArt-Objekt. |
| TextTriangleInverted | `139` | WordArt-Objekt. |
| TextChevron | `140` | WordArt-Objekt. |
| TextChevronInverted | `141` | WordArt-Objekt. |
| TextRingInside | `142` | WordArt-Objekt. |
| TextRingOutside | `143` | WordArt-Objekt. |
| TextArchUpCurve | `144` | WordArt-Objekt. |
| TextArchDownCurve | `145` | WordArt-Objekt. |
| TextCircleCurve | `146` | WordArt-Objekt. |
| TextButtonCurve | `147` | WordArt-Objekt. |
| TextArchUpPour | `148` | WordArt-Objekt. |
| TextArchDownPour | `149` | WordArt-Objekt. |
| TextCirclePour | `150` | WordArt-Objekt. |
| TextButtonPour | `151` | WordArt-Objekt. |
| TextCurveUp | `152` | WordArt-Objekt. |
| TextCurveDown | `153` | WordArt-Objekt. |
| TextCascadeUp | `154` | WordArt-Objekt. |
| TextCascadeDown | `155` | WordArt-Objekt. |
| TextWave1 | `156` | WordArt-Objekt. |
| TextWave2 | `157` | WordArt-Objekt. |
| TextWave3 | `158` | WordArt-Objekt. |
| TextWave4 | `159` | WordArt-Objekt. |
| TextInflate | `160` | WordArt-Objekt. |
| TextDeflate | `161` | WordArt-Objekt. |
| TextInflateBottom | `162` | WordArt-Objekt. |
| TextDeflateBottom | `163` | WordArt-Objekt. |
| TextInflateTop | `164` | WordArt-Objekt. |
| TextDeflateTop | `165` | WordArt-Objekt. |
| TextDeflateInflate | `166` | WordArt-Objekt. |
| TextDeflateInflateDeflate | `167` | WordArt-Objekt. |
| TextFadeRight | `168` | WordArt-Objekt. |
| TextFadeLeft | `169` | WordArt-Objekt. |
| TextFadeUp | `170` | WordArt-Objekt. |
| TextFadeDown | `171` | WordArt-Objekt. |
| TextSlantUp | `172` | WordArt-Objekt. |
| TextSlantDown | `173` | WordArt-Objekt. |
| TextCanUp | `174` | WordArt-Objekt. |
| TextCanDown | `175` | WordArt-Objekt. |
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
| SingleCornerSnipped | `203` | Rechteckiges Objekt mit einer einzelnen Ecke ausschneiden. |
| TopCornersSnipped | `204` | Gleichseitiges Eckrechteck ausschneiden. |
| DiagonalCornersSnipped | `205` | Diagonales Eckrechteck ausschneiden. |
| TopCornersOneRoundedOneSnipped | `206` | Snip und abgerundetes Rechteck mit einer Ecke. |
| SingleCornerRounded | `207` | Rundes Rechteck mit einer Ecke. |
| TopCornersRounded | `208` | Rundes Rechteck mit gleicher Ecke. |
| DiagonalCornersRounded | `209` | Rechteck mit abgerundeten diagonalen Ecken. |
| Heptagon | `210` | Siebeneck. |
| Cloud | `211` | Wolke. |
| Seal6 | `212` | Sechszackiger Stern. |
| Seal7 | `213` | Siebenzackiger Stern. |
| Seal10 | `214` | Zehnzackiger Stern. |
| Seal12 | `215` | Zwölfzackiger Stern. |
| SwooshArrow | `216` | Swoosh-Pfeil. |
| Teardrop | `217` | Träne. |
| SquareTabs | `218` | Quadratische Registerkarten. |
| PlaqueTabs | `219` | Plakettenreiter. |
| Pie | `220` | Kuchen. |
| WedgePie | `221` | Keilkuchen. |
| InverseLine | `222` | Umkehrlinie. |
| MathPlus | `223` | Mathematik plus. |
| MathMinus | `224` | Mathe minus. |
| MathMultiply | `225` | Mathematik multiplizieren. |
| MathDivide | `226` | Mathematische Division. |
| MathEqual | `227` | Mathematik gleich. |
| MathNotEqual | `228` | Mathematik ungleich. |
| NonIsoscelesTrapezoid | `229` | Nicht gleichschenkliges Trapez. |
| LeftRightCircularArrow | `230` | Kreisförmiger Links-Rechts-Pfeil. |
| LeftRightRibbon | `231` | Links-rechts-Band. |
| LeftCircularArrow | `232` | Linker kreisförmiger Pfeil. |
| Frame | `233` | Rahmen. |
| HalfFrame | `234` | Halbbild. |
| Funnel | `235` | Trichter. |
| Gear6 | `236` | Zahnrad mit sechs Zähnen. |
| Gear9 | `237` | Zahnrad mit neun Zähnen. |
| Decagon | `238` | Zehneck. |
| Dodecagon | `239` | Zwölfeck. |
| DiagonalStripe | `240` | Diagonalstreifen. |
| Corner | `241` | Ecke. |
| CornerTabs | `242` | Ecklaschen. |
| Chord | `243` | Akkord. |
| ChartPlus | `244` | Diagramm plus. |
| ChartStar | `245` | Diagrammstern. |
| ChartX | `246` | Diagramm X. |
| MinValue | `-2` | Reserviert für die Systemnutzung. |

### Beispiele

Zeigt, wie Sie eine Form mit einem Bild aus dem lokalen Dateisystem in ein Dokument einfügen.

```csharp
Document doc = new Document();

// Der öffentliche Konstruktor der Klasse „Shape“ erstellt eine Form mit dem Markup-Typ „ShapeMarkupLanguage.Vml“.
// Wenn Sie eine Form eines nicht primitiven Typs erstellen müssen, z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Bitte verwenden Sie DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Zeigt, wie Aspose.Words Formen identifiziert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Um Formtypen korrekt zu identifizieren, müssen Sie mit Formen als DML arbeiten.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // „Strict“- oder „Transitional“-Compliance ermöglicht das Speichern der Form als DML.
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

### Siehe auch

* property [ShapeType](../shapebase/shapetype/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
