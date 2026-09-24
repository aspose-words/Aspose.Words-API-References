---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words Java için"
description: "Java'da grafik öğelerinin şekil tipini belirtir."
type: docs
weight: 90
url: /tr/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

Grafik öğelerinin şekil tipini belirtir.

 **Examples:** 

Grafik veri etiketleri için dolgu, kenar ve açıklama biçimlendirmesinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 // Add new series.
 ChartSeries series = chart.getSeries().add("AW Series 1",
         new String[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
         new double[] { 100.0, 200.0, 300.0, 400.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);

 // Format data labels as callouts.
 ChartFormat format = series.getDataLabels().getFormat();
 format.setShapeType(ChartShapeType.WEDGE_RECT_CALLOUT);
 format.getStroke().setColor(Color.lightGray);
 format.getFill().solid(Color.GREEN);
 series.getDataLabels().getFont().setColor(Color.YELLOW);

 // Change fill and stroke of an individual data label.
 ChartFormat labelFormat = series.getDataLabels().get(0).getFormat();
 labelFormat.getStroke().setColor(Color.BLUE);
 labelFormat.getFill().solid(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.FormatDataLables.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Kenarlıklı vurgu açıklama 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Kenarlıklı vurgu açıklama 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Kenarlıklı vurgu açıklama 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Vurgu açıklama 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Vurgu açıklama 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Vurgu açıklama 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Geri veya önceki düğme. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Başlangıç düğmesi. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Boş düğme. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Belge düğmesi. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Bitiş düğmesi. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | İleri veya sonraki düğme. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Yardım düğmesi. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Ana sayfa düğmesi. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Bilgi düğmesi. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Film düğmesi. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Geri dön düğmesi. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Ses düğmesi. |
| [ARC](#ARC) | Yay. |
| [ARROW](#ARROW) | Ok. |
| [BENT_ARROW](#BENT-ARROW) | Bükülmüş ok. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Bükülmüş bağlayıcı 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Bükülmüş bağlayıcı 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Bükülmüş bağlayıcı 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Bükülmüş bağlayıcı 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Bükülmüş yukarı ok. |
| [BEVEL](#BEVEL) | Eğim. |
| [BLOCK_ARC](#BLOCK-ARC) | Blok yay. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Kenarlı açıklama 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Kenarlı açıklama 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Kenarlı açıklama 3. |
| [BRACE_PAIR](#BRACE-PAIR) | Parantez çifti. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Köşeli parantez çifti. |
| [CALLOUT_1](#CALLOUT-1) | Açıklama 1. |
| [CALLOUT_2](#CALLOUT-2) | Açıklama 2. |
| [CALLOUT_3](#CALLOUT-3) | Açıklama 3. |
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
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Eğri bağlayıcı 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Eğri bağlayıcı 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Eğri bağlayıcı 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Eğri bağlayıcı 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Eğri aşağı ok. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Eğri sola ok. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Eğri sağa ok. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Eğri yukarı ok. |
| [DECAGON](#DECAGON) | Ongen. |
| [DEFAULT](#DEFAULT) | Bir şeklin grafik öğesi için tanımlanmadığını gösterir. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Yuvarlatılmış diyagonal köşe dikdörtgeni. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Kırpılmış diyagonal köşe dikdörtgeni. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Diyagonal şerit. |
| [DIAMOND](#DIAMOND) | Elmas. |
| [DODECAGON](#DODECAGON) | On iki kenarlı çokgen. |
| [DONUT](#DONUT) | Donut. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Çift dalga. |
| [DOWN_ARROW](#DOWN-ARROW) | Aşağı ok. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Açıklama aşağı ok. |
| [ELLIPSE](#ELLIPSE) | Elips. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Elips şeridi. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Elips şeridi 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Alternatif süreç akışı. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Birleştirme akışı. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Bağlayıcı akışı. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Karar akışı. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Gecikme akışı. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Görüntüleme akışı. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Belge akışı. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Çıkarma akışı. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Girdi çıktı akışı. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Dahili depolama akışı. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Manyetik disk akışı. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Manyetik tambur akışı. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Manyetik bant akışı. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Manuel giriş akışı. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Manuel işlem akışı. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Kaynaştırma akışı. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Çoklu belge akışı. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Çevrim dışı depolama akışı. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Sayfa dışı bağlayıcı akışı. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Çevrim içi depolama akışı. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Veya akışı. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Önceden tanımlı süreç akışı. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Hazırlık akışı. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Süreç akışı. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Delikli kart akışı. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Delikli bant akışı. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Sıralama akışı. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Toplama kavşağı akışı. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Sonlandırıcı akışı. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Katlanmış köşe. |
| [FRAME](#FRAME) | Çerçeve. |
| [FUNNEL](#FUNNEL) | Huni. |
| [GEAR_6](#GEAR-6) | Altı dişli dişli. |
| [GEAR_9](#GEAR-9) | Dokuz dişli dişli. |
| [HALF_FRAME](#HALF-FRAME) | Yarım çerçeve. |
| [HEART](#HEART) | Kalp. |
| [HEPTAGON](#HEPTAGON) | Yedigen. |
| [HEXAGON](#HEXAGON) | Altıgen. |
| [HOME_PLATE](#HOME-PLATE) | Ev plakası. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Yatay kaydırma. |
| [INVERSE_LINE](#INVERSE-LINE) | Ters çizgi. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Düzensiz sızdırmazlık 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Düzensiz sızdırmazlık 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Sol ok. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Açıklama sol ok. |
| [LEFT_BRACE](#LEFT-BRACE) | Sol süslü parantez. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Sol köşeli parantez. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Sol dairesel ok. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Sol ve sağ ok. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Açıklama sol ve sağ ok. |
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
| [MOON](#MOON) | Ay. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | İzoceles olmayan yamuk. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Dişli sağ ok. |
| [NO_SMOKING](#NO-SMOKING) | Sigara içmek yasaktır. |
| [OCTAGON](#OCTAGON) | Sekizgen. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Paralelkenar. |
| [PENTAGON](#PENTAGON) | Beşgen. |
| [PIE](#PIE) | Pasta. |
| [PLAQUE](#PLAQUE) | Plak. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Plak sekmeleri. |
| [PLUS](#PLUS) | Artı. |
| [QUAD_ARROW](#QUAD-ARROW) | Dörtlü ok. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Açıklama dörtlü ok. |
| [RECTANGLE](#RECTANGLE) | Dikdörtgen. |
| [RIBBON](#RIBBON) | Şerit. |
| [RIBBON_2](#RIBBON-2) | Şerit 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Sağ oklu açıklama. |
| [RIGHT_BRACE](#RIGHT-BRACE) | Sağ süslü parantez. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Sağ köşeli parantez. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Sağ üçgen. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Yuvarlatılmış dikdörtgen. |
| [SEAL_10](#SEAL-10) | On noktalı yıldız. |
| [SEAL_12](#SEAL-12) | On iki noktalı yıldız. |
| [SEAL_16](#SEAL-16) | On altı noktalı yıldız. |
| [SEAL_24](#SEAL-24) | Yirmi dört noktalı yıldız. |
| [SEAL_32](#SEAL-32) | Otuz iki noktalı yıldız. |
| [SEAL_4](#SEAL-4) | Dört noktalı yıldız. |
| [SEAL_6](#SEAL-6) | Altı noktalı yıldız. |
| [SEAL_7](#SEAL-7) | Yedi noktalı yıldız. |
| [SEAL_8](#SEAL-8) | Sekiz noktalı yıldız. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Yuvarlatılmış tek köşeli dikdörtgen. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Tek köşeli dikdörtgen nesnesini kırp. |
| [SMILEY_FACE](#SMILEY-FACE) | Gülümseyen yüz. |
| [SQUARE_TABS](#SQUARE-TABS) | Kare sekmeler. |
| [STAR](#STAR) | Yıldız. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Düz bağlayıcı 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Şeritli sağ ok. |
| [SUN](#SUN) | Güneş. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Swoosh oku. |
| [TEARDROP](#TEARDROP) | Gözyaşı damlası. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Kırp ve yuvarlak tek köşeli dikdörtgen. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Yuvarlak aynı taraftaki köşeli dikdörtgen. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Kırp aynı taraftaki köşeli dikdörtgen. |
| [TRAPEZOID](#TRAPEZOID) | Trapez. |
| [TRIANGLE](#TRIANGLE) | Üçgen. |
| [UP_ARROW](#UP-ARROW) | Yukarı ok. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Açıklama yukarı ok. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Yukarı ve aşağı ok. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Açıklama yukarı ve aşağı ok. |
| [UTURN_ARROW](#UTURN-ARROW) | U dönüş ok. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Dikey kaydırma. |
| [WAVE](#WAVE) | Dalga. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Açıklama dilim elips. |
| [WEDGE_PIE](#WEDGE-PIE) | Dilim pasta. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Açıklama dilim dikdörtgen. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Açıklama dilim yuvarlak dikdörtgen. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Kenarlıklı vurgu açıklama 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Kenarlıklı vurgu açıklama 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Kenarlıklı vurgu açıklama 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Vurgu açıklama 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Vurgu açıklama 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Vurgu açıklama 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Geri veya önceki düğme.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Başlangıç düğmesi.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Boş düğme.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Belge düğmesi.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Bitiş düğmesi.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


İleri veya sonraki düğme.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Yardım düğmesi.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Ana sayfa düğmesi.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Bilgi düğmesi.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Film düğmesi.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Geri dön düğmesi.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Ses düğmesi.

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

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Bükülmüş ok.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Bükülmüş bağlayıcı 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Bükülmüş bağlayıcı 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Bükülmüş bağlayıcı 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Bükülmüş bağlayıcı 5.

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


Kenarlı açıklama 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Kenarlı açıklama 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Kenarlı açıklama 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Parantez çifti.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Köşeli parantez çifti.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Açıklama 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Açıklama 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Açıklama 3.

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

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Grafik yıldız.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Grafik X.

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

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Köşe sekmeleri.

### CUBE {#CUBE}
```
public static int CUBE
```


Küp.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Eğri bağlayıcı 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Eğri bağlayıcı 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Eğri bağlayıcı 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Eğri bağlayıcı 5.

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


Eğri yukarı ok.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Ongen.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Bir şeklin grafik öğesi için tanımlanmadığını gösterir.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Yuvarlatılmış diyagonal köşe dikdörtgeni.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Kırpılmış diyagonal köşe dikdörtgeni.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Diyagonal şerit.

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


Açıklama aşağı ok.

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


Alternatif süreç akışı.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Birleştirme akışı.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Bağlayıcı akışı.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Karar akışı.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Gecikme akışı.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Görüntüleme akışı.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Belge akışı.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Çıkarma akışı.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Girdi çıktı akışı.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Dahili depolama akışı.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Manyetik disk akışı.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Manyetik tambur akışı.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Manyetik bant akışı.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Manuel giriş akışı.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Manuel işlem akışı.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Kaynaştırma akışı.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Çoklu belge akışı.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Çevrim dışı depolama akışı.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Sayfa dışı bağlayıcı akışı.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Çevrim içi depolama akışı.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Veya akışı.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Önceden tanımlı süreç akışı.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Hazırlık akışı.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Süreç akışı.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Delikli kart akışı.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Delikli bant akışı.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Sıralama akışı.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Toplama kavşağı akışı.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Sonlandırıcı akışı.

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

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Huni.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Altı dişli dişli.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Dokuz dişli dişli.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Yarım çerçeve.

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

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Ters çizgi.

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


Açıklama sol ok.

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

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Sol ve sağ ok.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Açıklama sol ve sağ ok.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Sol-sağ dairesel ok.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Sol-sağ şerit.

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

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Matematik eşittir.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Matematik eksi.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Matematik çarpma.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Matematik eşit değil.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Matematik artı.

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

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Dişli sağ ok.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


Sigara içmek yasaktır.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Sekizgen.

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


Açıklama dörtlü ok.

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


Sağ oklu açıklama.

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


Yuvarlatılmış dikdörtgen.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


On noktalı yıldız.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


On iki noktalı yıldız.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


On altı noktalı yıldız.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Yirmi dört noktalı yıldız.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Otuz iki noktalı yıldız.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Dört noktalı yıldız.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Altı noktalı yıldız.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Yedi noktalı yıldız.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Sekiz noktalı yıldız.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Yuvarlatılmış tek köşeli dikdörtgen.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Tek köşeli dikdörtgen nesnesini kırp.

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

### STAR {#STAR}
```
public static int STAR
```


Yıldız.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Düz bağlayıcı 1.

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

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Gözyaşı damlası.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Kırp ve yuvarlak tek köşeli dikdörtgen.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Yuvarlak aynı taraftaki köşeli dikdörtgen.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Kırp aynı taraftaki köşeli dikdörtgen.

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


Açıklama yukarı ok.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Yukarı ve aşağı ok.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Açıklama yukarı ve aşağı ok.

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


Açıklama dilim elips.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Dilim pasta.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Açıklama dilim dikdörtgen.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Açıklama dilim yuvarlak dikdörtgen.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartShapeType) {#toString-int}
```
public static String toString(int chartShapeType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
