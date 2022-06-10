---
title: ShapeType
second_title: Aspose.Words for .NET API 参考
description: 指定 Microsoft Word 文档中的形状类型
type: docs
weight: 1120
url: /zh/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

指定 Microsoft Word 文档中的形状类型。

```csharp
public enum ShapeType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Image | `75` | 形状是图像。 |
| TextBox | `202` | 形状是一个文本框。请注意，许多其他类型的形状也可以在其中包含文本。 形状不必具有此类型即可包含文本。 |
| Group | `-1` | 形状是组形状。 |
| OleObject | `-2` | 形状是一个 OLE 对象。 |
| OleControl | `201` | 形状是一个 ActiveX 控件。 |
| NonPrimitive | `0` | 由用户绘制并由多个段和/或顶点（曲线、自由形式或涂鸦）组成的形状。 |
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
| CustomShape | `100` | 此形状类型似乎是为不属于 Microsoft Word 中 自动形状的标准集的形状设置的。例如，如果您从剪贴画插入一个新的自动形状。 |
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
| TextPlainText | `136` | 艺术字对象。 |
| TextStop | `137` | 艺术字对象。 |
| TextTriangle | `138` | 艺术字对象。 |
| TextTriangleInverted | `139` | 艺术字对象。 |
| TextChevron | `140` | 艺术字对象。 |
| TextChevronInverted | `141` | 艺术字对象。 |
| TextRingInside | `142` | 艺术字对象。 |
| TextRingOutside | `143` | 艺术字对象。 |
| TextArchUpCurve | `144` | 艺术字对象。 |
| TextArchDownCurve | `145` | 艺术字对象。 |
| TextCircleCurve | `146` | 艺术字对象。 |
| TextButtonCurve | `147` | 艺术字对象。 |
| TextArchUpPour | `148` | 艺术字对象。 |
| TextArchDownPour | `149` | 艺术字对象。 |
| TextCirclePour | `150` | 艺术字对象。 |
| TextButtonPour | `151` | 艺术字对象。 |
| TextCurveUp | `152` | 艺术字对象。 |
| TextCurveDown | `153` | 艺术字对象。 |
| TextCascadeUp | `154` | 艺术字对象。 |
| TextCascadeDown | `155` | 艺术字对象。 |
| TextWave1 | `156` | 艺术字对象。 |
| TextWave2 | `157` | 艺术字对象。 |
| TextWave3 | `158` | 艺术字对象。 |
| TextWave4 | `159` | 艺术字对象。 |
| TextInflate | `160` | 艺术字对象。 |
| TextDeflate | `161` | 艺术字对象。 |
| TextInflateBottom | `162` | 艺术字对象。 |
| TextDeflateBottom | `163` | 艺术字对象。 |
| TextInflateTop | `164` | 艺术字对象。 |
| TextDeflateTop | `165` | 艺术字对象。 |
| TextDeflateInflate | `166` | 艺术字对象。 |
| TextDeflateInflateDeflate | `167` | 艺术字对象。 |
| TextFadeRight | `168` | 艺术字对象。 |
| TextFadeLeft | `169` | 艺术字对象。 |
| TextFadeUp | `170` | 艺术字对象。 |
| TextFadeDown | `171` | 艺术字对象。 |
| TextSlantUp | `172` | 艺术字对象。 |
| TextSlantDown | `173` | 艺术字对象。 |
| TextCanUp | `174` | 艺术字对象。 |
| TextCanDown | `175` | 艺术字对象。 |
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
| SingleCornerSnipped | `203` | 剪断单角矩形对象。 |
| TopCornersSnipped | `204` | 剪断相同的边角矩形。 |
| DiagonalCornersSnipped | `205` | 剪断对角矩形。 |
| TopCornersOneRoundedOneSnipped | `206` | 剪切和圆化单角矩形。 |
| SingleCornerRounded | `207` | 圆形单角矩形。 |
| TopCornersRounded | `208` | 圆同边角矩形。 |
| DiagonalCornersRounded | `209` | 圆形对角矩形。 |
| Heptagon | `210` | 七边形。 |
| Cloud | `211` | 云。 |
| Seal6 | `212` | 六角星。 |
| Seal7 | `213` | 七角星。 |
| Seal10 | `214` | 十角星。 |
| Seal12 | `215` | 十二角星。 |
| SwooshArrow | `216` | 旋风箭头。 |
| Teardrop | `217` | 泪珠。 |
| SquareTabs | `218` | 方形制表符。 |
| PlaqueTabs | `219` | 斑块标签。 |
| Pie | `220` | 馅饼。 |
| WedgePie | `221` | 楔形派。 |
| InverseLine | `222` | 反转线。 |
| MathPlus | `223` | 数学加。 |
| MathMinus | `224` | 数学减号。 |
| MathMultiply | `225` | 数学乘法。 |
| MathDivide | `226` | 数学除法。 |
| MathEqual | `227` | 数学相等。 |
| MathNotEqual | `228` | 数学不相等。 |
| NonIsoscelesTrapezoid | `229` | 非等腰梯形。 |
| LeftRightCircularArrow | `230` | 左右圆形箭头。 |
| LeftRightRibbon | `231` | 左右色带。 |
| LeftCircularArrow | `232` | 左圆形箭头。 |
| Frame | `233` | 帧。 |
| HalfFrame | `234` | 半帧。 |
| Funnel | `235` | 漏斗。 |
| Gear6 | `236` | 六齿齿轮。 |
| Gear9 | `237` | 九齿齿轮。 |
| Decagon | `238` | 十边形。 |
| Dodecagon | `239` | 十二边形。 |
| DiagonalStripe | `240` | 斜条纹。 |
| Corner | `241` | 角。 |
| CornerTabs | `242` | 角落标签。 |
| Chord | `243` | 和弦。 |
| ChartPlus | `244` | 图表加。 |
| ChartStar | `245` | 图表星。 |
| ChartX | `246` | 图表 X. |
| MinValue | `-2` | 保留给系统使用。 |

### 例子

显示如何插入带有图像从本地文件系统转换为文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// 要正确识别形状类型，您需要将形状用作 DML。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // “严格”或“过渡”合规性允许将形状保存为 DML。
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

显示 Aspose.Words 如何识别形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// 要正确识别形状类型，您需要将形状用作 DML。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // “严格”或“过渡”合规性允许将形状保存为 DML。
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

### 也可以看看

* property [ShapeType](../shapebase/shapetype)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
