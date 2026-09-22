---
title: "Aspose::Words::Drawing::ShapeType enum"
linktitle: "ShapeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeType enum. C++'da bir Microsoft Word belgesindeki şekil türünü belirtir."
type: docs
weight: 38000
url: /tr/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


Microsoft Word belgesindeki şeklin tipini belirtir.

```cpp
enum class ShapeType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Image | 75 | Şekil bir görüntüdür. |
| MetinKutusu | 202 | Şekil bir metin kutusudur. Diğer birçok şekil türünün de içinde metin olabileceğini unutmayın. Bir şeklin metin içerebilmesi için bu tipe sahip olması gerekmez. |
| Group | -1 | Şekil bir grup şekildir. |
| OleObject | -2 | Şekil bir OLE nesnesidir. Bu türdeki şekilleri belgede oluşturamazsınız. |
| OleControl | 201 | Şekil bir ActiveX denetimidir. Bu türdeki şekilleri belgede oluşturamazsınız. |
| NonPrimitive | 0 | Kullanıcı tarafından çizilen ve birden fazla segment ve/veya köşeden (eğri, serbest biçim veya karalama) oluşan bir şekil. Bu türdeki şekilleri belgede oluşturamazsınız. |
| Rectangle | 1 | Dikdörtgen. |
| RoundRectangle | 2 | Yuvarlak köşeli dikdörtgen. |
| Ellipse | 3 | Elips. |
| Diamond | 4 | Karo. |
| Triangle | 5 | Üçgen. |
| RightTriangle | 6 | Dik üçgen. |
| Parallelogram | 7 | Paralelkenar. |
| Trapezoid | 8 | Trapez. |
| Hexagon | 9 | Altıgen. |
| Octagon | 10 | Sekizgen. |
| Artı | 11 | Artı. |
| Yıldız | 12 | Yıldız. |
| Ok | 13 | Ok. |
| KalınOk | 14 | Kalın ok. |
| EvPlakası | 15 | Ev plakası. |
| Küp | 16 | Küp. |
| Balon | 17 | Balon. |
| Mühür | 18 | Mühür. |
| Yay | 19 | Yay. |
| Çizgi | 20 | Çizgi. |
| Plak | 21 | Plak. |
| Kutu | 22 | Kutu. |
| Donut | 23 | Donut. |
| TextSimple | 24 | Basit metin. |
| TextOctagon | 25 | Sekizgen metin. |
| TextHexagon | 26 | Altıgen metin. |
| TextCurve | 27 | Eğri metin. |
| TextWave | 28 | Dalga metin. |
| TextRing | 29 | Halka metin. |
| TextOnCurve | 30 | Eğri üzerindeki metin. |
| TextOnRing | 31 | Halka üzerindeki metin. |
| StraightConnector1 | 32 | Düz bağlayıcı şekli. |
| BentConnector2 | 33 | İki segmentli bükülmüş bağlayıcı şekli. |
| BentConnector3 | 34 | Üç segmentli bükülmüş bağlayıcı şekli. |
| BentConnector4 | 35 | Dört segmentli bükülmüş bağlayıcı şekli. |
| BentConnector5 | 36 | Beş segmentli bükülmüş bağlayıcı şekli. |
| CurvedConnector2 | 37 | İki segmentli kavisli bağlayıcı şekli. |
| CurvedConnector3 | 38 | Üç segmentli kavisli bağlayıcı şekli. |
| CurvedConnector4 | 39 | Dört segmentli kavisli bağlayıcı şekli. |
| CurvedConnector5 | 40 | Beş segmentli kavisli bağlayıcı şekli. |
| Callout1 | 41 | Bir oklu açıklama şekli. |
| Callout2 | 42 | İki oklu açıklama şekli. |
| Callout3 | 43 | Üç oklu açıklama şekli. |
| AccentCallout1 | 44 | Bir oklu vurgu açıklama şekli. |
| AccentCallout2 | 45 | İki oklu vurgu açıklama şekli. |
| AccentCallout3 | 46 | Üç oklu vurgu açıklama şekli. |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) açıklama 1. |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) açıklama 2. |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) açıklama 3. |
| AccentBorderCallout1 | 50 | Vurgu kenarlıklı açıklama 1. |
| AccentBorderCallout2 | 51 | Vurgu kenarlıklı açıklama 2. |
| AccentBorderCallout3 | 52 | Vurgu kenarlıklı açıklama 3. |
| Şerit | 53 | Şerit. |
| Ribbon2 | 54 | Şerit 2. |
| Chevron | 55 | Chevron. |
| Beşgen | 56 | Beşgen. |
| NoSmoking | 57 | Sigara içilmez. |
| Seal8 | 58 | Sekiz köşeli yıldız. |
| Seal16 | 59 | 16 köşeli yıldız. |
| Seal32 | 60 | 32 köşeli yıldız. |
| WedgeRectCallout | 61 | Kama dikdörtgen açıklama. |
| WedgeRRectCallout | 62 | Wedge R dikdörtgen çağrı balonu. |
| WedgeEllipseCallout | 63 | Wedge elips çağrı balonu. |
| Wave | 64 | Dalga. |
| FoldedCorner | 65 | Katlanmış köşe. |
| LeftArrow | 66 | Sol ok. |
| DownArrow | 67 | Aşağı ok. |
| UpArrow | 68 | Yukarı ok. |
| LeftRightArrow | 69 | Sol sağ ok. |
| UpDownArrow | 70 | Yukarı aşağı ok. |
| IrregularSeal1 | 71 | Düzensiz mühür 1. |
| IrregularSeal2 | 72 | Düzensiz mühür 2. |
| LightningBolt | 73 | Şimşek çubuğu. |
| Heart | 74 | Kalp. |
| QuadArrow | 76 | Dörtlü ok. |
| SolOkAçıklama | 77 | Sol ok açıklaması. |
| SağOkAçıklama | 78 | Sağ ok açıklaması. |
| YukarıOkAçıklama | 79 | Yukarı ok açıklaması. |
| AşağıOkAçıklama | 80 | Aşağı ok açıklaması. |
| SolSağOkAçıklama | 81 | Sol sağ ok açıklaması. |
| YukarıAşağıOkAçıklama | 82 | Yukarı aşağı ok açıklaması. |
| DörtlüOkAçıklama | 83 | Dörtlü ok açıklaması. |
| Eğim | 84 | Eğim. |
| SolParantez | 85 | Sol parantez. |
| SağParantez | 86 | Sağ parantez. |
| SolKümeParantez | 87 | Sol küme parantez. |
| SağKümeParantez | 88 | Sağ küme parantez. |
| LeftUpArrow | 89 | Sol yukarı ok. |
| BentUpArrow | 90 | Bükülmüş yukarı ok. |
| BentArrow | 91 | Bükülmüş ok. |
| Seal24 | 92 | 24 uçlu yıldız. |
| StripedRightArrow | 93 | Şeritli sağ ok. |
| NotchedRightArrow | 94 | Çentikli sağ ok. |
| BlockArc | 95 | Blok yay. |
| SmileyFace | 96 | Gülümseyen yüz. |
| VerticalScroll | 97 | Dikey kaydırma. |
| HorizontalScroll | 98 | Yatay kaydırma. |
| CircularArrow | 99 | Dairesel ok. |
| CustomShape | 100 | Bu şekil türü, Microsoft Word'deki otomatik şekillerin standart setine dahil olmayan şekiller için ayarlanmış gibi görünüyor. Örneğin, ClipArt'tan yeni bir otomatik şekil eklediğinizde. Bu türde şekiller belge içinde oluşturulamaz. |
| UturnArrow | 101 | U dönüş oku. |
| CurvedRightArrow | 102 | Kavisli sağ ok. |
| CurvedLeftArrow | 103 | Kavisli sol ok. |
| CurvedUpArrow | 104 | Kavisli yukarı ok. |
| CurvedDownArrow | 105 | Kavisli aşağı ok. |
| CloudCallout | 106 | Bulut açıklama balonu. |
| EllipseRibbon | 107 | Elips şerit. |
| EllipseRibbon2 | 108 | Elips şerit 2. |
| FlowChartProcess | 109 | Akış şeması işlemi. |
| FlowChartDecision | 110 | Akış şeması kararı. |
| FlowChartInputOutput | 111 | Akış şeması giriş çıkış. |
| FlowChartPredefinedProcess | 112 | Akış şeması önceden tanımlı işlem. |
| FlowChartInternalStorage | 113 | Akış diyagramı dahili depolama. |
| FlowChartDocument | 114 | Akış diyagramı belgesi. |
| FlowChartMultidocument | 115 | Akış diyagramı çoklu belge. |
| FlowChartTerminator | 116 | Akış diyagramı sonlandırıcı. |
| FlowChartPreparation | 117 | Akış diyagramı hazırlık. |
| FlowChartManualInput | 118 | Akış diyagramı manuel girdi. |
| FlowChartManualOperation | 119 | Akış diyagramı manuel işlem. |
| FlowChartConnector | 120 | Akış diyagramı bağlayıcı. |
| FlowChartPunchedCard | 121 | Akış diyagramı delikli kart. |
| FlowChartPunchedTape | 122 | Akış diyagramı delikli bant. |
| FlowChartSummingJunction | 123 | Akış diyagramı toplama birleşimi. |
| FlowChartOr | 124 | Akış diyagramı veya. |
| FlowChartCollate | 125 | Akış diyagramı birleştir. |
| FlowChartSort | 126 | Akış diyagramı sıralama. |
| FlowChartExtract | 127 | Akış diyagramı çıkarma. |
| FlowChartMerge | 128 | Akış diyagramı birleştirme. |
| FlowChartOfflineStorage | 129 | Akış diyagramı çevrim dışı depolama. |
| FlowChartOnlineStorage | 130 | Akış diyagramı çevrim içi depolama. |
| FlowChartMagneticTape | 131 | Akış diyagramı manyetik bandı. |
| FlowChartMagneticDisk | 132 | Akış diyagramı manyetik disk. |
| FlowChartMagneticDrum | 133 | Akış diyagramı manyetik tambur. |
| FlowChartDisplay | 134 | Akış diyagramı görüntüleme. |
| FlowChartDelay | 135 | Akış diyagramı gecikme. |
| TextPlainText | 136 | Düz metin, WordArt nesnesi. |
| TextStop | 137 | Durdur, WordArt nesnesi. |
| TextTriangle | 138 | Üçgen, WordArt nesnesi. |
| TextTriangleInverted | 139 | Ters üçgen, WordArt nesnesi. |
| TextChevron | 140 | Chevron, WordArt nesnesi. |
| TextChevronInverted | 141 | Ters chevron, WordArt nesnesi. |
| TextRingInside | 142 | İç halka, WordArt nesnesi. |
| TextRingOutside | 143 | Dış halka, WordArt nesnesi. |
| TextArchUpCurve | 144 | Yukarı kavisli kemer, WordArt nesnesi. |
| TextArchDownCurve | 145 | Aşağı kavisli kemer, WordArt nesnesi. |
| TextCircleCurve | 146 | Daire eğrisi, WordArt nesnesi. |
| TextButtonCurve | 147 | Düğme eğrisi, WordArt nesnesi. |
| TextArchUpPour | 148 | Yukarı dökme kemer, WordArt nesnesi. |
| TextArchDownPour | 149 | Aşağı dökme kemer, WordArt nesnesi. |
| TextCirclePour | 150 | Daire dökme, WordArt nesnesi. |
| TextButtonPour | 151 | Düğme dökme, WordArt nesnesi. |
| TextCurveUp | 152 | Eğri yukarı, WordArt nesnesi. |
| TextCurveDown | 153 | Eğri aşağı, WordArt nesnesi. |
| TextCascadeUp | 154 | Kademeli yukarı, WordArt nesnesi. |
| TextCascadeDown | 155 | Kademeli aşağı, WordArt nesnesi. |
| TextWave1 | 156 | Dalga 1, WordArt nesnesi. |
| TextWave2 | 157 | Dalga 2, WordArt nesnesi. |
| TextWave3 | 158 | Dalga 3, WordArt nesnesi. |
| TextWave4 | 159 | Dalga 4, WordArt nesnesi. |
| TextInflate | 160 | Şişir, WordArt nesnesi. |
| TextDeflate | 161 | Sönük, WordArt nesnesi. |
| TextInflateBottom | 162 | Altı şişir, WordArt nesnesi. |
| TextDeflateBottom | 163 | Altı küçült, WordArt object. |
| TextInflateTop | 164 | Üstü büyüt, WordArt object. |
| TextDeflateTop | 165 | Üstü küçült, WordArt object. |
| TextDeflateInflate | 166 | Küçült büyüt, WordArt object. |
| TextDeflateInflateDeflate | 167 | Küçült büyüt küçült, WordArt object. |
| TextFadeRight | 168 | Sağa soluklaş, WordArt object. |
| TextFadeLeft | 169 | Sola soluklaş, WordArt object. |
| TextFadeUp | 170 | Yukarı soluklaş, WordArt object. |
| TextFadeDown | 171 | Aşağı soluklaş, WordArt object. |
| TextSlantUp | 172 | Yukarı eğ, WordArt object. |
| TextSlantDown | 173 | Aşağı eğ, WordArt object. |
| TextCanUp | 174 | Can yukarı, WordArt object. |
| TextCanDown | 175 | Can aşağı, WordArt object. |
| FlowChartAlternateProcess | 176 | Akış diyagramı alternatif süreç. |
| FlowChartOffpageConnector | 177 | Akış diyagramı sayfa dışı bağlayıcı. |
| Callout90 | 178 | Balon 90. |
| AccentCallout90 | 179 | Vurgu balon 90. |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) balon 90. |
| AccentBorderCallout90 | 181 | Vurgu kenarlık balon 90. |
| LeftRightUpArrow | 182 | Sol sağ yukarı ok. |
| Sun | 183 | Güneş. |
| Moon | 184 | Ay. |
| BracketPair | 185 | Parantez çifti. |
| BracePair | 186 | Süslü parantez çifti. |
| Seal4 | 187 | Dört noktalı yıldız. |
| DoubleWave | 188 | Çift dalga. |
| ActionButtonBlank | 189 | Eylem düğmesi boş. |
| ActionButtonHome | 190 | Eylem düğmesi ana sayfa. |
| ActionButtonHelp | 191 | Eylem düğmesi yardım. |
| ActionButtonInformation | 192 | Eylem düğmesi bilgi. |
| ActionButtonForwardNext | 193 | Eylem düğmesi ileri sonraki. |
| ActionButtonBackPrevious | 194 | Eylem düğmesi geri önceki. |
| ActionButtonEnd | 195 | Eylem düğmesi son. |
| ActionButtonBeginning | 196 | Eylem düğmesi başlangıç. |
| ActionButtonReturn | 197 | Eylem düğmesi geri dön. |
| ActionButtonDocument | 198 | Eylem düğmesi belge. |
| ActionButtonSound | 199 | Eylem düğmesi ses. |
| ActionButtonMovie | 200 | Eylem düğmesi film. |
| SingleCornerSnipped | 203 | Tek köşeli dikdörtgen nesnesini kırp. |
| ÜstKöşelerKırpıldı | 204 | Aynı taraftaki köşe dikdörtgenini kırp. |
| KöşegenKöşelerKırpıldı | 205 | Köşegen köşe dikdörtgenini kırp. |
| ÜstKöşelerBirYuvarlatılmışBirKırpıldı | 206 | Tek köşe dikdörtgenini kırp ve yuvarlat. |
| TekKöşeYuvarlatıldı | 207 | Tek köşe dikdörtgenini yuvarlat. |
| ÜstKöşelerYuvarlatıldı | 208 | Aynı taraftaki köşe dikdörtgenini yuvarlat. |
| KöşegenKöşelerYuvarlatıldı | 209 | Köşegen köşe dikdörtgenini yuvarlat. |
| Yedigen | 210 | Yedigen. |
| Bulut | 211 | Bulut. |
| Mühür6 | 212 | Altı köşeli yıldız. |
| Mühür7 | 213 | Yedi köşeli yıldız. |
| Mühür10 | 214 | On köşeli yıldız. |
| Mühür12 | 215 | On iki köşeli yıldız. |
| SwooshOk | 216 | Swoosh oku. |
| Gözyaşı damlası | 217 | Gözyaşı damlası. |
| SquareTabs | 218 | Kare sekmeler. |
| PlaqueTabs | 219 | Plak sekmeler. |
| Pasta | 220 | Pasta. |
| WedgePie | 221 | Dil pasta. |
| InverseLine | 222 | Ters çizgi. |
| MathPlus | 223 | [Math](../../aspose.words.math/) artı. |
| MathMinus | 224 | [Math](../../aspose.words.math/) eksi. |
| MathMultiply | 225 | [Math](../../aspose.words.math/) çarpma. |
| MathDivide | 226 | [Math](../../aspose.words.math/) bölme. |
| MathEqual | 227 | [Math](../../aspose.words.math/) eşit. |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) eşit değil. |
| NonIsoscelesTrapezoid | 229 | İzosenk olmayan yamuk. |
| LeftRightCircularArrow | 230 | Sol-sağ dairesel ok. |
| LeftRightRibbon | 231 | Sol-sağ kurdele. |
| SolDaireselOk | 232 | Sol dairesel ok. |
| Çerçeve | 233 | Çerçeve. |
| YarımÇerçeve | 234 | Yarım çerçeve. |
| Huni | 235 | Huni. |
| 6Dişli | 236 | Altı dişli dişli çark. |
| 9Dişli | 237 | Dokuz dişli dişli çark. |
| Onkenar | 238 | Onkenar. |
| Onikidik | 239 | Onikidik. |
| DiyagonalŞerit | 240 | Diyagonal şerit. |
| Köşe | 241 | Köşe. |
| KöşeSekmeleri | 242 | Köşe sekmeleri. |
| Kiriş | 243 | Kiriş. |
| GrafikPlus | 244 | Grafik plus. |
| ChartStar | 245 | Grafik yıldızı. |
| ChartX | 246 | Grafik X. |
| MinValue | n/a | Sistem kullanımı için ayrılmıştır. |


## Örnekler



Yerel dosya sisteminden bir görüntü içeren şeklin bir belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// \"Shape\" sınıfının genel yapıcı yöntemi, \"ShapeMarkupLanguage.Vml\" işaretleme türüyle bir şekil oluşturur.
// Eğer SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi ilkel olmayan bir türde şekil oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, veya DiagonalCornersRounded,
// lütfen DocumentBuilder.InsertShape yöntemini kullanın.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Aspose.Words'in şekilleri nasıl tanımladığını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// Şekil türlerini doğru şekilde tanımlamak için şekillerle DML olarak çalışmanız gerekir.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// \"Strict\" veya \"Transitional\" uyumluluğu, şeklin DML olarak kaydedilmesini sağlar.
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
