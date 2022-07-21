---
title: ShapeType
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie le type de forme dans un document Microsoft Word.
type: docs
weight: 1140
url: /fr/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Spécifie le type de forme dans un document Microsoft Word.

```csharp
public enum ShapeType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Image | `75` | La forme est une image. |
| TextBox | `202` | La forme est une zone de texte. Notez que les formes de nombreux autres types peuvent également contenir du texte. Une forme n'a pas besoin d'avoir ce type pour contenir du texte. |
| Group | `-1` | La forme est une forme de groupe. |
| OleObject | `-2` | La forme est un objet OLE. |
| OleControl | `201` | La forme est un contrôle ActiveX. |
| NonPrimitive | `0` | Une forme dessinée par l'utilisateur et composée de plusieurs segments et/ou sommets (courbe, forme libre ou gribouillis). |
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
| CustomShape | `100` | Ce type de forme semble être défini pour les formes qui ne font pas partie de l'ensemble standard des formes automatiques dans Microsoft Word. Par exemple, si vous insérez une nouvelle forme automatique à partir de ClipArt. |
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
| TextPlainText | `136` | Objet WordArt. |
| TextStop | `137` | Objet WordArt. |
| TextTriangle | `138` | Objet WordArt. |
| TextTriangleInverted | `139` | Objet WordArt. |
| TextChevron | `140` | Objet WordArt. |
| TextChevronInverted | `141` | Objet WordArt. |
| TextRingInside | `142` | Objet WordArt. |
| TextRingOutside | `143` | Objet WordArt. |
| TextArchUpCurve | `144` | Objet WordArt. |
| TextArchDownCurve | `145` | Objet WordArt. |
| TextCircleCurve | `146` | Objet WordArt. |
| TextButtonCurve | `147` | Objet WordArt. |
| TextArchUpPour | `148` | Objet WordArt. |
| TextArchDownPour | `149` | Objet WordArt. |
| TextCirclePour | `150` | Objet WordArt. |
| TextButtonPour | `151` | Objet WordArt. |
| TextCurveUp | `152` | Objet WordArt. |
| TextCurveDown | `153` | Objet WordArt. |
| TextCascadeUp | `154` | Objet WordArt. |
| TextCascadeDown | `155` | Objet WordArt. |
| TextWave1 | `156` | Objet WordArt. |
| TextWave2 | `157` | Objet WordArt. |
| TextWave3 | `158` | Objet WordArt. |
| TextWave4 | `159` | Objet WordArt. |
| TextInflate | `160` | Objet WordArt. |
| TextDeflate | `161` | Objet WordArt. |
| TextInflateBottom | `162` | Objet WordArt. |
| TextDeflateBottom | `163` | Objet WordArt. |
| TextInflateTop | `164` | Objet WordArt. |
| TextDeflateTop | `165` | Objet WordArt. |
| TextDeflateInflate | `166` | Objet WordArt. |
| TextDeflateInflateDeflate | `167` | Objet WordArt. |
| TextFadeRight | `168` | Objet WordArt. |
| TextFadeLeft | `169` | Objet WordArt. |
| TextFadeUp | `170` | Objet WordArt. |
| TextFadeDown | `171` | Objet WordArt. |
| TextSlantUp | `172` | Objet WordArt. |
| TextSlantDown | `173` | Objet WordArt. |
| TextCanUp | `174` | Objet WordArt. |
| TextCanDown | `175` | Objet WordArt. |
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
| SingleCornerSnipped | `203` | Couper un objet rectangle à coin unique. |
| TopCornersSnipped | `204` | Couper le rectangle d'angle du même côté. |
| DiagonalCornersSnipped | `205` | Coupez le rectangle d'angle en diagonale. |
| TopCornersOneRoundedOneSnipped | `206` | Couper et arrondir un rectangle à un coin. |
| SingleCornerRounded | `207` | Rectangle rond à un seul coin. |
| TopCornersRounded | `208` | Rectangle rond du même côté. |
| DiagonalCornersRounded | `209` | Rectangle rond en diagonale. |
| Heptagon | `210` | Heptagone. |
| Cloud | `211` | Nuage. |
| Seal6 | `212` | Étoile à six branches. |
| Seal7 | `213` | Étoile à sept branches. |
| Seal10 | `214` | Étoile à dix branches. |
| Seal12 | `215` | Étoile à douze branches. |
| SwooshArrow | `216` | Flèche Swoosh. |
| Teardrop | `217` | Larme. |
| SquareTabs | `218` | Onglets carrés. |
| PlaqueTabs | `219` | Onglets de plaque. |
| Pie | `220` | Tarte. |
| WedgePie | `221` | Tarte en coin. |
| InverseLine | `222` | Ligne inverse. |
| MathPlus | `223` | Mathématiques plus. |
| MathMinus | `224` | Math moins. |
| MathMultiply | `225` | Multiplication mathématique. |
| MathDivide | `226` | Division mathématique. |
| MathEqual | `227` | Math égal. |
| MathNotEqual | `228` | Mathématiques non égales. |
| NonIsoscelesTrapezoid | `229` | Trapèze non isocèle. |
| LeftRightCircularArrow | `230` | Flèche circulaire gauche-droite. |
| LeftRightRibbon | `231` | Ruban gauche-droite. |
| LeftCircularArrow | `232` | Flèche circulaire gauche. |
| Frame | `233` | Cadre. |
| HalfFrame | `234` | Demi cadre. |
| Funnel | `235` | Entonnoir. |
| Gear6 | `236` | Engrenage à six dents. |
| Gear9 | `237` | Engrenage à neuf dents. |
| Decagon | `238` | décagone. |
| Dodecagon | `239` | Dodécagone. |
| DiagonalStripe | `240` | Bande diagonale. |
| Corner | `241` | Coin. |
| CornerTabs | `242` | Onglets d'angle. |
| Chord | `243` | Accord. |
| ChartPlus | `244` | Graphique plus. |
| ChartStar | `245` | Carte étoile. |
| ChartX | `246` | Graphique X. |
| MinValue | `-2` | Réservé à l'utilisation du système. |

### Exemples

Montre comment insérer une forme avec une image du système de fichiers local dans un document.

```csharp
Document doc = new Document();

// Le constructeur public de la classe "Shape" créera une forme avec le type de balisage "ShapeMarkupLanguage.Vml".
// Si vous devez créer une forme d'un type non primitif, tel que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded ou DiagonalCornersRounded,
// veuillez utiliser DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Montre comment Aspose.Words identifie les formes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Pour corriger l'identification des types de formes, vous devez travailler avec des formes en tant que DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // La conformité "Stricte" ou "Transitionnelle" permet d'enregistrer la forme en DML.
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

### Voir également

* property [ShapeType](../shapebase/shapetype)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
