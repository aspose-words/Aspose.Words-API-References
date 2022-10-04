---
title: ShapeType
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica el tipo de forma en un documento de Microsoft Word.
type: docs
weight: 1140
url: /es/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Especifica el tipo de forma en un documento de Microsoft Word.

```csharp
public enum ShapeType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Image | `75` | La forma es una imagen. |
| TextBox | `202` | La forma es un cuadro de texto. Tenga en cuenta que las formas de muchos otros tipos también pueden tener texto dentro de ellas. Una forma no tiene que tener este tipo para contener texto. |
| Group | `-1` | La forma es una forma de grupo. |
| OleObject | `-2` | La forma es un objeto OLE. |
| OleControl | `201` | La forma es un control ActiveX. |
| NonPrimitive | `0` | Una forma dibujada por el usuario y que consta de múltiples segmentos y/o vértices (curva, forma libre o garabato). |
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
| CustomShape | `100` | Este tipo de forma parece estar configurado para formas que no forman parte del conjunto estándar de formas automáticas en Microsoft Word. Por ejemplo, si inserta una nueva forma automática desde ClipArt. |
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
| TextPlainText | `136` | objeto WordArt. |
| TextStop | `137` | objeto WordArt. |
| TextTriangle | `138` | objeto WordArt. |
| TextTriangleInverted | `139` | objeto WordArt. |
| TextChevron | `140` | objeto WordArt. |
| TextChevronInverted | `141` | objeto WordArt. |
| TextRingInside | `142` | objeto WordArt. |
| TextRingOutside | `143` | objeto WordArt. |
| TextArchUpCurve | `144` | objeto WordArt. |
| TextArchDownCurve | `145` | objeto WordArt. |
| TextCircleCurve | `146` | objeto WordArt. |
| TextButtonCurve | `147` | objeto WordArt. |
| TextArchUpPour | `148` | objeto WordArt. |
| TextArchDownPour | `149` | objeto WordArt. |
| TextCirclePour | `150` | objeto WordArt. |
| TextButtonPour | `151` | objeto WordArt. |
| TextCurveUp | `152` | objeto WordArt. |
| TextCurveDown | `153` | objeto WordArt. |
| TextCascadeUp | `154` | objeto WordArt. |
| TextCascadeDown | `155` | objeto WordArt. |
| TextWave1 | `156` | objeto WordArt. |
| TextWave2 | `157` | objeto WordArt. |
| TextWave3 | `158` | objeto WordArt. |
| TextWave4 | `159` | objeto WordArt. |
| TextInflate | `160` | objeto WordArt. |
| TextDeflate | `161` | objeto WordArt. |
| TextInflateBottom | `162` | objeto WordArt. |
| TextDeflateBottom | `163` | objeto WordArt. |
| TextInflateTop | `164` | objeto WordArt. |
| TextDeflateTop | `165` | objeto WordArt. |
| TextDeflateInflate | `166` | objeto WordArt. |
| TextDeflateInflateDeflate | `167` | objeto WordArt. |
| TextFadeRight | `168` | objeto WordArt. |
| TextFadeLeft | `169` | objeto WordArt. |
| TextFadeUp | `170` | objeto WordArt. |
| TextFadeDown | `171` | objeto WordArt. |
| TextSlantUp | `172` | objeto WordArt. |
| TextSlantDown | `173` | objeto WordArt. |
| TextCanUp | `174` | objeto WordArt. |
| TextCanDown | `175` | objeto WordArt. |
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
| SingleCornerSnipped | `203` | Cortar objeto de rectángulo de una sola esquina. |
| TopCornersSnipped | `204` | Recorte el rectángulo de la esquina del mismo lado. |
| DiagonalCornersSnipped | `205` | Rectángulo de esquina diagonal de corte. |
| TopCornersOneRoundedOneSnipped | `206` | Recorte y redondee el rectángulo de una sola esquina. |
| SingleCornerRounded | `207` | Rectángulo redondo de una sola esquina. |
| TopCornersRounded | `208` | Rectángulo de esquina redondeado del mismo lado. |
| DiagonalCornersRounded | `209` | Rectángulo de esquina diagonal redondeada. |
| Heptagon | `210` | Heptágono. |
| Cloud | `211` | Nube. |
| Seal6 | `212` | Estrella de seis puntas. |
| Seal7 | `213` | Estrella de siete puntas. |
| Seal10 | `214` | Estrella de diez puntas. |
| Seal12 | `215` | Estrella de doce puntas. |
| SwooshArrow | `216` | Flecha Swoosh. |
| Teardrop | `217` | Lágrima. |
| SquareTabs | `218` | Pestañas cuadradas. |
| PlaqueTabs | `219` | Pestañas placa. |
| Pie | `220` | Pie. |
| WedgePie | `221` | Pastel de cuña. |
| InverseLine | `222` | Línea inversa. |
| MathPlus | `223` | Más matemáticas. |
| MathMinus | `224` | Matemáticas menos. |
| MathMultiply | `225` | Multiplicación matemática. |
| MathDivide | `226` | División matemática. |
| MathEqual | `227` | Igualdad matemática. |
| MathNotEqual | `228` | Matemáticas no iguales. |
| NonIsoscelesTrapezoid | `229` | Trapezoide no isósceles. |
| LeftRightCircularArrow | `230` | Flecha circular izquierda-derecha. |
| LeftRightRibbon | `231` | Cinta izquierda-derecha. |
| LeftCircularArrow | `232` | Flecha circular izquierda. |
| Frame | `233` | Cuadro. |
| HalfFrame | `234` | Medio cuadro. |
| Funnel | `235` | Embudo. |
| Gear6 | `236` | Engranaje de seis dientes. |
| Gear9 | `237` | Engranaje de nueve dientes. |
| Decagon | `238` | Decágono. |
| Dodecagon | `239` | Dodecágono. |
| DiagonalStripe | `240` | Franja diagonal. |
| Corner | `241` | Esquina. |
| CornerTabs | `242` | Pestañas de esquina. |
| Chord | `243` | Acorde. |
| ChartPlus | `244` | Gráfico más. |
| ChartStar | `245` | Estrella del gráfico. |
| ChartX | `246` | Gráfico X. |
| MinValue | `-2` | Reservado para uso del sistema. |

### Ejemplos

Muestra cómo insertar una forma con una imagen del sistema de archivos local en un documento.

```csharp
Document doc = new Document();

// El constructor público de la clase "Shape" creará una forma con el tipo de marcado "ShapeMarkupLanguage.Vml".
// Si necesita crear una forma de un tipo no primitivo, como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded o DiagonalCornersRounded,
// utilice DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Muestra cómo Aspose.Words identifica formas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Para corregir la identificación de tipos de formas, debe trabajar con formas como DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // El cumplimiento "Estricto" o "Transicional" permite guardar la forma como DML.
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

### Ver también

* property [ShapeType](../shapebase/shapetype/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
