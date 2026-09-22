---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع الشكل لعناصر المخطط في جافا."
type: docs
weight: 90
url: /ar/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

يحدد نوع الشكل لعناصر المخطط.

 **Examples:** 

يظهر كيفية تعيين التعبئة، الحد وتنسيق التعليق لتسميات بيانات المخطط.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | تعليق مميز مع حد 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | تعليق مميز مع حد 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | تعليق مميز مع حد 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | تعليق مميز 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | تعليق مميز 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | تعليق مميز 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | زر الرجوع أو السابق. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | زر البداية. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | زر فارغ. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | زر المستند. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | زر النهاية. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | زر التقدم أو التالي. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | زر المساعدة. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | زر الصفحة الرئيسية. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | زر المعلومات. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | زر الفيلم. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | زر الإرجاع. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | زر الصوت. |
| [ARC](#ARC) | قوس. |
| [ARROW](#ARROW) | سهم. |
| [BENT_ARROW](#BENT-ARROW) | سهم منحني. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | موصل منحني 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | موصل منحني 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | موصل منحني 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | موصل منحني 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | سهم منحني لأعلى. |
| [BEVEL](#BEVEL) | منحدر. |
| [BLOCK_ARC](#BLOCK-ARC) | قوس كتلي. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | ملاحظة مع حد 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | ملاحظة مع حد 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | ملاحظة مع حد 3. |
| [BRACE_PAIR](#BRACE-PAIR) | زوج أقواس معقوفة. |
| [BRACKET_PAIR](#BRACKET-PAIR) | زوج أقواس مربعة. |
| [CALLOUT_1](#CALLOUT-1) | ملاحظة 1. |
| [CALLOUT_2](#CALLOUT-2) | ملاحظة 2. |
| [CALLOUT_3](#CALLOUT-3) | ملاحظة 3. |
| [CAN](#CAN) | علبة. |
| [CHART_PLUS](#CHART-PLUS) | مخطط زائد. |
| [CHART_STAR](#CHART-STAR) | مخطط نجمة. |
| [CHART_X](#CHART-X) | مخطط X. |
| [CHEVRON](#CHEVRON) | شيفرون. |
| [CHORD](#CHORD) | وتر. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | سهم دائري. |
| [CLOUD](#CLOUD) | سحابة. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | ملاحظة سحابة. |
| [CORNER](#CORNER) | زاوية. |
| [CORNER_TABS](#CORNER-TABS) | علامات زاوية. |
| [CUBE](#CUBE) | مكعب. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | موصل منحني 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | موصل منحني 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | موصل منحني 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | موصل منحني 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | سهم منحني لأسفل. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | سهم منحني لليسار. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | سهم منحني لليمين. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | سهم منحني لأعلى. |
| [DECAGON](#DECAGON) | عشريني. |
| [DEFAULT](#DEFAULT) | يشير إلى أن الشكل غير معرف لعنصر المخطط. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | مستطيل بزاوية قطرية مستديرة. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | مستطيل بزاوية قطرية مقصوصة. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | شريط قطري. |
| [DIAMOND](#DIAMOND) | ماس. |
| [DODECAGON](#DODECAGON) | دوديكاغون. |
| [DONUT](#DONUT) | دونات. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | موجة مزدوجة. |
| [DOWN_ARROW](#DOWN-ARROW) | سهم لأسفل. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | سهم توضيحي لأسفل. |
| [ELLIPSE](#ELLIPSE) | قطع ناقص. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | شريط قطع ناقص. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | شريط قطع ناقص 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | تدفق العملية البديلة. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | تدفق التجميع. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | تدفق الموصل. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | تدفق القرار. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | تدفق التأخير. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | تدفق العرض. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | تدفق المستند. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | تدفق الاستخراج. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | تدفق الإدخال والإخراج. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | تدفق التخزين الداخلي. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | تدفق القرص المغناطيسي. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | تدفق الأسطوانة المغناطيسية. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | تدفق الشريط المغناطيسي. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | تدفق الإدخال اليدوي. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | تدفق العملية اليدوية. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | تدفق الدمج. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | تدفق متعدد المستندات. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | تدفق التخزين غير المتصل. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | تدفق موصل خارج الصفحة. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | تدفق التخزين المتصل. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | تدفق أو. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | تدفق العملية المحددة مسبقًا. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | تدفق التحضير. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | تدفق العملية. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | تدفق بطاقة مثقوبة. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | تدفق الشريط المثقوب. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | تدفق الفرز. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | تدفق تقاطع الجمع. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | تدفق المنهي. |
| [FOLDED_CORNER](#FOLDED-CORNER) | زاوية مطوية. |
| [FRAME](#FRAME) | إطار. |
| [FUNNEL](#FUNNEL) | قمع. |
| [GEAR_6](#GEAR-6) | ترس ذو ست أسنان. |
| [GEAR_9](#GEAR-9) | ترس ذو تسع أسنان. |
| [HALF_FRAME](#HALF-FRAME) | نصف إطار. |
| [HEART](#HEART) | قلب. |
| [HEPTAGON](#HEPTAGON) | سباعي. |
| [HEXAGON](#HEXAGON) | سداسي. |
| [HOME_PLATE](#HOME-PLATE) | لوحة البداية. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | تمرير أفقي. |
| [INVERSE_LINE](#INVERSE-LINE) | خط عكسي. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | ختم غير منتظم 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | ختم غير منتظم 2. |
| [LEFT_ARROW](#LEFT-ARROW) | سهم يسار. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | سهم يسار توضيحي. |
| [LEFT_BRACE](#LEFT-BRACE) | قوس معقوف أيسر. |
| [LEFT_BRACKET](#LEFT-BRACKET) | قوس مربع أيسر. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | سهم دائري أيسر. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | سهم أيسر ويمين. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | سهم أيسر ويمين توضيحي. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | سهم دائري من اليسار إلى اليمين. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | شريط من اليسار إلى اليمين. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | سهم من اليسار إلى اليمين إلى الأعلى. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | سهم من اليسار إلى الأعلى. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | صاعقة. |
| [LINE](#LINE) | خط. |
| [MATH_DIVIDE](#MATH-DIVIDE) | قسمة رياضية. |
| [MATH_EQUAL](#MATH-EQUAL) | مساواة رياضية. |
| [MATH_MINUS](#MATH-MINUS) | طرح رياضي. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | ضرب رياضي. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | عدم مساواة رياضية. |
| [MATH_PLUS](#MATH-PLUS) | جمع رياضي. |
| [MOON](#MOON) | قمر. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | شبه منحرف غير متساوي الساقين. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | سهم يميني مسنن. |
| [NO_SMOKING](#NO-SMOKING) | ممنوع التدخين. |
| [OCTAGON](#OCTAGON) | مثمن. |
| [PARALLELOGRAM](#PARALLELOGRAM) | متوازي أضلاع. |
| [PENTAGON](#PENTAGON) | خماسي. |
| [PIE](#PIE) | فطيرة. |
| [PLAQUE](#PLAQUE) | لوحة. |
| [PLAQUE_TABS](#PLAQUE-TABS) | تبويبات اللوحة. |
| [PLUS](#PLUS) | زائد. |
| [QUAD_ARROW](#QUAD-ARROW) | سهم رباعي. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | سهم رباعي مع توضيح. |
| [RECTANGLE](#RECTANGLE) | مستطيل. |
| [RIBBON](#RIBBON) | شريط. |
| [RIBBON_2](#RIBBON-2) | شريط 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | سهم توضيحي إلى اليمين. |
| [RIGHT_BRACE](#RIGHT-BRACE) | قوس معقوف إلى اليمين. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | قوس مربع إلى اليمين. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | مثلث قائم الزاوية إلى اليمين. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | مستطيل مستدير الزوايا. |
| [SEAL_10](#SEAL-10) | نجمة ذات عشر نقاط. |
| [SEAL_12](#SEAL-12) | نجمة ذات اثنتا عشرة نقطة. |
| [SEAL_16](#SEAL-16) | نجمة ذات ستة عشر نقطة. |
| [SEAL_24](#SEAL-24) | نجمة ذات أربعة وعشرين نقطة. |
| [SEAL_32](#SEAL-32) | نجمة ذات اثنين وثلاثين نقطة. |
| [SEAL_4](#SEAL-4) | نجمة ذات أربع نقاط. |
| [SEAL_6](#SEAL-6) | نجمة ذات ست نقاط. |
| [SEAL_7](#SEAL-7) | نجمة ذات سبع نقاط. |
| [SEAL_8](#SEAL-8) | نجمة ذات ثمان نقاط. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | مستطيل زاوية واحدة مستديرة. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | كائن مستطيل زاوية واحدة مقطوعة. |
| [SMILEY_FACE](#SMILEY-FACE) | وجه مبتسم. |
| [SQUARE_TABS](#SQUARE-TABS) | تبويبات مربعة. |
| [STAR](#STAR) | نجمة. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | موصل مستقيم 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | سهم منقوش إلى اليمين. |
| [SUN](#SUN) | شمس. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | سهم سويش. |
| [TEARDROP](#TEARDROP) | قطرة دم. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | مستطيل بزاوية واحدة مقصّة ومستديرة. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | مستطيل بزاوية واحدة من نفس الجانب مستديرة. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | مستطيل بزاوية واحدة من نفس الجانب مقصّة. |
| [TRAPEZOID](#TRAPEZOID) | شبه منحرف. |
| [TRIANGLE](#TRIANGLE) | مثلث. |
| [UP_ARROW](#UP-ARROW) | سهم أعلى. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | ملاحظة بسهم أعلى. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | سهم أعلى وأسفل. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | ملاحظة بسهم أعلى وأسفل. |
| [UTURN_ARROW](#UTURN-ARROW) | سهم دوران U. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | تمرير عمودي. |
| [WAVE](#WAVE) | موجة. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | ملاحظة بقطاع إهليلجي. |
| [WEDGE_PIE](#WEDGE-PIE) | شريحة فطيرة. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | ملاحظة بقطاع مستطيل. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | ملاحظة بقطاع مستطيل مستدير. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


تعليق مميز مع حد 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


تعليق مميز مع حد 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


تعليق مميز مع حد 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


تعليق مميز 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


تعليق مميز 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


تعليق مميز 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


زر الرجوع أو السابق.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


زر البداية.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


زر فارغ.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


زر المستند.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


زر النهاية.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


زر التقدم أو التالي.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


زر المساعدة.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


زر الصفحة الرئيسية.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


زر المعلومات.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


زر الفيلم.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


زر الإرجاع.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


زر الصوت.

### ARC {#ARC}
```
public static int ARC
```


قوس.

### ARROW {#ARROW}
```
public static int ARROW
```


سهم.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


سهم منحني.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


موصل منحني 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


موصل منحني 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


موصل منحني 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


موصل منحني 5.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


سهم منحني لأعلى.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


منحدر.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


قوس كتلي.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


ملاحظة مع حد 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


ملاحظة مع حد 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


ملاحظة مع حد 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


زوج أقواس معقوفة.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


زوج أقواس مربعة.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


ملاحظة 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


ملاحظة 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


ملاحظة 3.

### CAN {#CAN}
```
public static int CAN
```


علبة.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


مخطط زائد.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


مخطط نجمة.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


مخطط X.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


شيفرون.

### CHORD {#CHORD}
```
public static int CHORD
```


وتر.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


سهم دائري.

### CLOUD {#CLOUD}
```
public static int CLOUD
```


سحابة.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


ملاحظة سحابة.

### CORNER {#CORNER}
```
public static int CORNER
```


زاوية.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


علامات زاوية.

### CUBE {#CUBE}
```
public static int CUBE
```


مكعب.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


موصل منحني 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


موصل منحني 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


موصل منحني 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


موصل منحني 5.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


سهم منحني لأسفل.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


سهم منحني لليسار.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


سهم منحني لليمين.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


سهم منحني لأعلى.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


عشريني.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يشير إلى أن الشكل غير معرف لعنصر المخطط.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


مستطيل بزاوية قطرية مستديرة.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


مستطيل بزاوية قطرية مقصوصة.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


شريط قطري.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


ماس.

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


دوديكاغون.

### DONUT {#DONUT}
```
public static int DONUT
```


دونات.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


موجة مزدوجة.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


سهم لأسفل.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


سهم توضيحي لأسفل.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


قطع ناقص.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


شريط قطع ناقص.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


شريط قطع ناقص 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


تدفق العملية البديلة.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


تدفق التجميع.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


تدفق الموصل.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


تدفق القرار.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


تدفق التأخير.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


تدفق العرض.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


تدفق المستند.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


تدفق الاستخراج.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


تدفق الإدخال والإخراج.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


تدفق التخزين الداخلي.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


تدفق القرص المغناطيسي.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


تدفق الأسطوانة المغناطيسية.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


تدفق الشريط المغناطيسي.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


تدفق الإدخال اليدوي.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


تدفق العملية اليدوية.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


تدفق الدمج.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


تدفق متعدد المستندات.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


تدفق التخزين غير المتصل.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


تدفق موصل خارج الصفحة.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


تدفق التخزين المتصل.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


تدفق أو.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


تدفق العملية المحددة مسبقًا.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


تدفق التحضير.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


تدفق العملية.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


تدفق بطاقة مثقوبة.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


تدفق الشريط المثقوب.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


تدفق الفرز.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


تدفق تقاطع الجمع.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


تدفق المنهي.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


زاوية مطوية.

### FRAME {#FRAME}
```
public static int FRAME
```


إطار.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


قمع.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


ترس ذو ست أسنان.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


ترس ذو تسع أسنان.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


نصف إطار.

### HEART {#HEART}
```
public static int HEART
```


قلب.

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


سباعي.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


سداسي.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


لوحة البداية.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


تمرير أفقي.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


خط عكسي.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


ختم غير منتظم 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


ختم غير منتظم 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


سهم يسار.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


سهم يسار توضيحي.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


قوس معقوف أيسر.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


قوس مربع أيسر.

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


سهم دائري أيسر.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


سهم أيسر ويمين.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


سهم أيسر ويمين توضيحي.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


سهم دائري من اليسار إلى اليمين.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


شريط من اليسار إلى اليمين.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


سهم من اليسار إلى اليمين إلى الأعلى.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


سهم من اليسار إلى الأعلى.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


صاعقة.

### LINE {#LINE}
```
public static int LINE
```


خط.

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


قسمة رياضية.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


مساواة رياضية.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


طرح رياضي.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


ضرب رياضي.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


عدم مساواة رياضية.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


جمع رياضي.

### MOON {#MOON}
```
public static int MOON
```


قمر.

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


شبه منحرف غير متساوي الساقين.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


سهم يميني مسنن.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


ممنوع التدخين.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


مثمن.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


متوازي أضلاع.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


خماسي.

### PIE {#PIE}
```
public static int PIE
```


فطيرة.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


لوحة.

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


تبويبات اللوحة.

### PLUS {#PLUS}
```
public static int PLUS
```


زائد.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


سهم رباعي.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


سهم رباعي مع توضيح.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


مستطيل.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


شريط.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


شريط 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


سهم توضيحي إلى اليمين.

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


قوس معقوف إلى اليمين.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


قوس مربع إلى اليمين.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


مثلث قائم الزاوية إلى اليمين.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


مستطيل مستدير الزوايا.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


نجمة ذات عشر نقاط.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


نجمة ذات اثنتا عشرة نقطة.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


نجمة ذات ستة عشر نقطة.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


نجمة ذات أربعة وعشرين نقطة.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


نجمة ذات اثنين وثلاثين نقطة.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


نجمة ذات أربع نقاط.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


نجمة ذات ست نقاط.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


نجمة ذات سبع نقاط.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


نجمة ذات ثمان نقاط.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


مستطيل زاوية واحدة مستديرة.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


كائن مستطيل زاوية واحدة مقطوعة.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


وجه مبتسم.

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


تبويبات مربعة.

### STAR {#STAR}
```
public static int STAR
```


نجمة.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


موصل مستقيم 1.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


سهم منقوش إلى اليمين.

### SUN {#SUN}
```
public static int SUN
```


شمس.

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


سهم سويش.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


قطرة دم.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


مستطيل بزاوية واحدة مقصّة ومستديرة.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


مستطيل بزاوية واحدة من نفس الجانب مستديرة.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


مستطيل بزاوية واحدة من نفس الجانب مقصّة.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


شبه منحرف.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


مثلث.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


سهم أعلى.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


ملاحظة بسهم أعلى.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


سهم أعلى وأسفل.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


ملاحظة بسهم أعلى وأسفل.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


سهم دوران U.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


تمرير عمودي.

### WAVE {#WAVE}
```
public static int WAVE
```


موجة.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


ملاحظة بقطاع إهليلجي.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


شريحة فطيرة.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


ملاحظة بقطاع مستطيل.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


ملاحظة بقطاع مستطيل مستدير.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
