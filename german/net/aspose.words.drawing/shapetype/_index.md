---
title: ShapeType Enum
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words.Drawing.ShapeType, um Formtypen in Ihren Microsoft Word-Dokumenten zu definieren und anzupassen, um die visuelle Attraktivität zu verbessern.
type: docs
weight: 1690
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
| TextBox | `202` | Die Form ist ein Textfeld. Beachten Sie, dass auch Formen vieler anderer Typen Text enthalten können. Eine Form muss nicht diesem Typ angehören, um Text zu enthalten. |
| Group | `-1` | Bei der Form handelt es sich um eine Gruppenform. |
| OleObject | `-2` | Die Form ist ein OLE-Objekt. |
| OleControl | `201` | Die Form ist ein ActiveX-Steuerelement. |
| NonPrimitive | `0` | Eine vom Benutzer gezeichnete Form, die aus mehreren Segmenten und/oder Scheitelpunkten besteht (Kurve, Freiform oder Kritzeleien). |
| Rectangle | `1` | Rechteck. |
| RoundRectangle | `2` | Rundes Rechteck. |
| Ellipse | `3` | Ellipse. |
| Diamond | `4` | Diamant. |
| Triangle | `5` | Dreieck. |
| RightTriangle | `6` | Rechtwinkliges Dreieck. |
| Parallelogram | `7` | Parallelogramm. |
| Trapezoid | `8` | Trapez. |
| Hexagon | `9` | Sechseck. |
| Octagon | `10` | Achteck. |
| Plus | `11` | Plus. |
| Star | `12` | Stern. |
| Arrow | `13` | Pfeil. |
| ThickArrow | `14` | Dicker Pfeil. |
| HomePlate | `15` | Home Plate. |
| Cube | `16` | Würfel. |
| Balloon | `17` | Ballon. |
| Seal | `18` | Siegel. |
| Arc | `19` | Bogen. |
| Line | `20` | Zeile. |
| Plaque | `21` | Plakette. |
| Can | `22` | Kann. |
| Donut | `23` | Donut. |
| TextSimple | `24` | Text einfach. |
| TextOctagon | `25` | Text Achteck. |
| TextHexagon | `26` | Textsechseck. |
| TextCurve | `27` | Textkurve. |
| TextWave | `28` | Textwelle. |
| TextRing | `29` | Textring. |
| TextOnCurve | `30` | Text auf Kurve. |
| TextOnRing | `31` | Text auf dem Ring. |
| StraightConnector1 | `32` | Eine gerade Verbindungsform. |
| BentConnector2 | `33` | Eine gebogene Verbindungsform mit zwei Segmenten. |
| BentConnector3 | `34` | Eine gebogene Verbindungsform mit drei Segmenten. |
| BentConnector4 | `35` | Eine gebogene Verbindungsform mit vier Segmenten. |
| BentConnector5 | `36` | Eine gebogene Verbindungsform mit fünf Segmenten. |
| CurvedConnector2 | `37` | Eine gebogene Verbindungsform mit zwei Segmenten. |
| CurvedConnector3 | `38` | Eine gebogene Verbindungsform mit drei Segmenten. |
| CurvedConnector4 | `39` | Eine gebogene Verbindungsform mit vier Segmenten. |
| CurvedConnector5 | `40` | Eine gebogene Verbindungsform mit fünf Segmenten. |
| Callout1 | `41` | Eine Callout-Form mit einem Pfeil. |
| Callout2 | `42` | Eine Callout-Form mit zwei Pfeilen. |
| Callout3 | `43` | Eine Callout-Form mit drei Pfeilen. |
| AccentCallout1 | `44` | Eine Akzent-Callout-Form mit einem Pfeil. |
| AccentCallout2 | `45` | Eine Akzent-Callout-Form mit zwei Pfeilen. |
| AccentCallout3 | `46` | Eine Akzent-Callout-Form mit drei Pfeilen. |
| BorderCallout1 | `47` | Randbeschriftung 1. |
| BorderCallout2 | `48` | Randbeschriftung 2. |
| BorderCallout3 | `49` | Randbeschriftung 3. |
| AccentBorderCallout1 | `50` | Akzent-Rahmen-Callout 1. |
| AccentBorderCallout2 | `51` | Akzent-Rahmen-Callout 2. |
| AccentBorderCallout3 | `52` | Akzent-Rahmen-Callout 3. |
| Ribbon | `53` | Band. |
| Ribbon2 | `54` | Band 2. |
| Chevron | `55` | Chevron. |
| Pentagon | `56` | Fünfeck. |
| NoSmoking | `57` | Rauchen verboten. |
| Seal8 | `58` | Achtzackiger Stern. |
| Seal16 | `59` | 16-zackiger Stern. |
| Seal32 | `60` | 32-zackiger Stern. |
| WedgeRectCallout | `61` | Keilrechteck-Beschriftung. |
| WedgeRRectCallout | `62` | Keil R Rechteck-Beschriftung. |
| WedgeEllipseCallout | `63` | Keilellipsen-Beschriftung. |
| Wave | `64` | Welle. |
| FoldedCorner | `65` | Gefaltete Ecke. |
| LeftArrow | `66` | Pfeil nach links. |
| DownArrow | `67` | Pfeil nach unten. |
| UpArrow | `68` | Pfeil nach oben. |
| LeftRightArrow | `69` | Pfeil links rechts. |
| UpDownArrow | `70` | Pfeil nach oben/unten. |
| IrregularSeal1 | `71` | Unregelmäßiges Siegel 1. |
| IrregularSeal2 | `72` | Unregelmäßiges Siegel 2. |
| LightningBolt | `73` | Blitzschlag. |
| Heart | `74` | Herz. |
| QuadArrow | `76` | Vierfachpfeil. |
| LeftArrowCallout | `77` | Linker Pfeil-Callout. |
| RightArrowCallout | `78` | Rechtspfeil-Callout |
| UpArrowCallout | `79` | Aufwärtspfeil-Beschriftung. |
| DownArrowCallout | `80` | Abwärtspfeil-Beschriftung. |
| LeftRightArrowCallout | `81` | Legende mit Pfeil nach links und rechts. |
| UpDownArrowCallout | `82` | Legende mit Pfeil nach oben und unten. |
| QuadArrowCallout | `83` | Quad-Pfeil-Beschriftung. |
| Bevel | `84` | Abschrägung. |
| LeftBracket | `85` | Linke Klammer. |
| RightBracket | `86` | Rechte Klammer. |
| LeftBrace | `87` | Linke Klammer. |
| RightBrace | `88` | Rechte Klammer. |
| LeftUpArrow | `89` | Pfeil nach links oben. |
| BentUpArrow | `90` | Nach oben gebogener Pfeil. |
| BentArrow | `91` | Gebogener Pfeil. |
| Seal24 | `92` | 24-zackiger Stern. |
| StripedRightArrow | `93` | Gestreifter Pfeil nach rechts. |
| NotchedRightArrow | `94` | Eingekerbter Pfeil nach rechts. |
| BlockArc | `95` | Blockbogen. |
| SmileyFace | `96` | Smiley-Gesicht. |
| VerticalScroll | `97` | Vertikales Scrollen. |
| HorizontalScroll | `98` | Horizontales Scrollen. |
| CircularArrow | `99` | Kreisförmiger Pfeil. |
| CustomShape | `100` | Dieser Formtyp scheint für Formen verwendet zu werden, die nicht zum Standardsatz der Auto-Formen in Microsoft Word gehören. Beispielsweise, wenn Sie eine neue Auto-Form aus ClipArt einfügen. |
| UturnArrow | `101` | Kehrtwende-Pfeil. |
| CurvedRightArrow | `102` | Gebogener Pfeil nach rechts. |
| CurvedLeftArrow | `103` | Gebogener Pfeil nach links. |
| CurvedUpArrow | `104` | Gebogener Pfeil nach oben |
| CurvedDownArrow | `105` | Nach unten gebogener Pfeil. |
| CloudCallout | `106` | Cloud-Callout. |
| EllipseRibbon | `107` | Ellipsenband. |
| EllipseRibbon2 | `108` | Ellipsenband 2. |
| FlowChartProcess | `109` | Flussdiagrammprozess. |
| FlowChartDecision | `110` | Flussdiagrammentscheidung. |
| FlowChartInputOutput | `111` | Flussdiagramm Eingabe Ausgabe. |
| FlowChartPredefinedProcess | `112` | Flussdiagramm vordefinierter Prozess |
| FlowChartInternalStorage | `113` | Flussdiagramm interner Speicher. |
| FlowChartDocument | `114` | Flussdiagrammdokument. |
| FlowChartMultidocument | `115` | Flussdiagramm, mehrere Dokumente. |
| FlowChartTerminator | `116` | Flussdiagramm-Abschlusszeichen. |
| FlowChartPreparation | `117` | Flussdiagrammvorbereitung. |
| FlowChartManualInput | `118` | Flussdiagramm manuelle Eingabe. |
| FlowChartManualOperation | `119` | Flussdiagramm manuelle Bedienung. |
| FlowChartConnector | `120` | Flussdiagramm-Anschluss. |
| FlowChartPunchedCard | `121` | Flussdiagramm-Lochkarte. |
| FlowChartPunchedTape | `122` | Flussdiagramm Lochstreifen. |
| FlowChartSummingJunction | `123` | Flussdiagramm Summierknoten. |
| FlowChartOr | `124` | Flussdiagramm oder. |
| FlowChartCollate | `125` | Flussdiagramm zusammenstellen. |
| FlowChartSort | `126` | Flussdiagramm sortieren. |
| FlowChartExtract | `127` | Flussdiagrammauszug. |
| FlowChartMerge | `128` | Flussdiagramm zusammenführen. |
| FlowChartOfflineStorage | `129` | Flussdiagramm Offline-Speicher. |
| FlowChartOnlineStorage | `130` | Flussdiagramm Online-Speicher. |
| FlowChartMagneticTape | `131` | Fließchar-Magnetband. |
| FlowChartMagneticDisk | `132` | Flussdiagramm Magnetplatte. |
| FlowChartMagneticDrum | `133` | Flussdiagramm Magnettrommel. |
| FlowChartDisplay | `134` | Flussdiagrammanzeige. |
| FlowChartDelay | `135` | Flussdiagrammverzögerung. |
| TextPlainText | `136` | Nur-Text, WordArt-Objekt. |
| TextStop | `137` | Stopp, WordArt-Objekt. |
| TextTriangle | `138` | Dreieck, WordArt-Objekt. |
| TextTriangleInverted | `139` | Dreieck umgedreht, WordArt-Objekt. |
| TextChevron | `140` | Chevron, WordArt-Objekt. |
| TextChevronInverted | `141` | Chevron invertiert, WordArt-Objekt. |
| TextRingInside | `142` | Ring innen, WordArt-Objekt. |
| TextRingOutside | `143` | Ring außen, WordArt-Objekt. |
| TextArchUpCurve | `144` | Bogen nach oben, WordArt-Objekt. |
| TextArchDownCurve | `145` | Bogen nach unten, WordArt-Objekt. |
| TextCircleCurve | `146` | Kreiskurve, WordArt-Objekt. |
| TextButtonCurve | `147` | Schaltflächenkurve, WordArt-Objekt. |
| TextArchUpPour | `148` | Aufgewölbt, WordArt-Objekt. |
| TextArchDownPour | `149` | Bogenförmiger Regenguss, WordArt-Objekt. |
| TextCirclePour | `150` | Kreisform, WordArt-Objekt. |
| TextButtonPour | `151` | Schaltfläche für WordArt-Objekt. |
| TextCurveUp | `152` | Kurve nach oben, WordArt-Objekt. |
| TextCurveDown | `153` | Kurve nach unten, WordArt-Objekt. |
| TextCascadeUp | `154` | Nach oben kaskadieren, WordArt-Objekt. |
| TextCascadeDown | `155` | Nach unten kaskadieren, WordArt-Objekt. |
| TextWave1 | `156` | Welle 1, WordArt-Objekt. |
| TextWave2 | `157` | Welle 2, WordArt-Objekt. |
| TextWave3 | `158` | Welle 3, WordArt-Objekt. |
| TextWave4 | `159` | Welle 4, WordArt-Objekt. |
| TextInflate | `160` | Aufblasen, WordArt-Objekt. |
| TextDeflate | `161` | Deflate, WordArt-Objekt. |
| TextInflateBottom | `162` | Unten aufblasen, WordArt-Objekt. |
| TextDeflateBottom | `163` | Unten entlüften, WordArt-Objekt. |
| TextInflateTop | `164` | Oben aufblasen, WordArt-Objekt. |
| TextDeflateTop | `165` | Oben entleeren, WordArt-Objekt. |
| TextDeflateInflate | `166` | Deflate aufblasen, WordArt-Objekt. |
| TextDeflateInflateDeflate | `167` | Entleeren, aufblasen, entleeren, WordArt-Objekt. |
| TextFadeRight | `168` | Nach rechts ausblenden, WordArt-Objekt. |
| TextFadeLeft | `169` | Nach links ausblenden, WordArt-Objekt. |
| TextFadeUp | `170` | Aufblenden, WordArt-Objekt. |
| TextFadeDown | `171` | Ausblenden, WordArt-Objekt. |
| TextSlantUp | `172` | Schräg nach oben, WordArt-Objekt. |
| TextSlantDown | `173` | Nach unten geneigt, WordArt-Objekt. |
| TextCanUp | `174` | Kann hoch, WordArt-Objekt. |
| TextCanDown | `175` | Kann runter, WordArt-Objekt. |
| FlowChartAlternateProcess | `176` | Flussdiagramm alternativer Prozess. |
| FlowChartOffpageConnector | `177` | Flussdiagramm-Offpage-Anschluss. |
| Callout90 | `178` | Legende 90. |
| AccentCallout90 | `179` | Akzent-Callout 90. |
| BorderCallout90 | `180` | Randbeschriftung 90. |
| AccentBorderCallout90 | `181` | Akzent-Rahmen-Beschriftung 90. |
| LeftRightUpArrow | `182` | Pfeil links rechts oben. |
| Sun | `183` | So. |
| Moon | `184` | Mond. |
| BracketPair | `185` | Klammerpaar. |
| BracePair | `186` | Klammerpaar |
| Seal4 | `187` | Vierzackiger Stern. |
| DoubleWave | `188` | Doppelwelle. |
| ActionButtonBlank | `189` | Aktionsschaltfläche leer. |
| ActionButtonHome | `190` | Aktionsschaltfläche Home. |
| ActionButtonHelp | `191` | Hilfe zur Aktionsschaltfläche. |
| ActionButtonInformation | `192` | Informationen zur Aktionsschaltfläche. |
| ActionButtonForwardNext | `193` | Aktionsschaltfläche „Weiter“ |
| ActionButtonBackPrevious | `194` | Aktionsschaltfläche Zurück Vorherige. |
| ActionButtonEnd | `195` | Aktionsschaltfläche Ende. |
| ActionButtonBeginning | `196` | Aktionsschaltfläche beginnt. |
| ActionButtonReturn | `197` | Aktionsschaltfläche „Zurück“ |
| ActionButtonDocument | `198` | Dokument mit Aktionsschaltfläche. |
| ActionButtonSound | `199` | Ton der Aktionstaste. |
| ActionButtonMovie | `200` | Action-Button-Film. |
| SingleCornerSnipped | `203` | Rechteckiges Objekt mit einer Ecke ausschneiden. |
| TopCornersSnipped | `204` | Rechteck an der Ecke derselben Seite ausschneiden. |
| DiagonalCornersSnipped | `205` | Diagonales Eckrechteck ausschneiden. |
| TopCornersOneRoundedOneSnipped | `206` | Rechteck mit einer Ecke ausschneiden und abrunden. |
| SingleCornerRounded | `207` | Rundes Rechteck mit einer Ecke. |
| TopCornersRounded | `208` | Rundes Rechteck mit gleicher Seitenecke. |
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
| PlaqueTabs | `219` | Plakettenlaschen. |
| Pie | `220` | Kuchen. |
| WedgePie | `221` | Keilkuchen. |
| InverseLine | `222` | Inverse Linie. |
| MathPlus | `223` | Mathe plus. |
| MathMinus | `224` | Mathe minus. |
| MathMultiply | `225` | Mathematische Multiplikation. |
| MathDivide | `226` | Mathematische Division. |
| MathEqual | `227` | Mathematisch gleich. |
| MathNotEqual | `228` | Mathematik ungleich. |
| NonIsoscelesTrapezoid | `229` | Nicht gleichschenkliges Trapez. |
| LeftRightCircularArrow | `230` | Links-rechts-Kreispfeil. |
| LeftRightRibbon | `231` | Links-rechts-Band. |
| LeftCircularArrow | `232` | Linker kreisförmiger Pfeil. |
| Frame | `233` | Rahmen. |
| HalfFrame | `234` | Halbbild. |
| Funnel | `235` | Trichter. |
| Gear6 | `236` | Sechszahnrad. |
| Gear9 | `237` | Zahnrad mit neun Zähnen. |
| Decagon | `238` | Zehneck. |
| Dodecagon | `239` | Zwölfeck. |
| DiagonalStripe | `240` | Diagonalstreifen. |
| Corner | `241` | Ecke. |
| CornerTabs | `242` | Ecklaschen. |
| Chord | `243` | Akkord. |
| ChartPlus | `244` | Diagramm plus. |
| ChartStar | `245` | Chartstern. |
| ChartX | `246` | Diagramm X. |
| MinValue | `-2` | Für die Systemnutzung reserviert. |

## Beispiele

Zeigt, wie eine Form mit einem Bild aus dem lokalen Dateisystem in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();

// Der öffentliche Konstruktor der Klasse „Shape“ erstellt eine Form mit dem Markup-Typ „ShapeMarkupLanguage.Vml“.
// Wenn Sie eine Form eines nicht-primitiven Typs erstellen müssen, z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// bitte verwenden Sie DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Zeigt, wie Aspose.Words Formen identifizieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Um Formtypen richtig zu identifizieren, müssen Sie mit Formen als DML arbeiten.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // Die „strenge“ oder „vorübergehende“ Konformität ermöglicht das Speichern der Form als DML.
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
