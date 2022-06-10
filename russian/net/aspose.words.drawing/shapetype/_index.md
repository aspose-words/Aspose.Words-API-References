---
title: ShapeType
second_title: Справочник по API Aspose.Words для .NET
description: Указывает тип фигуры в документе Microsoft Word.
type: docs
weight: 1120
url: /ru/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Указывает тип фигуры в документе Microsoft Word.

```csharp
public enum ShapeType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Image | `75` | Форма - это изображение. |
| TextBox | `202` | Форма представляет собой текстовое поле. Обратите внимание, что фигуры многих других типов также могут содержать текст внутри себя. Фигура не обязательно должна иметь этот тип, чтобы содержать текст. |
| Group | `-1` | Форма представляет собой групповую форму. |
| OleObject | `-2` | Фигура является объектом OLE. |
| OleControl | `201` | Форма представляет собой элемент управления ActiveX. |
| NonPrimitive | `0` | Фигура, нарисованная пользователем и состоящая из нескольких сегментов и/или вершин (кривая, произвольная форма или каракули). |
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
| CustomShape | `100` | Этот тип фигуры, по-видимому, установлен для фигур, которые не являются частью стандартного набора автоматических фигур в Microsoft Word. Например, если вы вставите новую автофигуру из ClipArt. |
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
| TextPlainText | `136` | Объект WordArt. |
| TextStop | `137` | Объект WordArt. |
| TextTriangle | `138` | Объект WordArt. |
| TextTriangleInverted | `139` | Объект WordArt. |
| TextChevron | `140` | Объект WordArt. |
| TextChevronInverted | `141` | Объект WordArt. |
| TextRingInside | `142` | Объект WordArt. |
| TextRingOutside | `143` | Объект WordArt. |
| TextArchUpCurve | `144` | Объект WordArt. |
| TextArchDownCurve | `145` | Объект WordArt. |
| TextCircleCurve | `146` | Объект WordArt. |
| TextButtonCurve | `147` | Объект WordArt. |
| TextArchUpPour | `148` | Объект WordArt. |
| TextArchDownPour | `149` | Объект WordArt. |
| TextCirclePour | `150` | Объект WordArt. |
| TextButtonPour | `151` | Объект WordArt. |
| TextCurveUp | `152` | Объект WordArt. |
| TextCurveDown | `153` | Объект WordArt. |
| TextCascadeUp | `154` | Объект WordArt. |
| TextCascadeDown | `155` | Объект WordArt. |
| TextWave1 | `156` | Объект WordArt. |
| TextWave2 | `157` | Объект WordArt. |
| TextWave3 | `158` | Объект WordArt. |
| TextWave4 | `159` | Объект WordArt. |
| TextInflate | `160` | Объект WordArt. |
| TextDeflate | `161` | Объект WordArt. |
| TextInflateBottom | `162` | Объект WordArt. |
| TextDeflateBottom | `163` | Объект WordArt. |
| TextInflateTop | `164` | Объект WordArt. |
| TextDeflateTop | `165` | Объект WordArt. |
| TextDeflateInflate | `166` | Объект WordArt. |
| TextDeflateInflateDeflate | `167` | Объект WordArt. |
| TextFadeRight | `168` | Объект WordArt. |
| TextFadeLeft | `169` | Объект WordArt. |
| TextFadeUp | `170` | Объект WordArt. |
| TextFadeDown | `171` | Объект WordArt. |
| TextSlantUp | `172` | Объект WordArt. |
| TextSlantDown | `173` | Объект WordArt. |
| TextCanUp | `174` | Объект WordArt. |
| TextCanDown | `175` | Объект WordArt. |
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
| SingleCornerSnipped | `203` | Вырезать прямоугольный объект с одним углом. |
| TopCornersSnipped | `204` | Обрежьте прямоугольник с одинаковым углом. |
| DiagonalCornersSnipped | `205` | Обрежьте прямоугольник по диагонали. |
| TopCornersOneRoundedOneSnipped | `206` | Отрежьте и закруглите прямоугольник с одним углом. |
| SingleCornerRounded | `207` | Прямоугольник со скругленными углами. |
| TopCornersRounded | `208` | Прямоугольник со скругленными углами. |
| DiagonalCornersRounded | `209` | Прямоугольник с круглым диагональным углом. |
| Heptagon | `210` | Семиугольник. |
| Cloud | `211` | Облако. |
| Seal6 | `212` | Шестиконечная звезда. |
| Seal7 | `213` | Семиконечная звезда. |
| Seal10 | `214` | Десятиконечная звезда. |
| Seal12 | `215` | Двенадцатиконечная звезда. |
| SwooshArrow | `216` | Стрелка-галочка. |
| Teardrop | `217` | Слеза. |
| SquareTabs | `218` | Квадратные вкладки. |
| PlaqueTabs | `219` | Пластинчатые вкладки. |
| Pie | `220` | Пирог. |
| WedgePie | `221` | Пирог на танкетке. |
| InverseLine | `222` | Обратная линия. |
| MathPlus | `223` | Математика плюс. |
| MathMinus | `224` | Математика минус. |
| MathMultiply | `225` | Математическое умножение. |
| MathDivide | `226` | Математическое деление. |
| MathEqual | `227` | Математическое равенство. |
| MathNotEqual | `228` | Математика не равна. |
| NonIsoscelesTrapezoid | `229` | Неравнобедренная трапеция. |
| LeftRightCircularArrow | `230` | Круговая стрелка влево-вправо. |
| LeftRightRibbon | `231` | Левая-правая лента. |
| LeftCircularArrow | `232` | Круговая стрелка влево. |
| Frame | `233` | Кадр. |
| HalfFrame | `234` | Половина кадра. |
| Funnel | `235` | Воронка. |
| Gear6 | `236` | Шестизубая шестерня. |
| Gear9 | `237` | Шестерня девятизубая. |
| Decagon | `238` | Десятиугольник. |
| Dodecagon | `239` | Додекагон. |
| DiagonalStripe | `240` | Диагональная полоса. |
| Corner | `241` | Угловой. |
| CornerTabs | `242` | Угловые вкладки. |
| Chord | `243` | Аккорд. |
| ChartPlus | `244` | Диаграмма плюс. |
| ChartStar | `245` | Звезда диаграммы. |
| ChartX | `246` | Таблица X. |
| MinValue | `-2` | Зарезервировано для системного использования. |

### Примеры

Показывает, как вставить фигуру с изображение из локальной файловой системы в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Чтобы правильно идентифицировать типы фигур, вам нужно работать с фигурами как с DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // "Строгое" или "Переходное" соответствие позволяет сохранять форму как DML.
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

Показывает, как Aspose.Words идентифицирует фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Чтобы правильно идентифицировать типы фигур, вам нужно работать с фигурами как с DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // "Строгое" или "Переходное" соответствие позволяет сохранять форму как DML.
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

### Смотрите также

* property [ShapeType](../shapebase/shapetype)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
