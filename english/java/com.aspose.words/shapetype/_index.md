---
title: ShapeType
linktitle: ShapeType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of shape in a Microsoft Word document in Java.
type: docs
weight: 530
url: /java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

Specifies the type of shape in a Microsoft Word document.

 **Examples:** 

Shows how to insert a shape with an image from the local file system into a document.

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

Shows how Aspose.Words identify shapes.

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
## Fields

| Field | Description |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) |  |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) |  |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) |  |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) |  |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) |  |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) |  |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) |  |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) |  |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) |  |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) |  |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) |  |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) |  |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) |  |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) |  |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) |  |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) |  |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) |  |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) |  |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) |  |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) |  |
| [ARC](#ARC) |  |
| [ARROW](#ARROW) |  |
| [BALLOON](#BALLOON) |  |
| [BENT_ARROW](#BENT-ARROW) |  |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) |  |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) |  |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) |  |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) |  |
| [BENT_UP_ARROW](#BENT-UP-ARROW) |  |
| [BEVEL](#BEVEL) |  |
| [BLOCK_ARC](#BLOCK-ARC) |  |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) |  |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) |  |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) |  |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) |  |
| [BRACE_PAIR](#BRACE-PAIR) |  |
| [BRACKET_PAIR](#BRACKET-PAIR) |  |
| [CALLOUT_1](#CALLOUT-1) |  |
| [CALLOUT_2](#CALLOUT-2) |  |
| [CALLOUT_3](#CALLOUT-3) |  |
| [CALLOUT_90](#CALLOUT-90) |  |
| [CAN](#CAN) |  |
| [CHART_PLUS](#CHART-PLUS) | Chart plus. |
| [CHART_STAR](#CHART-STAR) | Chart star. |
| [CHART_X](#CHART-X) | Chart X. |
| [CHEVRON](#CHEVRON) |  |
| [CHORD](#CHORD) | Chord. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) |  |
| [CLOUD](#CLOUD) | Cloud. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) |  |
| [CORNER](#CORNER) | Corner. |
| [CORNER_TABS](#CORNER-TABS) | Corner tabs. |
| [CUBE](#CUBE) |  |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) |  |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) |  |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) |  |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) |  |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) |  |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) |  |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) |  |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) |  |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | This shape type seems to be set for shapes that are not part of the standard set of the auto shapes in Microsoft Word. |
| [DECAGON](#DECAGON) | Decagon. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Round diagonal corner rectangle. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Snip diagonal corner rectangle. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Diagonal stripe. |
| [DIAMOND](#DIAMOND) |  |
| [DODECAGON](#DODECAGON) | Dodecagon. |
| [DONUT](#DONUT) |  |
| [DOUBLE_WAVE](#DOUBLE-WAVE) |  |
| [DOWN_ARROW](#DOWN-ARROW) |  |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) |  |
| [ELLIPSE](#ELLIPSE) |  |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) |  |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) |  |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) |  |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) |  |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) |  |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) |  |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) |  |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) |  |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) |  |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) |  |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) |  |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) |  |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) |  |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) |  |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) |  |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) |  |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) |  |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) |  |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) |  |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) |  |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) |  |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) |  |
| [FLOW_CHART_OR](#FLOW-CHART-OR) |  |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) |  |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) |  |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) |  |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) |  |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) |  |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) |  |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) |  |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) |  |
| [FOLDED_CORNER](#FOLDED-CORNER) |  |
| [FRAME](#FRAME) | Frame. |
| [FUNNEL](#FUNNEL) | Funnel. |
| [GEAR_6](#GEAR-6) | Six-tooth gear. |
| [GEAR_9](#GEAR-9) | Nine-tooth gear. |
| [GROUP](#GROUP) | The shape is a group shape. |
| [HALF_FRAME](#HALF-FRAME) | Half frame. |
| [HEART](#HEART) |  |
| [HEPTAGON](#HEPTAGON) | Heptagon. |
| [HEXAGON](#HEXAGON) |  |
| [HOME_PLATE](#HOME-PLATE) |  |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) |  |
| [IMAGE](#IMAGE) | The shape is an image. |
| [INVERSE_LINE](#INVERSE-LINE) | Inverse line. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) |  |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) |  |
| [LEFT_ARROW](#LEFT-ARROW) |  |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) |  |
| [LEFT_BRACE](#LEFT-BRACE) |  |
| [LEFT_BRACKET](#LEFT-BRACKET) |  |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Left circular arrow. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) |  |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) |  |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Left-right circular arrow. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Left-right ribbon. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) |  |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) |  |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) |  |
| [LINE](#LINE) |  |
| [MATH_DIVIDE](#MATH-DIVIDE) | Math divide. |
| [MATH_EQUAL](#MATH-EQUAL) | Math equal. |
| [MATH_MINUS](#MATH-MINUS) | Math minus. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Math multiply. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Math not equal. |
| [MATH_PLUS](#MATH-PLUS) | Math plus. |
| [MIN_VALUE](#MIN-VALUE) | Reserved for the system use. |
| [MOON](#MOON) |  |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Non-isosceles trapezoid. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | A shape drawn by user and consisting of multiple segments and/or vertices (curve, freeform or scribble). |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) |  |
| [NO_SMOKING](#NO-SMOKING) |  |
| [OCTAGON](#OCTAGON) |  |
| [OLE_CONTROL](#OLE-CONTROL) | The shape is an ActiveX control. |
| [OLE_OBJECT](#OLE-OBJECT) | The shape is an OLE object. |
| [PARALLELOGRAM](#PARALLELOGRAM) |  |
| [PENTAGON](#PENTAGON) |  |
| [PIE](#PIE) | Pie. |
| [PLAQUE](#PLAQUE) |  |
| [PLAQUE_TABS](#PLAQUE-TABS) | Plaque tabs. |
| [PLUS](#PLUS) |  |
| [QUAD_ARROW](#QUAD-ARROW) |  |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) |  |
| [RECTANGLE](#RECTANGLE) |  |
| [RIBBON](#RIBBON) |  |
| [RIBBON_2](#RIBBON-2) |  |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) |  |
| [RIGHT_BRACE](#RIGHT-BRACE) |  |
| [RIGHT_BRACKET](#RIGHT-BRACKET) |  |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) |  |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) |  |
| [SEAL](#SEAL) |  |
| [SEAL_10](#SEAL-10) | Ten-pointed star. |
| [SEAL_12](#SEAL-12) | Twelve-pointed star. |
| [SEAL_16](#SEAL-16) |  |
| [SEAL_24](#SEAL-24) |  |
| [SEAL_32](#SEAL-32) |  |
| [SEAL_4](#SEAL-4) |  |
| [SEAL_6](#SEAL-6) | Six-pointed star. |
| [SEAL_7](#SEAL-7) | Seven-pointed star. |
| [SEAL_8](#SEAL-8) |  |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Round single corner rectangle. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Snip single corner rectangle object. |
| [SMILEY_FACE](#SMILEY-FACE) |  |
| [SQUARE_TABS](#SQUARE-TABS) | Square tabs. |
| [STAR](#STAR) |  |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) |  |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) |  |
| [SUN](#SUN) |  |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Swoosh arrow. |
| [TEARDROP](#TEARDROP) | Teardrop. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | WordArt object. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | WordArt object. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | WordArt object. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | WordArt object. |
| [TEXT_BOX](#TEXT-BOX) | The shape is a textbox. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | WordArt object. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | WordArt object. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | WordArt object. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | WordArt object. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | WordArt object. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | WordArt object. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | WordArt object. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | WordArt object. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | WordArt object. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | WordArt object. |
| [TEXT_CURVE](#TEXT-CURVE) |  |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | WordArt object. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | WordArt object. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | WordArt object. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | WordArt object. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | WordArt object. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | WordArt object. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | WordArt object. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | WordArt object. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | WordArt object. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | WordArt object. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | WordArt object. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) |  |
| [TEXT_INFLATE](#TEXT-INFLATE) | WordArt object. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | WordArt object. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | WordArt object. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) |  |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) |  |
| [TEXT_ON_RING](#TEXT-ON-RING) |  |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | WordArt object. |
| [TEXT_RING](#TEXT-RING) |  |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | WordArt object. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | WordArt object. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) |  |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | WordArt object. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | WordArt object. |
| [TEXT_STOP](#TEXT-STOP) | WordArt object. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | WordArt object. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | WordArt object. |
| [TEXT_WAVE](#TEXT-WAVE) |  |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | WordArt object. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | WordArt object. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | WordArt object. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | WordArt object. |
| [THICK_ARROW](#THICK-ARROW) |  |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Snip and round single corner rectangle. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Round same side corner rectangle. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Snip same side corner rectangle. |
| [TRAPEZOID](#TRAPEZOID) |  |
| [TRIANGLE](#TRIANGLE) |  |
| [UP_ARROW](#UP-ARROW) |  |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) |  |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) |  |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) |  |
| [UTURN_ARROW](#UTURN-ARROW) |  |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) |  |
| [WAVE](#WAVE) |  |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) |  |
| [WEDGE_PIE](#WEDGE-PIE) | Wedge pie. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) |  |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int shapeType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```




### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```




### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```




### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```




### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```




### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```




### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```




### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```




### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```




### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```




### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```




### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```




### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```




### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```




### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```




### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```




### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```




### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```




### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```




### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```




### ARC {#ARC}
```
public static int ARC
```




### ARROW {#ARROW}
```
public static int ARROW
```




### BALLOON {#BALLOON}
```
public static int BALLOON
```




### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```




### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```




### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```




### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```




### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```




### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```




### BEVEL {#BEVEL}
```
public static int BEVEL
```




### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```




### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```




### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```




### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```




### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```




### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```




### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```




### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```




### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```




### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```




### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```




### CAN {#CAN}
```
public static int CAN
```




### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


Chart plus.

 **Remarks:** 

Applicable only for DML shapes.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Chart star.

 **Remarks:** 

Applicable only for DML shapes.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Chart X.

 **Remarks:** 

Applicable only for DML shapes.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```




### CHORD {#CHORD}
```
public static int CHORD
```


Chord.

 **Remarks:** 

Applicable only for DML shapes.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```




### CLOUD {#CLOUD}
```
public static int CLOUD
```


Cloud.

 **Remarks:** 

Applicable only for DML shapes.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```




### CORNER {#CORNER}
```
public static int CORNER
```


Corner.

 **Remarks:** 

Applicable only for DML shapes.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Corner tabs.

 **Remarks:** 

Applicable only for DML shapes.

### CUBE {#CUBE}
```
public static int CUBE
```




### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```




### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```




### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```




### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```




### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```




### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```




### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```




### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```




### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


This shape type seems to be set for shapes that are not part of the standard set of the auto shapes in Microsoft Word. For example, if you insert a new auto shape from ClipArt.

You cannot create shapes of this type in the document.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Decagon.

 **Remarks:** 

Applicable only for DML shapes.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Round diagonal corner rectangle.

 **Remarks:** 

Applicable only for DML shapes.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Snip diagonal corner rectangle.

 **Remarks:** 

Applicable only for DML shapes.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Diagonal stripe.

 **Remarks:** 

Applicable only for DML shapes.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```




### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


Dodecagon.

 **Remarks:** 

Applicable only for DML shapes.

### DONUT {#DONUT}
```
public static int DONUT
```




### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```




### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```




### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```




### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```




### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```




### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```




### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```




### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```




### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```




### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```




### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```




### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```




### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```




### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```




### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```




### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```




### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```




### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```




### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```




### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```




### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```




### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```




### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```




### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```




### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```




### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```




### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```




### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```




### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```




### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```




### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```




### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```




### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```




### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```




### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```




### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```




### FRAME {#FRAME}
```
public static int FRAME
```


Frame.

 **Remarks:** 

Applicable only for DML shapes.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Funnel.

 **Remarks:** 

Applicable only for DML shapes.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Six-tooth gear.

 **Remarks:** 

Applicable only for DML shapes.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Nine-tooth gear.

 **Remarks:** 

Applicable only for DML shapes.

### GROUP {#GROUP}
```
public static int GROUP
```


The shape is a group shape.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Half frame.

 **Remarks:** 

Applicable only for DML shapes.

### HEART {#HEART}
```
public static int HEART
```




### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


Heptagon.

 **Remarks:** 

Applicable only for DML shapes.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```




### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```




### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```




### IMAGE {#IMAGE}
```
public static int IMAGE
```


The shape is an image.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Inverse line.

 **Remarks:** 

Applicable only for DML shapes.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```




### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```




### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```




### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```




### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```




### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```




### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


Left circular arrow.

 **Remarks:** 

Applicable only for DML shapes.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```




### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```




### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Left-right circular arrow.

 **Remarks:** 

Applicable only for DML shapes.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Left-right ribbon.

 **Remarks:** 

Applicable only for DML shapes.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```




### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```




### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```




### LINE {#LINE}
```
public static int LINE
```




### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


Math divide.

 **Remarks:** 

Applicable only for DML shapes.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Math equal.

 **Remarks:** 

Applicable only for DML shapes.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Math minus.

 **Remarks:** 

Applicable only for DML shapes.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Math multiply.

 **Remarks:** 

Applicable only for DML shapes.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Math not equal.

 **Remarks:** 

Applicable only for DML shapes.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Math plus.

 **Remarks:** 

Applicable only for DML shapes.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


Reserved for the system use.

### MOON {#MOON}
```
public static int MOON
```




### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


Non-isosceles trapezoid.

 **Remarks:** 

Applicable only for DML shapes.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


A shape drawn by user and consisting of multiple segments and/or vertices (curve, freeform or scribble).

You cannot create shapes of this type in the document.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```




### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```




### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```




### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


The shape is an ActiveX control.

You cannot create shapes of this type in the document.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


The shape is an OLE object.

You cannot create shapes of this type in the document.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```




### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```




### PIE {#PIE}
```
public static int PIE
```


Pie.

 **Remarks:** 

Applicable only for DML shapes.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```




### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


Plaque tabs.

 **Remarks:** 

Applicable only for DML shapes.

### PLUS {#PLUS}
```
public static int PLUS
```




### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```




### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```




### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```




### RIBBON {#RIBBON}
```
public static int RIBBON
```




### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```




### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```




### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```




### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```




### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```




### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```




### SEAL {#SEAL}
```
public static int SEAL
```




### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Ten-pointed star.

 **Remarks:** 

Applicable only for DML shapes.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Twelve-pointed star.

 **Remarks:** 

Applicable only for DML shapes.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```




### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```




### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```




### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```




### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Six-pointed star.

 **Remarks:** 

Applicable only for DML shapes.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Seven-pointed star.

 **Remarks:** 

Applicable only for DML shapes.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```




### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Round single corner rectangle.

 **Remarks:** 

Applicable only for DML shapes.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Snip single corner rectangle object.

 **Remarks:** 

Applicable only for DML shapes.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```




### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


Square tabs.

 **Remarks:** 

Applicable only for DML shapes.

### STAR {#STAR}
```
public static int STAR
```




### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```




### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```




### SUN {#SUN}
```
public static int SUN
```




### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


Swoosh arrow.

 **Remarks:** 

Applicable only for DML shapes.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Teardrop.

 **Remarks:** 

Applicable only for DML shapes.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


WordArt object.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


WordArt object.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


WordArt object.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


WordArt object.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


The shape is a textbox. Note that shapes of many other types can also have text inside them too. A shape does not have to have this type to contain text.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


WordArt object.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


WordArt object.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


WordArt object.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


WordArt object.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


WordArt object.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


WordArt object.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


WordArt object.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


WordArt object.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


WordArt object.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


WordArt object.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```




### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


WordArt object.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


WordArt object.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


WordArt object.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


WordArt object.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


WordArt object.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


WordArt object.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


WordArt object.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


WordArt object.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


WordArt object.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


WordArt object.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


WordArt object.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```




### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


WordArt object.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


WordArt object.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


WordArt object.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```




### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```




### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```




### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


WordArt object.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```




### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


WordArt object.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


WordArt object.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```




### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


WordArt object.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


WordArt object.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


WordArt object.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


WordArt object.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


WordArt object.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```




### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


WordArt object.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


WordArt object.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


WordArt object.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


WordArt object.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```




### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Snip and round single corner rectangle.

 **Remarks:** 

Applicable only for DML shapes.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Round same side corner rectangle.

 **Remarks:** 

Applicable only for DML shapes.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Snip same side corner rectangle.

 **Remarks:** 

Applicable only for DML shapes.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```




### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```




### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```




### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```




### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```




### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```




### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```




### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```




### WAVE {#WAVE}
```
public static int WAVE
```




### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```




### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Wedge pie.

 **Remarks:** 

Applicable only for DML shapes.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```




### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```




### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| Parameter | Type | Description |
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int shapeType) {#toString-int}
```
public static String toString(int shapeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

