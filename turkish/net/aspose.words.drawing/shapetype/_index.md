---
title: ShapeType
second_title: Aspose.Words for .NET API Referansı
description: Microsoft Word belgesindeki şeklin türünü belirtir.
type: docs
weight: 1140
url: /tr/net/aspose.words.drawing/shapetype/
---
## ShapeType enumeration

Microsoft Word belgesindeki şeklin türünü belirtir.

```csharp
public enum ShapeType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Image | `75` | Şekil bir görüntüdür. |
| TextBox | `202` | Şekil bir metin kutusudur. Diğer birçok türdeki şekillerin de içinde metin olabileceğini unutmayın. Bir şeklin metin içermesi için bu tür olması gerekmez. |
| Group | `-1` | Şekil bir grup şeklidir. |
| OleObject | `-2` | Şekil bir OLE nesnesidir. |
| OleControl | `201` | Şekil bir ActiveX denetimidir. |
| NonPrimitive | `0` | Kullanıcı tarafından çizilen ve birden çok parça ve/veya tepe noktasından (eğri, serbest biçim veya karalama) oluşan bir şekil. |
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
| CustomShape | `100` | Bu şekil türü, Microsoft Word'deki standart otomatik şekiller kümesinin parçası olmayan şekiller için ayarlanmış gibi görünüyor. Örneğin, ClipArt. 'den yeni bir otomatik şekil eklerseniz |
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
| TextPlainText | `136` | WordArt nesnesi. |
| TextStop | `137` | WordArt nesnesi. |
| TextTriangle | `138` | WordArt nesnesi. |
| TextTriangleInverted | `139` | WordArt nesnesi. |
| TextChevron | `140` | WordArt nesnesi. |
| TextChevronInverted | `141` | WordArt nesnesi. |
| TextRingInside | `142` | WordArt nesnesi. |
| TextRingOutside | `143` | WordArt nesnesi. |
| TextArchUpCurve | `144` | WordArt nesnesi. |
| TextArchDownCurve | `145` | WordArt nesnesi. |
| TextCircleCurve | `146` | WordArt nesnesi. |
| TextButtonCurve | `147` | WordArt nesnesi. |
| TextArchUpPour | `148` | WordArt nesnesi. |
| TextArchDownPour | `149` | WordArt nesnesi. |
| TextCirclePour | `150` | WordArt nesnesi. |
| TextButtonPour | `151` | WordArt nesnesi. |
| TextCurveUp | `152` | WordArt nesnesi. |
| TextCurveDown | `153` | WordArt nesnesi. |
| TextCascadeUp | `154` | WordArt nesnesi. |
| TextCascadeDown | `155` | WordArt nesnesi. |
| TextWave1 | `156` | WordArt nesnesi. |
| TextWave2 | `157` | WordArt nesnesi. |
| TextWave3 | `158` | WordArt nesnesi. |
| TextWave4 | `159` | WordArt nesnesi. |
| TextInflate | `160` | WordArt nesnesi. |
| TextDeflate | `161` | WordArt nesnesi. |
| TextInflateBottom | `162` | WordArt nesnesi. |
| TextDeflateBottom | `163` | WordArt nesnesi. |
| TextInflateTop | `164` | WordArt nesnesi. |
| TextDeflateTop | `165` | WordArt nesnesi. |
| TextDeflateInflate | `166` | WordArt nesnesi. |
| TextDeflateInflateDeflate | `167` | WordArt nesnesi. |
| TextFadeRight | `168` | WordArt nesnesi. |
| TextFadeLeft | `169` | WordArt nesnesi. |
| TextFadeUp | `170` | WordArt nesnesi. |
| TextFadeDown | `171` | WordArt nesnesi. |
| TextSlantUp | `172` | WordArt nesnesi. |
| TextSlantDown | `173` | WordArt nesnesi. |
| TextCanUp | `174` | WordArt nesnesi. |
| TextCanDown | `175` | WordArt nesnesi. |
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
| SingleCornerSnipped | `203` | Tek köşeli dikdörtgen nesneyi alın. |
| TopCornersSnipped | `204` | Aynı yan köşe dikdörtgenini alın. |
| DiagonalCornersSnipped | `205` | Çapraz köşe dikdörtgenini alın. |
| TopCornersOneRoundedOneSnipped | `206` | Tek köşeli dikdörtgeni alın ve yuvarlayın. |
| SingleCornerRounded | `207` | Yuvarlak tek köşeli dikdörtgen. |
| TopCornersRounded | `208` | Yuvarlak aynı kenar köşe dikdörtgeni. |
| DiagonalCornersRounded | `209` | Yuvarlak köşegen köşeli dikdörtgen. |
| Heptagon | `210` | Heptagon. |
| Cloud | `211` | Bulut. |
| Seal6 | `212` | Altı köşeli yıldız. |
| Seal7 | `213` | Yedi köşeli yıldız. |
| Seal10 | `214` | On köşeli yıldız. |
| Seal12 | `215` | On iki köşeli yıldız. |
| SwooshArrow | `216` | Swoosh oku. |
| Teardrop | `217` | Gözyaşı. |
| SquareTabs | `218` | Kare sekmeler. |
| PlaqueTabs | `219` | Plak sekmeleri. |
| Pie | `220` | Pasta. |
| WedgePie | `221` | Dilimli turta. |
| InverseLine | `222` | Ters çizgi. |
| MathPlus | `223` | Matematik artı. |
| MathMinus | `224` | Matematik eksi. |
| MathMultiply | `225` | Matematik çarpması. |
| MathDivide | `226` | Matematik bölme. |
| MathEqual | `227` | Matematik eşittir. |
| MathNotEqual | `228` | Matematik eşit değil. |
| NonIsoscelesTrapezoid | `229` | İkizkenar olmayan yamuk. |
| LeftRightCircularArrow | `230` | Sol-sağ dairesel ok. |
| LeftRightRibbon | `231` | Sol-sağ şerit. |
| LeftCircularArrow | `232` | Sol dairesel ok. |
| Frame | `233` | Çerçeve. |
| HalfFrame | `234` | Yarım çerçeve. |
| Funnel | `235` | Huni. |
| Gear6 | `236` | Altı dişli dişli. |
| Gear9 | `237` | Dokuz dişli dişli. |
| Decagon | `238` | Decagon. |
| Dodecagon | `239` | Dodecagon. |
| DiagonalStripe | `240` | Çapraz şerit. |
| Corner | `241` | Köşe. |
| CornerTabs | `242` | Köşe sekmeleri. |
| Chord | `243` | Akor. |
| ChartPlus | `244` | Grafik artı. |
| ChartStar | `245` | Harita yıldızı. |
| ChartX | `246` | Grafik X. |
| MinValue | `-2` | Sistem kullanımı için ayrılmıştır. |

### Örnekler

Yerel dosya sisteminden bir görüntüyle bir şeklin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// "Shape" sınıfının genel kurucusu, "ShapeMarkupLanguage.Vml" işaretleme türüyle bir şekil oluşturacaktır.
// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi ilkel olmayan türde bir şekil oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded veya DiagonalCornersRounded,
// lütfen DocumentBuilder.InsertShape'i kullanın.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Aspose.Words'ün şekilleri nasıl tanımladığını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertShape(ShapeType.Heptagon, RelativeHorizontalPosition.Page, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.Cloud, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

builder.InsertShape(ShapeType.MathPlus, RelativeHorizontalPosition.RightMargin, 0,
    RelativeVerticalPosition.Page, 0, 0, 0, WrapType.None);

// Şekil türlerini tanımlamak için şekillerle DML olarak çalışmanız gerekir.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
{
    // "Strict" veya "Transitional" uyumluluğu, şeklin DML olarak kaydedilmesini sağlar.
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

### Ayrıca bakınız

* property [ShapeType](../shapebase/shapetype/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
