---
title: "ShapeType"
linktitle: "ShapeType"
second_title: "Aspose.Words Java için"
description: "Java'da bir Microsoft Word belgesindeki şekil türünü belirtir."
type: docs
weight: 618
url: /tr/java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

Microsoft Word belgesindeki şeklin türünü belirtir.

 **Examples:** 

Yerel dosya sisteminden bir görüntü ile şekil eklemeyi belgeye nasıl yapacağınızı gösterir.

```

 Document doc = new Document();

 // The "Shape" class's public constructor will create a shape with "ShapeMarkupLanguage.Vml" markup type.
 // If you need to create a shape of a non-primitive type, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
 // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
 // please use DocumentBuilder.InsertShape.
 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.FromFile.docx");
 
```

Aspose.Words'un şekilleri nasıl tanımladığını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertShape(ShapeType.HEPTAGON, RelativeHorizontalPosition.PAGE, 0.0,
         RelativeVerticalPosition.PAGE, 0.0, 0.0, 0.0, WrapType.NONE);

 builder.insertShape(ShapeType.CLOUD, RelativeHorizontalPosition.RIGHT_MARGIN, 0.0,
         RelativeVerticalPosition.PAGE, 0.0, 0.0, 0.0, WrapType.NONE);

 builder.insertShape(ShapeType.MATH_PLUS, RelativeHorizontalPosition.RIGHT_MARGIN, 0.0,
         RelativeVerticalPosition.PAGE, 0.0, 0.0, 0.0, WrapType.NONE);

 // To correct identify shape types you need to work with shapes as DML.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.DOCX);
 {
     // "Strict" or "Transitional" compliance allows to save shape as DML.
     saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_TRANSITIONAL);
 }

 doc.save(getArtifactsDir() + "Shape.ShapeTypes.docx", saveOptions);
 doc = new Document(getArtifactsDir() + "Shape.ShapeTypes.docx");

 List shapes = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 for (Shape shape : shapes)
 {
     System.out.println(shape.getShapeType());
 }
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Vurgu kenarlık açıklama 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Vurgu kenarlık açıklama 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Vurgu kenarlık açıklama 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | Vurgu kenarlık açıklama 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Bir oklu vurgu açıklama şekli. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | İki oklu vurgu açıklama şekli. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Üç oklu vurgu açıklama şekli. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | Vurgu açıklama 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Geri önceki eylem düğmesi. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Başlangıç eylem düğmesi. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Boş eylem düğmesi. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Belge eylem düğmesi. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Son eylem düğmesi. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | İleri sonraki eylem düğmesi. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Eylem düğmesi yardım. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Eylem düğmesi ana sayfa. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Eylem düğmesi bilgi. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Eylem düğmesi film. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Eylem düğmesi geri. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Eylem düğmesi ses. |
| [ARC](#ARC) | Yay. |
| [ARROW](#ARROW) | Ok. |
| [BALLOON](#BALLOON) | Balon. |
| [BENT_ARROW](#BENT-ARROW) | Bükülmüş ok. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | İki segmentli bükülmüş bağlayıcı şekli. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Üç segmentli bükülmüş bağlayıcı şekli. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Dört segmentli bükülmüş bağlayıcı şekli. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Beş segmentli bükülmüş bağlayıcı şekli. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Bükülmüş yukarı ok. |
| [BEVEL](#BEVEL) | Eğim. |
| [BLOCK_ARC](#BLOCK-ARC) | Blok yay. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Kenarlık açıklama 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Kenarlık açıklama 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Kenarlık açıklama 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | Kenarlık açıklama 90. |
| [BRACE_PAIR](#BRACE-PAIR) | Ayraç çifti |
| [BRACKET_PAIR](#BRACKET-PAIR) | Köşeli parantez çifti. |
| [CALLOUT_1](#CALLOUT-1) | Tek oklu açıklama şekli. |
| [CALLOUT_2](#CALLOUT-2) | İki oklu açıklama şekli. |
| [CALLOUT_3](#CALLOUT-3) | Üç oklu açıklama şekli. |
| [CALLOUT_90](#CALLOUT-90) | Açıklama 90. |
| [CAN](#CAN) | Kutu. |
| [CHART_PLUS](#CHART-PLUS) | Grafik artı. |
| [CHART_STAR](#CHART-STAR) | Grafik yıldız. |
| [CHART_X](#CHART-X) | Grafik X. |
| [CHEVRON](#CHEVRON) | Şerit. |
| [CHORD](#CHORD) | Kiriş. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Dairesel ok. |
| [CLOUD](#CLOUD) | Bulut. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Bulut açıklama. |
| [CORNER](#CORNER) | Köşe. |
| [CORNER_TABS](#CORNER-TABS) | Köşe sekmeleri. |
| [CUBE](#CUBE) | Küp. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | İki segmentli kavisli bağlayıcı şekli. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Üç segmentli kavisli bağlayıcı şekli. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Dört segmentli kavisli bağlayıcı şekli. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Beş segmentli kavisli bağlayıcı şekli. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Eğri aşağı ok. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Eğri sola ok. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Eğri sağa ok. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Kavisli yukarı ok |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | Bu şekil türü, Microsoft Word'deki otomatik şekillerin standart setine dahil olmayan şekiller için ayarlanmış gibi görünüyor. |
| [DECAGON](#DECAGON) | Ongen. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Yuvarlak köşeli diyagonal dikdörtgen. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Kırpılmış diyagonal köşe dikdörtgeni. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Diyagonal şerit. |
| [DIAMOND](#DIAMOND) | Elmas. |
| [DODECAGON](#DODECAGON) | On iki kenarlı çokgen. |
| [DONUT](#DONUT) | Donut. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Çift dalga. |
| [DOWN_ARROW](#DOWN-ARROW) | Aşağı ok. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Aşağı ok açıklama balonu. |
| [ELLIPSE](#ELLIPSE) | Elips. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Elips şeridi. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Elips şeridi 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Akış şeması alternatif süreç. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Akış şeması derle. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Akış şeması bağlayıcı. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Akış şeması karar. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Akış şeması gecikme. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Akış şeması gösterim. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Akış şeması belge. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Akış şeması çıkarma. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Akış şeması giriş çıkış. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Akış şeması dahili depolama. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Akış şeması manyetik disk. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Akış şeması manyetik tambur. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Akış karakter manyetik bant. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Akış şeması manuel giriş. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Akış şeması manuel işlem. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Akış şeması birleştirme. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Akış şeması çoklu belge. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Akış şeması çevrim dışı depolama. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Akış şeması sayfa dışı bağlayıcı. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Akış şeması çevrimiçi depolama. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Akış şeması veya. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Akış diyagramı önceden tanımlı işlem |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Akış diyagramı hazırlığı. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Akış diyagramı işlemi. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Akış diyagramı delikli kart. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Akış diyagramı delikli bant. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Akış diyagramı sıralama. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Akış diyagramı toplama birleşimi. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Akış diyagramı sonlandırıcı. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Katlanmış köşe. |
| [FRAME](#FRAME) | Çerçeve. |
| [FUNNEL](#FUNNEL) | Huni. |
| [GEAR_6](#GEAR-6) | Altı dişli dişli. |
| [GEAR_9](#GEAR-9) | Dokuz dişli dişli. |
| [GROUP](#GROUP) | Şekil bir grup şekli. |
| [HALF_FRAME](#HALF-FRAME) | Yarım çerçeve. |
| [HEART](#HEART) | Kalp. |
| [HEPTAGON](#HEPTAGON) | Yedigen. |
| [HEXAGON](#HEXAGON) | Altıgen. |
| [HOME_PLATE](#HOME-PLATE) | Ev plakası. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Yatay kaydırma. |
| [IMAGE](#IMAGE) | Şekil bir görüntüdür. |
| [INVERSE_LINE](#INVERSE-LINE) | Ters çizgi. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Düzensiz sızdırmazlık 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Düzensiz sızdırmazlık 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Sol ok. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Sol ok açıklama balonu. |
| [LEFT_BRACE](#LEFT-BRACE) | Sol süslü parantez. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Sol köşeli parantez. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Sol dairesel ok. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Sol sağ ok. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Sol sağ ok açıklama balonu. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Sol-sağ dairesel ok. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Sol-sağ şerit. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | Sol sağ yukarı ok. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | Sol yukarı ok. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | Şimşek. |
| [LINE](#LINE) | Çizgi. |
| [MATH_DIVIDE](#MATH-DIVIDE) | Matematik bölme. |
| [MATH_EQUAL](#MATH-EQUAL) | Matematik eşittir. |
| [MATH_MINUS](#MATH-MINUS) | Matematik eksi. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Matematik çarpma. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Matematik eşit değil. |
| [MATH_PLUS](#MATH-PLUS) | Matematik artı. |
| [MIN_VALUE](#MIN-VALUE) | Sistem kullanımı için ayrılmıştır. |
| [MOON](#MOON) | Ay. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | İzoceles olmayan yamuk. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | Kullanıcı tarafından çizilen ve birden fazla segment ve/veya köşe (eğri, serbest form veya karalama) içeren bir şekil. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Dişli sağ ok. |
| [NO_SMOKING](#NO-SMOKING) | SigaraYok. |
| [OCTAGON](#OCTAGON) | Sekizgen. |
| [OLE_CONTROL](#OLE-CONTROL) | Şekil bir ActiveX denetimidir. |
| [OLE_OBJECT](#OLE-OBJECT) | Şekil bir OLE nesnesidir. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Paralelkenar. |
| [PENTAGON](#PENTAGON) | Beşgen. |
| [PIE](#PIE) | Pasta. |
| [PLAQUE](#PLAQUE) | Plak. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Plak sekmeleri. |
| [PLUS](#PLUS) | Artı. |
| [QUAD_ARROW](#QUAD-ARROW) | Dörtlü ok. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Dört yönlü ok açıklama balonu. |
| [RECTANGLE](#RECTANGLE) | Dikdörtgen. |
| [RIBBON](#RIBBON) | Şerit. |
| [RIBBON_2](#RIBBON-2) | Şerit 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Sağ ok açıklama balonu |
| [RIGHT_BRACE](#RIGHT-BRACE) | Sağ süslü parantez. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Sağ köşeli parantez. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Sağ üçgen. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Yuvarlak dikdörtgen. |
| [SEAL](#SEAL) | Mühür. |
| [SEAL_10](#SEAL-10) | On köşeli yıldız. |
| [SEAL_12](#SEAL-12) | On iki köşeli yıldız. |
| [SEAL_16](#SEAL-16) | On altı köşeli yıldız. |
| [SEAL_24](#SEAL-24) | 24 uçlu yıldız. |
| [SEAL_32](#SEAL-32) | 32 uçlu yıldız. |
| [SEAL_4](#SEAL-4) | Dört uçlu yıldız. |
| [SEAL_6](#SEAL-6) | Altı uçlu yıldız. |
| [SEAL_7](#SEAL-7) | Yedi uçlu yıldız. |
| [SEAL_8](#SEAL-8) | Sekiz uçlu yıldız. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Yuvarlak tek köşeli dikdörtgen. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Tek köşeli dikdörtgen nesnesini kırp. |
| [SMILEY_FACE](#SMILEY-FACE) | Gülümseyen yüz. |
| [SQUARE_TABS](#SQUARE-TABS) | Kare sekmeler. |
| [STAR](#STAR) | Yıldız. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Düz bir bağlayıcı şekil. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Şeritli sağ ok. |
| [SUN](#SUN) | Güneş. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Swoosh oku. |
| [TEARDROP](#TEARDROP) | Gözyaşı damlası. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | Aşağı yay eğrisi, WordArt nesnesi. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | Aşağı yay doldurma, WordArt nesnesi. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | Yukarı yay eğrisi, WordArt nesnesi. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | Yukarı yay doldurma, WordArt nesnesi. |
| [TEXT_BOX](#TEXT-BOX) | Şekil bir metin kutusudur. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | Düğme eğrisi, WordArt nesnesi. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | Düğme doldurma, WordArt nesnesi. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | Aşağı kutu, WordArt nesnesi. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | Yukarı kutu, WordArt nesnesi. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | Aşağı kademeli, WordArt nesnesi. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | Yukarı kademeli, WordArt nesnesi. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | Chevron, WordArt nesnesi. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | Ters Chevron, WordArt nesnesi. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | Daire eğrisi, WordArt nesnesi. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | Daire doldurma, WordArt nesnesi. |
| [TEXT_CURVE](#TEXT-CURVE) | Metin eğrisi. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | Aşağı eğri, WordArt nesnesi. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | Yukarı eğri, WordArt nesnesi. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | Sönük, WordArt nesnesi. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | Altı sönük, WordArt nesnesi. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | Sönük şişir, WordArt nesnesi. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | Sönük şişir sönük, WordArt nesnesi. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | Üstü sönük, WordArt nesnesi. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | Aşağı soluklaş, WordArt nesnesi. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | Sola soluklaş, WordArt nesnesi. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | Sağa soluklaş, WordArt nesnesi. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | Yukarı soluklaş, WordArt nesnesi. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | Metin altıgen. |
| [TEXT_INFLATE](#TEXT-INFLATE) | Şişir, WordArt nesnesi. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | Altı şişir, WordArt nesnesi. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | Üstü şişir, WordArt nesnesi. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | Metin sekizgen. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | Eğri üzerindeki metin. |
| [TEXT_ON_RING](#TEXT-ON-RING) | Halka üzerindeki metin. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | Düz metin, WordArt nesnesi. |
| [TEXT_RING](#TEXT-RING) | Metin halkası. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | İçte halka, WordArt nesnesi. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | Dışta halka, WordArt nesnesi. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | Basit metin. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | Aşağı eğim, WordArt nesnesi. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | Yukarı eğim, WordArt nesnesi. |
| [TEXT_STOP](#TEXT-STOP) | Dur, WordArt nesnesi. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | Üçgen, WordArt nesnesi. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | Ters üçgen, WordArt nesnesi. |
| [TEXT_WAVE](#TEXT-WAVE) | Metin dalgası. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | Dalga 1, WordArt nesnesi. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | Dalga 2, WordArt nesnesi. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | Dalga 3, WordArt nesnesi. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | Dalga 4, WordArt nesnesi. |
| [THICK_ARROW](#THICK-ARROW) | Kalın ok. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Kırp ve yuvarlak tek köşeli dikdörtgen. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Yuvarlak aynı taraf köşe dikdörtgeni. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Kırp aynı taraftaki köşeli dikdörtgen. |
| [TRAPEZOID](#TRAPEZOID) | Trapez. |
| [TRIANGLE](#TRIANGLE) | Üçgen. |
| [UP_ARROW](#UP-ARROW) | Yukarı ok. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Yukarı ok açıklama balonu. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Yukarı aşağı ok. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Yukarı aşağı ok açıklama balonu. |
| [UTURN_ARROW](#UTURN-ARROW) | U dönüş ok. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Dikey kaydırma. |
| [WAVE](#WAVE) | Dalga. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Kama elips açıklama balonu. |
| [WEDGE_PIE](#WEDGE-PIE) | Dilim pasta. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Kama dikdörtgen açıklama balonu. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Kama R dikdörtgen açıklama balonu. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Vurgu kenarlık açıklama 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Vurgu kenarlık açıklama 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Vurgu kenarlık açıklama 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


Vurgu kenarlık açıklama 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Bir oklu vurgu açıklama şekli.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


İki oklu vurgu açıklama şekli.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Üç oklu vurgu açıklama şekli.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


Vurgu açıklama 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Geri önceki eylem düğmesi.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Başlangıç eylem düğmesi.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Boş eylem düğmesi.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Belge eylem düğmesi.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Son eylem düğmesi.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


İleri sonraki eylem düğmesi.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Eylem düğmesi yardım.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Eylem düğmesi ana sayfa.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Eylem düğmesi bilgi.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Eylem düğmesi film.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Eylem düğmesi geri.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Eylem düğmesi ses.

### ARC {#ARC}
```
public static int ARC
```


Yay.

### ARROW {#ARROW}
```
public static int ARROW
```


Ok.

### BALLOON {#BALLOON}
```
public static int BALLOON
```


Balon.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Bükülmüş ok.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


İki segmentli bükülmüş bağlayıcı şekli.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Üç segmentli bükülmüş bağlayıcı şekli.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Dört segmentli bükülmüş bağlayıcı şekli.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Beş segmentli bükülmüş bağlayıcı şekli.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


Bükülmüş yukarı ok.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


Eğim.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


Blok yay.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


Kenarlık açıklama 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Kenarlık açıklama 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Kenarlık açıklama 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


Kenarlık açıklama 90.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Ayraç çifti

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Köşeli parantez çifti.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Tek oklu açıklama şekli.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


İki oklu açıklama şekli.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Üç oklu açıklama şekli.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


Açıklama 90.

### CAN {#CAN}
```
public static int CAN
```


Kutu.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


Grafik artı.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Grafik yıldız.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Grafik X.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


Şerit.

### CHORD {#CHORD}
```
public static int CHORD
```


Kiriş.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


Dairesel ok.

### CLOUD {#CLOUD}
```
public static int CLOUD
```


Bulut.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Bulut açıklama.

### CORNER {#CORNER}
```
public static int CORNER
```


Köşe.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Köşe sekmeleri.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### CUBE {#CUBE}
```
public static int CUBE
```


Küp.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


İki segmentli kavisli bağlayıcı şekli.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Üç segmentli kavisli bağlayıcı şekli.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Dört segmentli kavisli bağlayıcı şekli.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Beş segmentli kavisli bağlayıcı şekli.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


Eğri aşağı ok.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


Eğri sola ok.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


Eğri sağa ok.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


Kavisli yukarı ok

### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


Bu şekil türü, Microsoft Word'deki otomatik şekillerin standart kümesinin bir parçası olmayan şekiller için ayarlanmış gibi görünüyor. Örneğin, ClipArt'tan yeni bir otomatik şekil eklediğinizde.

Bu türde şekiller belge içinde oluşturulamaz.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Ongen.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Yuvarlak köşeli diyagonal dikdörtgen.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Kırpılmış diyagonal köşe dikdörtgeni.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Diyagonal şerit.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Elmas.

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


On iki kenarlı çokgen.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### DONUT {#DONUT}
```
public static int DONUT
```


Donut.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


Çift dalga.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


Aşağı ok.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


Aşağı ok açıklama balonu.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


Elips.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


Elips şeridi.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


Elips şeridi 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


Akış şeması alternatif süreç.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Akış şeması derle.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Akış şeması bağlayıcı.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Akış şeması karar.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Akış şeması gecikme.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Akış şeması gösterim.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Akış şeması belge.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Akış şeması çıkarma.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Akış şeması giriş çıkış.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Akış şeması dahili depolama.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Akış şeması manyetik disk.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Akış şeması manyetik tambur.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Akış karakter manyetik bant.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Akış şeması manuel giriş.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Akış şeması manuel işlem.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Akış şeması birleştirme.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Akış şeması çoklu belge.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Akış şeması çevrim dışı depolama.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Akış şeması sayfa dışı bağlayıcı.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Akış şeması çevrimiçi depolama.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Akış şeması veya.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Akış diyagramı önceden tanımlı işlem

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Akış diyagramı hazırlığı.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Akış diyagramı işlemi.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Akış diyagramı delikli kart.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Akış diyagramı delikli bant.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Akış diyagramı sıralama.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Akış diyagramı toplama birleşimi.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Akış diyagramı sonlandırıcı.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


Katlanmış köşe.

### FRAME {#FRAME}
```
public static int FRAME
```


Çerçeve.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Huni.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Altı dişli dişli.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Dokuz dişli dişli.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### GROUP {#GROUP}
```
public static int GROUP
```


Şekil bir grup şekli.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Yarım çerçeve.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### HEART {#HEART}
```
public static int HEART
```


Kalp.

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


Yedigen.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


Altıgen.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


Ev plakası.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


Yatay kaydırma.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Şekil bir görüntüdür.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Ters çizgi.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


Düzensiz sızdırmazlık 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


Düzensiz sızdırmazlık 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


Sol ok.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


Sol ok açıklama balonu.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


Sol süslü parantez.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


Sol köşeli parantez.

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


Sol dairesel ok.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Sol sağ ok.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Sol sağ ok açıklama balonu.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Sol-sağ dairesel ok.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Sol-sağ şerit.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


Sol sağ yukarı ok.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


Sol yukarı ok.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


Şimşek.

### LINE {#LINE}
```
public static int LINE
```


Çizgi.

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


Matematik bölme.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Matematik eşittir.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Matematik eksi.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Matematik çarpma.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Matematik eşit değil.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Matematik artı.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


Sistem kullanımı için ayrılmıştır.

### MOON {#MOON}
```
public static int MOON
```


Ay.

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


İzoceles olmayan yamuk.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


Kullanıcı tarafından çizilen ve birden fazla segment ve/veya köşe (eğri, serbest form veya karalama) içeren bir şekil.

Bu türde şekiller belge içinde oluşturulamaz.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Dişli sağ ok.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


SigaraYok.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Sekizgen.

### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


Şekil bir ActiveX denetimidir.

Bu türde şekiller belge içinde oluşturulamaz.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


Şekil bir OLE nesnesidir.

Bu türde şekiller belge içinde oluşturulamaz.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


Paralelkenar.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


Beşgen.

### PIE {#PIE}
```
public static int PIE
```


Pasta.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


Plak.

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


Plak sekmeleri.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### PLUS {#PLUS}
```
public static int PLUS
```


Artı.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


Dörtlü ok.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


Dört yönlü ok açıklama balonu.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


Dikdörtgen.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


Şerit.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


Şerit 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


Sağ ok açıklama balonu

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


Sağ süslü parantez.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


Sağ köşeli parantez.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


Sağ üçgen.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


Yuvarlak dikdörtgen.

### SEAL {#SEAL}
```
public static int SEAL
```


Mühür.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


On köşeli yıldız.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


On iki köşeli yıldız.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


On altı köşeli yıldız.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


24 uçlu yıldız.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


32 uçlu yıldız.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Dört uçlu yıldız.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Altı uçlu yıldız.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Yedi uçlu yıldız.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Sekiz uçlu yıldız.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Yuvarlak tek köşeli dikdörtgen.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Tek köşeli dikdörtgen nesnesini kırp.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


Gülümseyen yüz.

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


Kare sekmeler.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### STAR {#STAR}
```
public static int STAR
```


Yıldız.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Düz bir bağlayıcı şekil.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


Şeritli sağ ok.

### SUN {#SUN}
```
public static int SUN
```


Güneş.

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


Swoosh oku.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Gözyaşı damlası.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


Aşağı yay eğrisi, WordArt nesnesi.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


Aşağı yay doldurma, WordArt nesnesi.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


Yukarı yay eğrisi, WordArt nesnesi.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


Yukarı yay doldurma, WordArt nesnesi.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Şekil bir metin kutusudur. Diğer birçok şekil türünün de içinde metin olabileceğini unutmayın. Bir şeklin metin içermesi için bu tipe sahip olması gerekmez.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


Düğme eğrisi, WordArt nesnesi.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


Düğme doldurma, WordArt nesnesi.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


Aşağı kutu, WordArt nesnesi.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


Yukarı kutu, WordArt nesnesi.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


Aşağı kademeli, WordArt nesnesi.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


Yukarı kademeli, WordArt nesnesi.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


Chevron, WordArt nesnesi.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


Ters Chevron, WordArt nesnesi.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


Daire eğrisi, WordArt nesnesi.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


Daire doldurma, WordArt nesnesi.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


Metin eğrisi.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


Aşağı eğri, WordArt nesnesi.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


Yukarı eğri, WordArt nesnesi.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


Sönük, WordArt nesnesi.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


Altı sönük, WordArt nesnesi.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


Sönük şişir, WordArt nesnesi.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


Sönük şişir sönük, WordArt nesnesi.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


Üstü sönük, WordArt nesnesi.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


Aşağı soluklaş, WordArt nesnesi.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


Sola soluklaş, WordArt nesnesi.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


Sağa soluklaş, WordArt nesnesi.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


Yukarı soluklaş, WordArt nesnesi.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


Metin altıgen.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


Şişir, WordArt nesnesi.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


Altı şişir, WordArt nesnesi.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


Üstü şişir, WordArt nesnesi.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


Metin sekizgen.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


Eğri üzerindeki metin.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


Halka üzerindeki metin.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


Düz metin, WordArt nesnesi.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


Metin halkası.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


İçte halka, WordArt nesnesi.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


Dışta halka, WordArt nesnesi.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


Basit metin.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


Aşağı eğim, WordArt nesnesi.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


Yukarı eğim, WordArt nesnesi.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


Dur, WordArt nesnesi.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


Üçgen, WordArt nesnesi.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


Ters üçgen, WordArt nesnesi.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


Metin dalgası.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


Dalga 1, WordArt nesnesi.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


Dalga 2, WordArt nesnesi.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


Dalga 3, WordArt nesnesi.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


Dalga 4, WordArt nesnesi.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


Kalın ok.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Kırp ve yuvarlak tek köşeli dikdörtgen.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Yuvarlak aynı taraf köşe dikdörtgeni.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Kırp aynı taraftaki köşeli dikdörtgen.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


Trapez.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Üçgen.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


Yukarı ok.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


Yukarı ok açıklama balonu.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Yukarı aşağı ok.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Yukarı aşağı ok açıklama balonu.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


U dönüş ok.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


Dikey kaydırma.

### WAVE {#WAVE}
```
public static int WAVE
```


Dalga.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


Kama elips açıklama balonu.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Dilim pasta.

 **Remarks:** 

Yalnızca DML şekilleri için geçerlidir.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Kama dikdörtgen açıklama balonu.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Kama R dikdörtgen açıklama balonu.

### length {#length}
```
public static int length
```


### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeType) {#toString-int}
```
public static String toString(int shapeType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
