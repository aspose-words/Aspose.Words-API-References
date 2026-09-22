---
title: "ShapeType"
linktitle: "ShapeType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع الشكل في مستند Microsoft Word في Java."
type: docs
weight: 618
url: /ar/java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

يحدد نوع الشكل في مستند Microsoft Word.

 **Examples:** 

يُظهر كيفية إدراج شكل مع صورة من نظام الملفات المحلي إلى مستند.

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

يُظهر كيفية تعريف Aspose.Words للأشكال.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | مستدعي حدود مميزة 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | مستدعي حدود مميزة 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | مستدعي حدود مميزة 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | مستدعي حدود مميزة 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | شكل مستدعي مميز بسهم واحد. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | شكل مستدعي مميز بسهمين. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | شكل مستدعي مميز بثلاثة أسهم. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | مستدعي مميز 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | زر الإجراء للعودة إلى السابق. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | زر الإجراء للبداية. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | زر الإجراء فارغ. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | زر الإجراء للمستند. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | زر الإجراء للنهاية. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | زر الإجراء للتقدم إلى التالي. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | زر الإجراء مساعدة. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | زر الإجراء المنزل. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | زر الإجراء معلومات. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | زر الإجراء فيلم. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | زر الإجراء عودة. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | زر الإجراء صوت. |
| [ARC](#ARC) | قوس. |
| [ARROW](#ARROW) | سهم. |
| [BALLOON](#BALLOON) | بالون. |
| [BENT_ARROW](#BENT-ARROW) | سهم منحني. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | شكل موصل منحني مع مقطعين. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | شكل موصل منحني مع ثلاثة مقاطع. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | شكل موصل منحني مع أربعة مقاطع. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | شكل موصل منحني مع خمسة مقاطع. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | سهم منحني لأعلى. |
| [BEVEL](#BEVEL) | منحدر. |
| [BLOCK_ARC](#BLOCK-ARC) | قوس كتلي. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | ملاحظة حدود 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | ملاحظة حدود 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | ملاحظة حدود 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | ملاحظة حدود 90. |
| [BRACE_PAIR](#BRACE-PAIR) | زوج الأقواس |
| [BRACKET_PAIR](#BRACKET-PAIR) | زوج أقواس مربعة. |
| [CALLOUT_1](#CALLOUT-1) | شكل ملاحظة بسهم واحد. |
| [CALLOUT_2](#CALLOUT-2) | شكل ملاحظة بسهمين. |
| [CALLOUT_3](#CALLOUT-3) | شكل ملاحظة بثلاثة أسهم. |
| [CALLOUT_90](#CALLOUT-90) | ملاحظة 90. |
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
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | شكل موصل منحني مع مقطعين. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | شكل موصل منحني مع ثلاثة مقاطع. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | شكل موصل منحني مع أربعة مقاطع. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | شكل موصل منحني مع خمسة مقاطع. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | سهم منحني لأسفل. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | سهم منحني لليسار. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | سهم منحني لليمين. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | سهم منحني للأعلى |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | يبدو أن نوع الشكل هذا مخصص للأشكال التي لا تكون جزءًا من مجموعة الأشكال التلقائية القياسية في Microsoft Word. |
| [DECAGON](#DECAGON) | عشريني. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | مستطيل بزاوية قطرية مستديرة. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | مستطيل بزاوية قطرية مقصوصة. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | شريط قطري. |
| [DIAMOND](#DIAMOND) | ماس. |
| [DODECAGON](#DODECAGON) | دوديكاغون. |
| [DONUT](#DONUT) | دونات. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | موجة مزدوجة. |
| [DOWN_ARROW](#DOWN-ARROW) | سهم لأسفل. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | ملاحظة بسهم لأسفل. |
| [ELLIPSE](#ELLIPSE) | قطع ناقص. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | شريط قطع ناقص. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | شريط قطع ناقص 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | مخطط تدفق لعملية بديلة. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | مخطط تدفق لتجميع. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | موصل مخطط تدفق. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | قرار مخطط تدفق. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | تأخير مخطط تدفق. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | عرض مخطط تدفق. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | مستند مخطط تدفق. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | استخراج مخطط تدفق. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | إدخال وإخراج مخطط تدفق. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | تخزين داخلي لمخطط تدفق. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | قرص مغناطيسي لمخطط تدفق. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | اسطوانة مغناطيسية لمخطط تدفق. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | شريط مغناطيسي لتدفق. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | إدخال يدوي لمخطط تدفق. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | عملية يدوية لمخطط تدفق. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | دمج مخطط تدفق. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | مستند متعدد لمخطط تدفق. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | تخزين غير متصل لمخطط تدفق. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | موصل خارج الصفحة لمخطط تدفق. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | تخزين متصل لمخطط تدفق. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | أو مخطط تدفق. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | عملية مخطط تدفق محددة مسبقًا |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | تحضير مخطط التدفق. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | عملية مخطط التدفق. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | بطاقة مثقوبة مخطط التدفق. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | شريط مثقوب مخطط التدفق. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | فرز مخطط التدفق. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | تقاطع جمع مخطط التدفق. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | منهي مخطط التدفق. |
| [FOLDED_CORNER](#FOLDED-CORNER) | زاوية مطوية. |
| [FRAME](#FRAME) | إطار. |
| [FUNNEL](#FUNNEL) | قمع. |
| [GEAR_6](#GEAR-6) | ترس ذو ست أسنان. |
| [GEAR_9](#GEAR-9) | ترس ذو تسع أسنان. |
| [GROUP](#GROUP) | الشكل هو شكل مجموعة. |
| [HALF_FRAME](#HALF-FRAME) | نصف إطار. |
| [HEART](#HEART) | قلب. |
| [HEPTAGON](#HEPTAGON) | سباعي. |
| [HEXAGON](#HEXAGON) | سداسي. |
| [HOME_PLATE](#HOME-PLATE) | لوحة البداية. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | تمرير أفقي. |
| [IMAGE](#IMAGE) | الشكل هو صورة. |
| [INVERSE_LINE](#INVERSE-LINE) | خط عكسي. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | ختم غير منتظم 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | ختم غير منتظم 2. |
| [LEFT_ARROW](#LEFT-ARROW) | سهم يسار. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | ملاحظة سهم يسار. |
| [LEFT_BRACE](#LEFT-BRACE) | قوس معقوف أيسر. |
| [LEFT_BRACKET](#LEFT-BRACKET) | قوس مربع أيسر. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | سهم دائري أيسر. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | سهم يسار يمين. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | ملاحظة سهم يسار يمين. |
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
| [MIN_VALUE](#MIN-VALUE) | محجوز لاستخدام النظام. |
| [MOON](#MOON) | قمر. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | شبه منحرف غير متساوي الساقين. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | شكل يرسمه المستخدم ويتكون من عدة مقاطع و/أو رؤوس (منحنى، شكل حر أو خربشة). |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | سهم يميني مسنن. |
| [NO_SMOKING](#NO-SMOKING) | ممنوع التدخين. |
| [OCTAGON](#OCTAGON) | مثمن. |
| [OLE_CONTROL](#OLE-CONTROL) | الشكل هو عنصر تحكم ActiveX. |
| [OLE_OBJECT](#OLE-OBJECT) | الشكل هو كائن OLE. |
| [PARALLELOGRAM](#PARALLELOGRAM) | متوازي أضلاع. |
| [PENTAGON](#PENTAGON) | خماسي. |
| [PIE](#PIE) | فطيرة. |
| [PLAQUE](#PLAQUE) | لوحة. |
| [PLAQUE_TABS](#PLAQUE-TABS) | تبويبات اللوحة. |
| [PLUS](#PLUS) | زائد. |
| [QUAD_ARROW](#QUAD-ARROW) | سهم رباعي. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | ملاحظة سهم رباعي. |
| [RECTANGLE](#RECTANGLE) | مستطيل. |
| [RIBBON](#RIBBON) | شريط. |
| [RIBBON_2](#RIBBON-2) | شريط 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | ملاحظة سهم يمين |
| [RIGHT_BRACE](#RIGHT-BRACE) | قوس معقوف إلى اليمين. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | قوس مربع إلى اليمين. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | مثلث قائم الزاوية إلى اليمين. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | مستطيل مستدير. |
| [SEAL](#SEAL) | ختم. |
| [SEAL_10](#SEAL-10) | نجمة ذات عشر نقاط. |
| [SEAL_12](#SEAL-12) | نجمة ذات اثنتا عشرة نقطة. |
| [SEAL_16](#SEAL-16) | نجمة ذات ستة عشر نقطة. |
| [SEAL_24](#SEAL-24) | نجمة ذات 24 طرفًا. |
| [SEAL_32](#SEAL-32) | نجمة ذات 32 طرفًا. |
| [SEAL_4](#SEAL-4) | نجمة ذات أربعة أطراف. |
| [SEAL_6](#SEAL-6) | نجمة ذات ستة أطراف. |
| [SEAL_7](#SEAL-7) | نجمة ذات سبعة أطراف. |
| [SEAL_8](#SEAL-8) | نجمة ذات ثمانية أطراف. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | مستطيل بزاوية واحدة مستديرة. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | كائن مستطيل زاوية واحدة مقطوعة. |
| [SMILEY_FACE](#SMILEY-FACE) | وجه مبتسم. |
| [SQUARE_TABS](#SQUARE-TABS) | تبويبات مربعة. |
| [STAR](#STAR) | نجمة. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | شكل موصل مستقيم. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | سهم منقوش إلى اليمين. |
| [SUN](#SUN) | شمس. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | سهم سويش. |
| [TEARDROP](#TEARDROP) | قطرة دم. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | قوس منحني لأسفل، كائن WordArt. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | قوس سكب لأسفل، كائن WordArt. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | قوس منحني لأعلى، كائن WordArt. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | قوس سكب لأعلى، كائن WordArt. |
| [TEXT_BOX](#TEXT-BOX) | الشكل هو مربع نص. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | منحنى زر، كائن WordArt. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | سكب زر، كائن WordArt. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | علبة لأسفل، كائن WordArt. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | علبة لأعلى، كائن WordArt. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | شلال لأسفل، كائن WordArt. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | شلال لأعلى، كائن WordArt. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | شيفرون، كائن WordArt. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | شيفرون مقلوب، كائن WordArt. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | منحنى دائرة، كائن WordArt. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | سكب دائرة، كائن WordArt. |
| [TEXT_CURVE](#TEXT-CURVE) | منحنى نص. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | منحنى لأسفل، كائن WordArt. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | منحنى للأعلى، كائن WordArt. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | تفريغ، كائن WordArt. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | تفريغ أسفل، كائن WordArt. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | تفريغ تضخم، كائن WordArt. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | تفريغ تضخم تفريغ، كائن WordArt. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | تفريغ أعلى، كائن WordArt. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | تلاشي للأسفل، كائن WordArt. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | تلاشي إلى اليسار، كائن WordArt. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | تلاشي إلى اليمين، كائن WordArt. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | تلاشي للأعلى، كائن WordArt. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | نص سداسي. |
| [TEXT_INFLATE](#TEXT-INFLATE) | تضخم، كائن WordArt. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | تضخم أسفل، كائن WordArt. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | تضخم أعلى، كائن WordArt. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | نص مثمن. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | نص على منحنى. |
| [TEXT_ON_RING](#TEXT-ON-RING) | نص على حلقة. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | نص عادي، كائن WordArt. |
| [TEXT_RING](#TEXT-RING) | نص حلقة. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | حلقة داخلية، كائن WordArt. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | حلقة خارجية، كائن WordArt. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | نص بسيط. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | انحدار للأسفل، كائن WordArt. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | انحدار للأعلى، كائن WordArt. |
| [TEXT_STOP](#TEXT-STOP) | إيقاف، كائن WordArt. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | مثلث، كائن WordArt. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | مثلث مقلوب، كائن WordArt. |
| [TEXT_WAVE](#TEXT-WAVE) | موجة نص. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | موجة 1، كائن WordArt. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | موجة 2، كائن WordArt. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | موجة 3، كائن WordArt. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | موجة 4، كائن WordArt. |
| [THICK_ARROW](#THICK-ARROW) | سهم سميك. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | مستطيل بزاوية واحدة مقصّة ومستديرة. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | مستطيل زاوية مستديرة على نفس الجانب. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | مستطيل بزاوية واحدة من نفس الجانب مقصّة. |
| [TRAPEZOID](#TRAPEZOID) | شبه منحرف. |
| [TRIANGLE](#TRIANGLE) | مثلث. |
| [UP_ARROW](#UP-ARROW) | سهم أعلى. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | سهم توضيحي للأعلى. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | سهم لأعلى وأسفل. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | سهم توضيحي لأعلى وأسفل. |
| [UTURN_ARROW](#UTURN-ARROW) | سهم انعطاف. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | تمرير عمودي. |
| [WAVE](#WAVE) | موجة. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | ملاحظة إسفنج إهليلجي. |
| [WEDGE_PIE](#WEDGE-PIE) | شريحة فطيرة. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | ملاحظة إسفنج مستطيلة. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | ملاحظة إسفنج R مستطيلة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


مستدعي حدود مميزة 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


مستدعي حدود مميزة 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


مستدعي حدود مميزة 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


مستدعي حدود مميزة 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


شكل مستدعي مميز بسهم واحد.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


شكل مستدعي مميز بسهمين.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


شكل مستدعي مميز بثلاثة أسهم.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


مستدعي مميز 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


زر الإجراء للعودة إلى السابق.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


زر الإجراء للبداية.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


زر الإجراء فارغ.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


زر الإجراء للمستند.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


زر الإجراء للنهاية.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


زر الإجراء للتقدم إلى التالي.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


زر الإجراء مساعدة.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


زر الإجراء المنزل.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


زر الإجراء معلومات.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


زر الإجراء فيلم.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


زر الإجراء عودة.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


زر الإجراء صوت.

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

### BALLOON {#BALLOON}
```
public static int BALLOON
```


بالون.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


سهم منحني.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


شكل موصل منحني مع مقطعين.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


شكل موصل منحني مع ثلاثة مقاطع.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


شكل موصل منحني مع أربعة مقاطع.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


شكل موصل منحني مع خمسة مقاطع.

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


ملاحظة حدود 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


ملاحظة حدود 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


ملاحظة حدود 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


ملاحظة حدود 90.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


زوج الأقواس

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


زوج أقواس مربعة.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


شكل ملاحظة بسهم واحد.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


شكل ملاحظة بسهمين.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


شكل ملاحظة بثلاثة أسهم.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


ملاحظة 90.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


مخطط نجمة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


مخطط X.

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


علامات زاوية.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### CUBE {#CUBE}
```
public static int CUBE
```


مكعب.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


شكل موصل منحني مع مقطعين.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


شكل موصل منحني مع ثلاثة مقاطع.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


شكل موصل منحني مع أربعة مقاطع.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


شكل موصل منحني مع خمسة مقاطع.

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


سهم منحني للأعلى

### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


يبدو أن هذا النوع من الأشكال مخصص للأشكال التي لا تُعد جزءًا من مجموعة الأشكال التلقائية القياسية في Microsoft Word. على سبيل المثال، إذا قمت بإدراج شكل تلقائي جديد من ClipArt.

لا يمكنك إنشاء أشكال من هذا النوع في المستند.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


عشريني.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


مستطيل بزاوية قطرية مستديرة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


مستطيل بزاوية قطرية مقصوصة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


شريط قطري.

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

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


ملاحظة بسهم لأسفل.

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


مخطط تدفق لعملية بديلة.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


مخطط تدفق لتجميع.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


موصل مخطط تدفق.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


قرار مخطط تدفق.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


تأخير مخطط تدفق.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


عرض مخطط تدفق.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


مستند مخطط تدفق.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


استخراج مخطط تدفق.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


إدخال وإخراج مخطط تدفق.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


تخزين داخلي لمخطط تدفق.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


قرص مغناطيسي لمخطط تدفق.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


اسطوانة مغناطيسية لمخطط تدفق.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


شريط مغناطيسي لتدفق.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


إدخال يدوي لمخطط تدفق.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


عملية يدوية لمخطط تدفق.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


دمج مخطط تدفق.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


مستند متعدد لمخطط تدفق.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


تخزين غير متصل لمخطط تدفق.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


موصل خارج الصفحة لمخطط تدفق.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


تخزين متصل لمخطط تدفق.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


أو مخطط تدفق.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


عملية مخطط تدفق محددة مسبقًا

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


تحضير مخطط التدفق.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


عملية مخطط التدفق.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


بطاقة مثقوبة مخطط التدفق.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


شريط مثقوب مخطط التدفق.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


فرز مخطط التدفق.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


تقاطع جمع مخطط التدفق.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


منهي مخطط التدفق.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


قمع.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


ترس ذو ست أسنان.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


ترس ذو تسع أسنان.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### GROUP {#GROUP}
```
public static int GROUP
```


الشكل هو شكل مجموعة.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


نصف إطار.

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

### IMAGE {#IMAGE}
```
public static int IMAGE
```


الشكل هو صورة.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


خط عكسي.

 **Remarks:** 

ينطبق فقط على أشكال DML.

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


ملاحظة سهم يسار.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


سهم يسار يمين.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


ملاحظة سهم يسار يمين.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


سهم دائري من اليسار إلى اليمين.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


شريط من اليسار إلى اليمين.

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


مساواة رياضية.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


طرح رياضي.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


ضرب رياضي.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


عدم مساواة رياضية.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


جمع رياضي.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


محجوز لاستخدام النظام.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


شكل يرسمه المستخدم ويتكون من عدة مقاطع و/أو رؤوس (منحنى، شكل حر أو خربشة).

لا يمكنك إنشاء أشكال من هذا النوع في المستند.

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

### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


الشكل هو عنصر تحكم ActiveX.

لا يمكنك إنشاء أشكال من هذا النوع في المستند.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


الشكل هو كائن OLE.

لا يمكنك إنشاء أشكال من هذا النوع في المستند.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

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


ملاحظة سهم رباعي.

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


ملاحظة سهم يمين

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


مستطيل مستدير.

### SEAL {#SEAL}
```
public static int SEAL
```


ختم.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


نجمة ذات عشر نقاط.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


نجمة ذات اثنتا عشرة نقطة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


نجمة ذات ستة عشر نقطة.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


نجمة ذات 24 طرفًا.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


نجمة ذات 32 طرفًا.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


نجمة ذات أربعة أطراف.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


نجمة ذات ستة أطراف.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


نجمة ذات سبعة أطراف.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


نجمة ذات ثمانية أطراف.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


مستطيل بزاوية واحدة مستديرة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


كائن مستطيل زاوية واحدة مقطوعة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### STAR {#STAR}
```
public static int STAR
```


نجمة.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


شكل موصل مستقيم.

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

 **Remarks:** 

ينطبق فقط على أشكال DML.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


قطرة دم.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


قوس منحني لأسفل، كائن WordArt.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


قوس سكب لأسفل، كائن WordArt.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


قوس منحني لأعلى، كائن WordArt.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


قوس سكب لأعلى، كائن WordArt.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


الشكل هو مربع نص. لاحظ أن الأشكال من أنواع أخرى كثيرة يمكنها أيضًا أن تحتوي على نص بداخلها. لا يلزم أن يكون الشكل من هذا النوع ليحتوي على نص.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


منحنى زر، كائن WordArt.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


سكب زر، كائن WordArt.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


علبة لأسفل، كائن WordArt.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


علبة لأعلى، كائن WordArt.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


شلال لأسفل، كائن WordArt.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


شلال لأعلى، كائن WordArt.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


شيفرون، كائن WordArt.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


شيفرون مقلوب، كائن WordArt.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


منحنى دائرة، كائن WordArt.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


سكب دائرة، كائن WordArt.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


منحنى نص.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


منحنى لأسفل، كائن WordArt.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


منحنى للأعلى، كائن WordArt.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


تفريغ، كائن WordArt.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


تفريغ أسفل، كائن WordArt.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


تفريغ تضخم، كائن WordArt.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


تفريغ تضخم تفريغ، كائن WordArt.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


تفريغ أعلى، كائن WordArt.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


تلاشي للأسفل، كائن WordArt.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


تلاشي إلى اليسار، كائن WordArt.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


تلاشي إلى اليمين، كائن WordArt.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


تلاشي للأعلى، كائن WordArt.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


نص سداسي.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


تضخم، كائن WordArt.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


تضخم أسفل، كائن WordArt.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


تضخم أعلى، كائن WordArt.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


نص مثمن.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


نص على منحنى.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


نص على حلقة.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


نص عادي، كائن WordArt.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


نص حلقة.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


حلقة داخلية، كائن WordArt.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


حلقة خارجية، كائن WordArt.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


نص بسيط.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


انحدار للأسفل، كائن WordArt.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


انحدار للأعلى، كائن WordArt.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


إيقاف، كائن WordArt.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


مثلث، كائن WordArt.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


مثلث مقلوب، كائن WordArt.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


موجة نص.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


موجة 1، كائن WordArt.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


موجة 2، كائن WordArt.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


موجة 3، كائن WordArt.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


موجة 4، كائن WordArt.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


سهم سميك.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


مستطيل بزاوية واحدة مقصّة ومستديرة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


مستطيل زاوية مستديرة على نفس الجانب.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


مستطيل بزاوية واحدة من نفس الجانب مقصّة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

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


سهم توضيحي للأعلى.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


سهم لأعلى وأسفل.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


سهم توضيحي لأعلى وأسفل.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


سهم انعطاف.

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


ملاحظة إسفنج إهليلجي.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


شريحة فطيرة.

 **Remarks:** 

ينطبق فقط على أشكال DML.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


ملاحظة إسفنج مستطيلة.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


ملاحظة إسفنج R مستطيلة.

### length {#length}
```
public static int length
```


### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
