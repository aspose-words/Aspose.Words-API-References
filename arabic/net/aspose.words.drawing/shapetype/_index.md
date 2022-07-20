---
title: ShapeType
second_title: Aspose.Words لمراجع .NET API
description: يحدد نوع الشكل في مستند Microsoft Word .
type: docs
weight: 1140
url: /ar/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

يحدد نوع الشكل في مستند Microsoft Word .

```csharp
public enum ShapeType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Image | `75` | الشكل عبارة عن صورة. |
| TextBox | `202` | الشكل عبارة عن مربع نص. لاحظ أن الأشكال من العديد من الأنواع الأخرى يمكن أن تحتوي أيضًا على نص بداخلها أيضًا ._ x000d_ لا يجب أن يحتوي الشكل على هذا النوع ليحتوي على نص. |
| Group | `-1` | الشكل عبارة عن شكل مجموعة. |
| OleObject | `-2` | الشكل عبارة عن كائن OLE . |
| OleControl | `201` | الشكل عبارة عن عنصر تحكم ActiveX. |
| NonPrimitive | `0` | شكل رسمه المستخدم ويتكون من عدة مقاطع و / أو رؤوس (منحنى أو شكل حر أو خربشة). |
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
| CustomShape | `100` | يبدو أن نوع الشكل هذا قد تم تعيينه للأشكال التي ليست جزءًا من المجموعة القياسية لـ_ x000d_ الأشكال التلقائية في Microsoft Word. على سبيل المثال ، إذا قمت بإدراج شكل تلقائي جديد من ClipArt. |
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
| TextPlainText | `136` | كائن WordArt . |
| TextStop | `137` | كائن WordArt . |
| TextTriangle | `138` | كائن WordArt . |
| TextTriangleInverted | `139` | كائن WordArt . |
| TextChevron | `140` | كائن WordArt . |
| TextChevronInverted | `141` | كائن WordArt . |
| TextRingInside | `142` | كائن WordArt . |
| TextRingOutside | `143` | كائن WordArt . |
| TextArchUpCurve | `144` | كائن WordArt . |
| TextArchDownCurve | `145` | كائن WordArt . |
| TextCircleCurve | `146` | كائن WordArt . |
| TextButtonCurve | `147` | كائن WordArt . |
| TextArchUpPour | `148` | كائن WordArt . |
| TextArchDownPour | `149` | كائن WordArt . |
| TextCirclePour | `150` | كائن WordArt . |
| TextButtonPour | `151` | كائن WordArt . |
| TextCurveUp | `152` | كائن WordArt . |
| TextCurveDown | `153` | كائن WordArt . |
| TextCascadeUp | `154` | كائن WordArt . |
| TextCascadeDown | `155` | كائن WordArt . |
| TextWave1 | `156` | كائن WordArt . |
| TextWave2 | `157` | كائن WordArt . |
| TextWave3 | `158` | كائن WordArt . |
| TextWave4 | `159` | كائن WordArt . |
| TextInflate | `160` | كائن WordArt . |
| TextDeflate | `161` | كائن WordArt . |
| TextInflateBottom | `162` | كائن WordArt . |
| TextDeflateBottom | `163` | كائن WordArt . |
| TextInflateTop | `164` | كائن WordArt . |
| TextDeflateTop | `165` | كائن WordArt . |
| TextDeflateInflate | `166` | كائن WordArt . |
| TextDeflateInflateDeflate | `167` | كائن WordArt . |
| TextFadeRight | `168` | كائن WordArt . |
| TextFadeLeft | `169` | كائن WordArt . |
| TextFadeUp | `170` | كائن WordArt . |
| TextFadeDown | `171` | كائن WordArt . |
| TextSlantUp | `172` | كائن WordArt . |
| TextSlantDown | `173` | كائن WordArt . |
| TextCanUp | `174` | كائن WordArt . |
| TextCanDown | `175` | كائن WordArt . |
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
| SingleCornerSnipped | `203` | قص كائن مستطيل ذو زاوية واحدة ._ x000d_ |
| TopCornersSnipped | `204` | قص مستطيل زاوية الجانب نفسه. |
| DiagonalCornersSnipped | `205` | مستطيل ذو زاوية قطرية قص ._ x000d_ |
| TopCornersOneRoundedOneSnipped | `206` | مستطيل ذو زاوية واحدة مقتصة ودائرية ._ x000d_ |
| SingleCornerRounded | `207` | مستطيل ذو زاوية واحدة مستديرة . |
| TopCornersRounded | `208` | مستطيل ذو زاوية جانبية مستديرة. |
| DiagonalCornersRounded | `209` | مستطيل ذو زاوية قطرية دائرية ._ x000d_ |
| Heptagon | `210` | سباعي . |
| Cloud | `211` | سحابة . |
| Seal6 | `212` | نجمة سداسية . |
| Seal7 | `213` | نجمة ذات سبع نقاط . |
| Seal10 | `214` | نجمة ذات عشر نقاط . |
| Seal12 | `215` | نجمة اثني عشر ._ x000d_ |
| SwooshArrow | `216` | سهم Swoosh . |
| Teardrop | `217` | دمعة . |
| SquareTabs | `218` | علامات تبويب مربعة. x000d_ |
| PlaqueTabs | `219` | علامات تبويب البلاك. _ x000d_ |
| Pie | `220` | فطيرة . |
| WedgePie | `221` | فطيرة الوتد ._ x000d_ |
| InverseLine | `222` | خط معكوس . |
| MathPlus | `223` | الرياضيات زائد . |
| MathMinus | `224` | رياضيات ناقص . |
| MathMultiply | `225` | ضرب الرياضيات . |
| MathDivide | `226` | قسم الرياضيات ._ x000d_ |
| MathEqual | `227` | رياضيات متساوية . |
| MathNotEqual | `228` | الرياضيات لا تساوي. |
| NonIsoscelesTrapezoid | `229` | شبه منحرف غير متساوي الساقين. |
| LeftRightCircularArrow | `230` | سهم دائري من اليسار إلى اليمين. |
| LeftRightRibbon | `231` | شريط من اليسار إلى اليمين ._ x000d_ |
| LeftCircularArrow | `232` | سهم دائري أيسر ._ x000d_ |
| Frame | `233` | إطار . |
| HalfFrame | `234` | نصف إطار . |
| Funnel | `235` | قمع . |
| Gear6 | `236` | معدات بستة أسنان . |
| Gear9 | `237` | معدات تسع أسنان . |
| Decagon | `238` | عشري . |
| Dodecagon | `239` | Dodecagon. |
| DiagonalStripe | `240` | شريط قطري ._ x000d_ |
| Corner | `241` | ركن . |
| CornerTabs | `242` | علامات تبويب الزاوية. _ x000d_ |
| Chord | `243` | وتر. _ x000d_ |
| ChartPlus | `244` | مخطط زائد . |
| ChartStar | `245` | نجمة المخطط ._ x000d_ |
| ChartX | `246` | الرسم البياني X. |
| MinValue | `-2` | محجوزة لاستخدام النظام ._ x000d_ |

### أمثلة

يوضح كيفية إدراج شكل بصورة من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();

// سيقوم المُنشئ العام لفئة "الشكل" بإنشاء شكل بنوع علامة "ShapeMarkupLanguage.Vml".
// إذا كنت بحاجة إلى إنشاء شكل من نوع غير بدائي ، مثل SingleCornerSnipped و TopCornersSnipped و DiagonalCornersSnipped ،
// TopCornersOneRoundedOneSnipped أو SingleCornerRounded أو TopCornersRounded أو DiagonalCornersRounded
// الرجاء استخدام DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

يوضح كيف تتعرف Aspose. Words على الأشكال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// لتصحيح تحديد أنواع الأشكال ، تحتاج إلى العمل مع الأشكال مثل DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    يسمح التوافق "الصارم" أو "الانتقالي" بحفظ الشكل على هيئة DML.
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

### أنظر أيضا

* property [ShapeType](../shapebase/shapetype)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
