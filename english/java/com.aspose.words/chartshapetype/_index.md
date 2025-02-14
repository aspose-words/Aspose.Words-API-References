---
title: ChartShapeType
linktitle: ChartShapeType
second_title: Aspose.Words for Java
description: Specifies the shape type of chart elements in Java.
type: docs
weight: 90
url: /java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

Specifies the shape type of chart elements.

 **Examples:** 

Shows how to set fill, stroke and callout formatting for chart data labels.

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
## Fields

| Field | Description |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Accent callout with border 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Accent callout with border 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Accent callout with border 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Accent callout 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Accent callout 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Accent callout 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Back or previous button. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Beginning button. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Blank button. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Document button. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | End button. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Forward or next button. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Help button. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Home button. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Information button. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Movie button. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Return button. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Sound button. |
| [ARC](#ARC) | Arc. |
| [ARROW](#ARROW) | Arrow. |
| [BENT_ARROW](#BENT-ARROW) | Bent arrow. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Bent connector 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Bent connector 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Bent connector 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Bent connector 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Bent up arrow. |
| [BEVEL](#BEVEL) | Bevel. |
| [BLOCK_ARC](#BLOCK-ARC) | Block arc. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Callout with border 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Callout with border 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Callout with border 3. |
| [BRACE_PAIR](#BRACE-PAIR) | Brace pair. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Bracket pair. |
| [CALLOUT_1](#CALLOUT-1) | Callout 1. |
| [CALLOUT_2](#CALLOUT-2) | Callout 2. |
| [CALLOUT_3](#CALLOUT-3) | Callout 3. |
| [CAN](#CAN) | Can. |
| [CHART_PLUS](#CHART-PLUS) | Chart plus. |
| [CHART_STAR](#CHART-STAR) | Chart star. |
| [CHART_X](#CHART-X) | Chart X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Chord. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Circular arrow. |
| [CLOUD](#CLOUD) | Cloud. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Callout cloud. |
| [CORNER](#CORNER) | Corner. |
| [CORNER_TABS](#CORNER-TABS) | Corner tabs. |
| [CUBE](#CUBE) | Cube. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Curved connector 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Curved connector 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Curved connector 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Curved connector 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Curved down arrow. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Curved left arrow. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Curved right arrow. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Curved up arrow. |
| [DECAGON](#DECAGON) | Decagon. |
| [DEFAULT](#DEFAULT) | Indicates that a shape is not defined for the chart element. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rounded diagonal corner rectangle. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Snip diagonal corner rectangle. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Diagonal stripe. |
| [DIAMOND](#DIAMOND) | Diamond. |
| [DODECAGON](#DODECAGON) | Dodecagon. |
| [DONUT](#DONUT) | Donut. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Double wave. |
| [DOWN_ARROW](#DOWN-ARROW) | Down arrow. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Callout down arrow. |
| [ELLIPSE](#ELLIPSE) | Ellipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Ellipse ribbon. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Ellipse ribbon 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Alternate process flow. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Collate flow. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Connector flow. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Decision flow. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Delay flow. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Display flow. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Document flow. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Extract flow. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Input output flow. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Internal storage flow. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Magnetic disk flow. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Magnetic drum flow. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Magnetic tape flow. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Manual input flow. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Manual operation flow. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Merge flow. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Multi-document flow. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Offline storage flow. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Off-page connector flow. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Online storage flow. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Or flow. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Predefined process flow. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Preparation flow. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Process flow. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Punched card flow. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Punched tape flow. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Sort flow. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Summing junction flow. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Terminator flow. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Folded corner. |
| [FRAME](#FRAME) | Frame. |
| [FUNNEL](#FUNNEL) | Funnel. |
| [GEAR_6](#GEAR-6) | Six-tooth gear. |
| [GEAR_9](#GEAR-9) | Nine-tooth gear. |
| [HALF_FRAME](#HALF-FRAME) | Half frame. |
| [HEART](#HEART) | Heart. |
| [HEPTAGON](#HEPTAGON) | Heptagon. |
| [HEXAGON](#HEXAGON) | Hexagon. |
| [HOME_PLATE](#HOME-PLATE) | Home plate. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Horizontal scroll. |
| [INVERSE_LINE](#INVERSE-LINE) | Inverse line. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Irregular seal 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Irregular seal 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Left arrow. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Callout left arrow. |
| [LEFT_BRACE](#LEFT-BRACE) | Left brace. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Left bracket. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Left circular arrow. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Left and right arrow. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Callout left and right arrow. |
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
| [MOON](#MOON) | Moon. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Non-isosceles trapezoid. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Notched right arrow. |
| [NO_SMOKING](#NO-SMOKING) | No smoking. |
| [OCTAGON](#OCTAGON) | Octagon. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallelogram. |
| [PENTAGON](#PENTAGON) | Pentagon. |
| [PIE](#PIE) | Pie. |
| [PLAQUE](#PLAQUE) | Plaque. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Plaque tabs. |
| [PLUS](#PLUS) | Plus. |
| [QUAD_ARROW](#QUAD-ARROW) | Quad arrow. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Callout quad arrow. |
| [RECTANGLE](#RECTANGLE) | Rectangle. |
| [RIBBON](#RIBBON) | Ribbon. |
| [RIBBON_2](#RIBBON-2) | Ribbon 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Callout right arrow. |
| [RIGHT_BRACE](#RIGHT-BRACE) | Right brace. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Right bracket. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Right triangle. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Rounded rectangle. |
| [SEAL_10](#SEAL-10) | Ten pointed star. |
| [SEAL_12](#SEAL-12) | Twelve pointed star. |
| [SEAL_16](#SEAL-16) | Sixteen pointed star. |
| [SEAL_24](#SEAL-24) | Twenty-four pointed star. |
| [SEAL_32](#SEAL-32) | Thirty-two pointed star. |
| [SEAL_4](#SEAL-4) | Four pointed star. |
| [SEAL_6](#SEAL-6) | Six pointed star. |
| [SEAL_7](#SEAL-7) | Seven pointed star. |
| [SEAL_8](#SEAL-8) | Eight pointed star. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rounded single corner rectangle. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Snip single corner rectangle object. |
| [SMILEY_FACE](#SMILEY-FACE) | Smiley face. |
| [SQUARE_TABS](#SQUARE-TABS) | Square tabs. |
| [STAR](#STAR) | Star. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Straight connector 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Striped right arrow. |
| [SUN](#SUN) | Sun. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Swoosh arrow. |
| [TEARDROP](#TEARDROP) | Teardrop. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Snip and round single corner rectangle. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rounded same side corner rectangle. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Snip same side corner rectangle. |
| [TRAPEZOID](#TRAPEZOID) | Trapezoid. |
| [TRIANGLE](#TRIANGLE) | Triangle. |
| [UP_ARROW](#UP-ARROW) | Up arrow. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Callout up arrow. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Up and down arrow. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Callout up and down arrow. |
| [UTURN_ARROW](#UTURN-ARROW) | U-turn arrow. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Vertical scroll. |
| [WAVE](#WAVE) | Wave. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Callout wedge ellipse. |
| [WEDGE_PIE](#WEDGE-PIE) | Wedge pie. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Callout wedge rectangle. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Callout wedge round rectangle. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Accent callout with border 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Accent callout with border 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Accent callout with border 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Accent callout 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Accent callout 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Accent callout 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Back or previous button.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Beginning button.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Blank button.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Document button.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


End button.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Forward or next button.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Help button.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Home button.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Information button.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Movie button.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Return button.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Sound button.

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

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Bent arrow.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Bent connector 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Bent connector 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Bent connector 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Bent connector 5.

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


Callout with border 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Callout with border 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Callout with border 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Brace pair.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Bracket pair.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Callout 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Callout 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Callout 3.

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

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Chart star.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Chart X.

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

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Callout cloud.

### CORNER {#CORNER}
```
public static int CORNER
```


Corner.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Corner tabs.

### CUBE {#CUBE}
```
public static int CUBE
```


Cube.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Curved connector 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Curved connector 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Curved connector 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Curved connector 5.

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


Curved up arrow.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Decagon.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Indicates that a shape is not defined for the chart element.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rounded diagonal corner rectangle.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Snip diagonal corner rectangle.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Diagonal stripe.

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


Callout down arrow.

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


Alternate process flow.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Collate flow.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Connector flow.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Decision flow.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Delay flow.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Display flow.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Document flow.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Extract flow.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Input output flow.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Internal storage flow.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Magnetic disk flow.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Magnetic drum flow.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Magnetic tape flow.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Manual input flow.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Manual operation flow.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Merge flow.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Multi-document flow.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Offline storage flow.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Off-page connector flow.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Online storage flow.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Or flow.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Predefined process flow.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Preparation flow.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Process flow.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Punched card flow.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Punched tape flow.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Sort flow.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Summing junction flow.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Terminator flow.

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

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Funnel.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Six-tooth gear.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Nine-tooth gear.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Half frame.

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

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Inverse line.

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


Callout left arrow.

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

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Left and right arrow.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Callout left and right arrow.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Left-right circular arrow.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Left-right ribbon.

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

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Math equal.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Math minus.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Math multiply.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Math not equal.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Math plus.

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

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Notched right arrow.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


No smoking.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Octagon.

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


Callout quad arrow.

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


Callout right arrow.

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


Rounded rectangle.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Ten pointed star.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Twelve pointed star.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Sixteen pointed star.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Twenty-four pointed star.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Thirty-two pointed star.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Four pointed star.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Six pointed star.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Seven pointed star.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Eight pointed star.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Rounded single corner rectangle.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Snip single corner rectangle object.

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

### STAR {#STAR}
```
public static int STAR
```


Star.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Straight connector 1.

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

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Teardrop.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Snip and round single corner rectangle.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rounded same side corner rectangle.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Snip same side corner rectangle.

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


Callout up arrow.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Up and down arrow.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Callout up and down arrow.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


U-turn arrow.

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


Callout wedge ellipse.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Wedge pie.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Callout wedge rectangle.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Callout wedge round rectangle.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
