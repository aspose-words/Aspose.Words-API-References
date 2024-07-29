---
title: ShapeType
linktitle: ShapeType
second_title: Aspose.Words for Java
description: Specifies the type of shape in a Microsoft Word document in Java.
type: docs
weight: 570
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
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Accent border callout 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Accent border callout 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Accent border callout 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | Accent border callout 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | An accent callout shape with one arrow. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | An accent callout shape with two arrows. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | An accent callout shape with three arrows. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | Accent callout 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Action button back previous. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Action button beginning. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Action button blank. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Action button document. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Action button end. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Action button forward next. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Action button help. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Action button home. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Action button information. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Action button movie. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Action button return. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Action button sound. |
| [ARC](#ARC) | Arc. |
| [ARROW](#ARROW) | Arrow. |
| [BALLOON](#BALLOON) | Balloon. |
| [BENT_ARROW](#BENT-ARROW) | Bent arrow. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | A bent connector shape with two segments. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | A bent connector shape with three segments. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | A bent connector shape with four segments. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | A bent connector shape with five segments. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Bent up arrow. |
| [BEVEL](#BEVEL) | Bevel. |
| [BLOCK_ARC](#BLOCK-ARC) | Block arc. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Border callout 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Border callout 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Border callout 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | Border callout 90. |
| [BRACE_PAIR](#BRACE-PAIR) | Brace pair |
| [BRACKET_PAIR](#BRACKET-PAIR) | Bracket pair. |
| [CALLOUT_1](#CALLOUT-1) | A callout shape with one arrow. |
| [CALLOUT_2](#CALLOUT-2) | A callout shape with two arrows. |
| [CALLOUT_3](#CALLOUT-3) | A callout shape with three arrows. |
| [CALLOUT_90](#CALLOUT-90) | Callout 90. |
| [CAN](#CAN) | Can. |
| [CHART_PLUS](#CHART-PLUS) | Chart plus. |
| [CHART_STAR](#CHART-STAR) | Chart star. |
| [CHART_X](#CHART-X) | Chart X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Chord. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Circular arrow. |
| [CLOUD](#CLOUD) | Cloud. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Cloud callout. |
| [CORNER](#CORNER) | Corner. |
| [CORNER_TABS](#CORNER-TABS) | Corner tabs. |
| [CUBE](#CUBE) | Cube. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | A curved connector shape with two segments. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | A curved connector shape with three segments. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | A curved connector shape with four segments. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | A curved connector shape with five segments. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Curved down arrow. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Curved left arrow. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Curved right arrow. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Curved up arrow |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | This shape type seems to be set for shapes that are not part of the standard set of the auto shapes in Microsoft Word. |
| [DECAGON](#DECAGON) | Decagon. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Round diagonal corner rectangle. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Snip diagonal corner rectangle. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Diagonal stripe. |
| [DIAMOND](#DIAMOND) | Diamond. |
| [DODECAGON](#DODECAGON) | Dodecagon. |
| [DONUT](#DONUT) | Donut. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Double wave. |
| [DOWN_ARROW](#DOWN-ARROW) | Down arrow. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Down arrow callout. |
| [ELLIPSE](#ELLIPSE) | Ellipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Ellipse ribbon. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Ellipse ribbon 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Flow chart alternate process. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Flow chart collate. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Flow chart connector. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Flow chart decision. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Flow chart delay. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Flow chart display. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Flow chart document. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Flow chart extract. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Flow chart input output. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Flow chart internal storage. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Flow chart magnetic disk. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Flow chart magnetic drum. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Flow char magnetic tape. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Flow chart manual input. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Flow chart manual operation. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Flow chart merge. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Flow chart multi document. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Flow chart off-line storage. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Flow chart off page connector. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Flow chart on-line storage. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Flow chart or. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Flow chart predefined process |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Flow chart preparation. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Flow chart process. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Flow chart punched card. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Flow chart punched tape. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Flow chart sort. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Flow chart summing junction. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Flow chart terminator. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Folded corner. |
| [FRAME](#FRAME) | Frame. |
| [FUNNEL](#FUNNEL) | Funnel. |
| [GEAR_6](#GEAR-6) | Six-tooth gear. |
| [GEAR_9](#GEAR-9) | Nine-tooth gear. |
| [GROUP](#GROUP) | The shape is a group shape. |
| [HALF_FRAME](#HALF-FRAME) | Half frame. |
| [HEART](#HEART) | Heart. |
| [HEPTAGON](#HEPTAGON) | Heptagon. |
| [HEXAGON](#HEXAGON) | Hexagon. |
| [HOME_PLATE](#HOME-PLATE) | Home plate. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Horizontal scroll. |
| [IMAGE](#IMAGE) | The shape is an image. |
| [INVERSE_LINE](#INVERSE-LINE) | Inverse line. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Irregular seal 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Irregular seal 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Left arrow. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Left arrow callout. |
| [LEFT_BRACE](#LEFT-BRACE) | Left brace. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Left bracket. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Left circular arrow. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Left right arrow. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Left right arrow callout. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Left-right circular arrow. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Left-right ribbon. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | Left right up arrow. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | Left up arrow. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | Lightning bolt. |
| [LINE](#LINE) | Line. |
| [MATH_DIVIDE](#MATH-DIVIDE) | Math divide. |
| [MATH_EQUAL](#MATH-EQUAL) | Math equal. |
| [MATH_MINUS](#MATH-MINUS) | Math minus. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Math multiply. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Math not equal. |
| [MATH_PLUS](#MATH-PLUS) | Math plus. |
| [MIN_VALUE](#MIN-VALUE) | Reserved for the system use. |
| [MOON](#MOON) | Moon. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Non-isosceles trapezoid. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | A shape drawn by user and consisting of multiple segments and/or vertices (curve, freeform or scribble). |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Notched right arrow. |
| [NO_SMOKING](#NO-SMOKING) | NoSmoking. |
| [OCTAGON](#OCTAGON) | Octagon. |
| [OLE_CONTROL](#OLE-CONTROL) | The shape is an ActiveX control. |
| [OLE_OBJECT](#OLE-OBJECT) | The shape is an OLE object. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallelogram. |
| [PENTAGON](#PENTAGON) | Pentagon. |
| [PIE](#PIE) | Pie. |
| [PLAQUE](#PLAQUE) | Plaque. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Plaque tabs. |
| [PLUS](#PLUS) | Plus. |
| [QUAD_ARROW](#QUAD-ARROW) | Quad arrow. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Quad arrow callout. |
| [RECTANGLE](#RECTANGLE) | Rectangle. |
| [RIBBON](#RIBBON) | Ribbon. |
| [RIBBON_2](#RIBBON-2) | Ribbon 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Right arrow callout |
| [RIGHT_BRACE](#RIGHT-BRACE) | Right brace. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Right bracket. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Right triangle. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Round rectangle. |
| [SEAL](#SEAL) | Seal. |
| [SEAL_10](#SEAL-10) | Ten-pointed star. |
| [SEAL_12](#SEAL-12) | Twelve-pointed star. |
| [SEAL_16](#SEAL-16) | 16-pointed star. |
| [SEAL_24](#SEAL-24) | 24-pointed star. |
| [SEAL_32](#SEAL-32) | 32-pointed star. |
| [SEAL_4](#SEAL-4) | Four-pointed star. |
| [SEAL_6](#SEAL-6) | Six-pointed star. |
| [SEAL_7](#SEAL-7) | Seven-pointed star. |
| [SEAL_8](#SEAL-8) | Eight-pointed star. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Round single corner rectangle. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Snip single corner rectangle object. |
| [SMILEY_FACE](#SMILEY-FACE) | Smiley face. |
| [SQUARE_TABS](#SQUARE-TABS) | Square tabs. |
| [STAR](#STAR) | Star. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | A straight connector shape. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Striped right arrow. |
| [SUN](#SUN) | Sun. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Swoosh arrow. |
| [TEARDROP](#TEARDROP) | Teardrop. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | Arch down curve, WordArt object. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | Arch down pour, WordArt object. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | Arch up curve, WordArt object. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | Arch up pour, WordArt object. |
| [TEXT_BOX](#TEXT-BOX) | The shape is a textbox. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | Button curve, WordArt object. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | Button pour, WordArt object. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | Can down, WordArt object. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | Can up, WordArt object. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | Cascade down, WordArt object. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | Cascade up, WordArt object. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | Chevron, WordArt object. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | Chevron inverted, WordArt object. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | Circle curve, WordArt object. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | Circle pour, WordArt object. |
| [TEXT_CURVE](#TEXT-CURVE) | Text curve. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | Curve down, WordArt object. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | Curve up, WordArt object. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | Deflate, WordArt object. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | Deflate bottom, WordArt object. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | Deflate inflate, WordArt object. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | Deflate inflate deflate, WordArt object. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | Deflate top, WordArt object. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | Fade down, WordArt object. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | Fade left, WordArt object. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | Fade right, WordArt object. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | Fade up, WordArt object. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | Text hexagon. |
| [TEXT_INFLATE](#TEXT-INFLATE) | Inflate, WordArt object. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | Inflate bottom, WordArt object. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | Inflate top, WordArt object. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | Text octagon. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | Text on curve. |
| [TEXT_ON_RING](#TEXT-ON-RING) | Text on ring. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | Plain-text, WordArt object. |
| [TEXT_RING](#TEXT-RING) | Text ring. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | Ring inside, WordArt object. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | Ring outside, WordArt object. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | Text simple. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | Slant down, WordArt object. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | Slant up, WordArt object. |
| [TEXT_STOP](#TEXT-STOP) | Stop, WordArt object. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | Triangle, WordArt object. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | Triangle inverted, WordArt object. |
| [TEXT_WAVE](#TEXT-WAVE) | Text wave. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | Wave 1, WordArt object. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | Wave 2, WordArt object. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | Wave 3, WordArt object. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | Wave 4, WordArt object. |
| [THICK_ARROW](#THICK-ARROW) | Thick arrow. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Snip and round single corner rectangle. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Round same side corner rectangle. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Snip same side corner rectangle. |
| [TRAPEZOID](#TRAPEZOID) | Trapezoid. |
| [TRIANGLE](#TRIANGLE) | Triangle. |
| [UP_ARROW](#UP-ARROW) | Up arrow. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Up arrow callout. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Up down arrow. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Up down arrow callout. |
| [UTURN_ARROW](#UTURN-ARROW) | Uturn arrow. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Vertical scroll. |
| [WAVE](#WAVE) | Wave. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Wedge ellipse callout. |
| [WEDGE_PIE](#WEDGE-PIE) | Wedge pie. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Wedge rect callout. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Wedge R rect callout. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Accent border callout 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Accent border callout 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Accent border callout 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


Accent border callout 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


An accent callout shape with one arrow.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


An accent callout shape with two arrows.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


An accent callout shape with three arrows.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


Accent callout 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Action button back previous.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Action button beginning.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Action button blank.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Action button document.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Action button end.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Action button forward next.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Action button help.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Action button home.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Action button information.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Action button movie.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Action button return.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Action button sound.

### ARC {#ARC}
```
public static int ARC
```


Arc.

### ARROW {#ARROW}
```
public static int ARROW
```


Arrow.

### BALLOON {#BALLOON}
```
public static int BALLOON
```


Balloon.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Bent arrow.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


A bent connector shape with two segments.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


A bent connector shape with three segments.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


A bent connector shape with four segments.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


A bent connector shape with five segments.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


Bent up arrow.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


Bevel.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


Block arc.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


Border callout 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Border callout 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Border callout 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


Border callout 90.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Brace pair

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Bracket pair.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


A callout shape with one arrow.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


A callout shape with two arrows.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


A callout shape with three arrows.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


Callout 90.

### CAN {#CAN}
```
public static int CAN
```


Can.

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


Chevron.

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


Circular arrow.

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


Cloud callout.

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


Cube.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


A curved connector shape with two segments.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


A curved connector shape with three segments.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


A curved connector shape with four segments.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


A curved connector shape with five segments.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


Curved down arrow.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


Curved left arrow.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


Curved right arrow.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


Curved up arrow

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


Diamond.

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


Donut.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


Double wave.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


Down arrow.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


Down arrow callout.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


Ellipse.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


Ellipse ribbon.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


Ellipse ribbon 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


Flow chart alternate process.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Flow chart collate.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Flow chart connector.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Flow chart decision.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Flow chart delay.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Flow chart display.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Flow chart document.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Flow chart extract.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Flow chart input output.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Flow chart internal storage.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Flow chart magnetic disk.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Flow chart magnetic drum.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Flow char magnetic tape.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Flow chart manual input.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Flow chart manual operation.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Flow chart merge.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Flow chart multi document.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Flow chart off-line storage.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Flow chart off page connector.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Flow chart on-line storage.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Flow chart or.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Flow chart predefined process

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Flow chart preparation.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Flow chart process.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Flow chart punched card.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Flow chart punched tape.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Flow chart sort.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Flow chart summing junction.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Flow chart terminator.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


Folded corner.

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


Heart.

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


Hexagon.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


Home plate.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


Horizontal scroll.

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


Irregular seal 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


Irregular seal 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


Left arrow.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


Left arrow callout.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


Left brace.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


Left bracket.

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


Left right arrow.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Left right arrow callout.

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


Left right up arrow.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


Left up arrow.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


Lightning bolt.

### LINE {#LINE}
```
public static int LINE
```


Line.

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


Moon.

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


Notched right arrow.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


NoSmoking.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Octagon.

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


Parallelogram.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


Pentagon.

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


Plaque.

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


Plus.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


Quad arrow.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


Quad arrow callout.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


Rectangle.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


Ribbon.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


Ribbon 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


Right arrow callout

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


Right brace.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


Right bracket.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


Right triangle.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


Round rectangle.

### SEAL {#SEAL}
```
public static int SEAL
```


Seal.

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


16-pointed star.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


24-pointed star.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


32-pointed star.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Four-pointed star.

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


Eight-pointed star.

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


Smiley face.

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


Star.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


A straight connector shape.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


Striped right arrow.

### SUN {#SUN}
```
public static int SUN
```


Sun.

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


Arch down curve, WordArt object.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


Arch down pour, WordArt object.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


Arch up curve, WordArt object.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


Arch up pour, WordArt object.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


The shape is a textbox. Note that shapes of many other types can also have text inside them too. A shape does not have to have this type to contain text.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


Button curve, WordArt object.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


Button pour, WordArt object.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


Can down, WordArt object.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


Can up, WordArt object.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


Cascade down, WordArt object.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


Cascade up, WordArt object.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


Chevron, WordArt object.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


Chevron inverted, WordArt object.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


Circle curve, WordArt object.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


Circle pour, WordArt object.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


Text curve.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


Curve down, WordArt object.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


Curve up, WordArt object.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


Deflate, WordArt object.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


Deflate bottom, WordArt object.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


Deflate inflate, WordArt object.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


Deflate inflate deflate, WordArt object.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


Deflate top, WordArt object.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


Fade down, WordArt object.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


Fade left, WordArt object.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


Fade right, WordArt object.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


Fade up, WordArt object.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


Text hexagon.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


Inflate, WordArt object.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


Inflate bottom, WordArt object.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


Inflate top, WordArt object.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


Text octagon.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


Text on curve.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


Text on ring.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


Plain-text, WordArt object.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


Text ring.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


Ring inside, WordArt object.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


Ring outside, WordArt object.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


Text simple.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


Slant down, WordArt object.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


Slant up, WordArt object.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


Stop, WordArt object.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


Triangle, WordArt object.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


Triangle inverted, WordArt object.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


Text wave.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


Wave 1, WordArt object.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


Wave 2, WordArt object.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


Wave 3, WordArt object.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


Wave 4, WordArt object.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


Thick arrow.

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


Trapezoid.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Triangle.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


Up arrow.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


Up arrow callout.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Up down arrow.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Up down arrow callout.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


Uturn arrow.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


Vertical scroll.

### WAVE {#WAVE}
```
public static int WAVE
```


Wave.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


Wedge ellipse callout.

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


Wedge rect callout.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Wedge R rect callout.

### length {#length}
```
public static int length
```


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
