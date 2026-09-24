---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de forma de los elementos del gráfico en Java."
type: docs
weight: 90
url: /es/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

Especifica el tipo de forma de los elementos del gráfico.

 **Examples:** 

Muestra cómo establecer el formato de relleno, trazo y llamada de atención para las etiquetas de datos del gráfico.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Llamada de atención acentuada con borde 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Llamada de atención acentuada con borde 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Llamada de atención acentuada con borde 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Llamada de atención 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Llamada de atención 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Llamada de atención 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Botón de retroceso o anterior. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Botón de inicio. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Botón en blanco. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Botón de documento. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Botón de fin. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Botón de avance o siguiente. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Botón de ayuda. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Botón de inicio. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Botón de información. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Botón de película. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Botón de retorno. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Botón de sonido. |
| [ARC](#ARC) | Arco. |
| [ARROW](#ARROW) | Flecha. |
| [BENT_ARROW](#BENT-ARROW) | Flecha doblada. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Conector doblado 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Conector doblado 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Conector doblado 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Conector doblado 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Flecha doblada hacia arriba. |
| [BEVEL](#BEVEL) | Bisel. |
| [BLOCK_ARC](#BLOCK-ARC) | Arco de bloque. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Globo con borde 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Globo con borde 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Globo con borde 3. |
| [BRACE_PAIR](#BRACE-PAIR) | Par de llaves. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Par de corchetes. |
| [CALLOUT_1](#CALLOUT-1) | Globo 1. |
| [CALLOUT_2](#CALLOUT-2) | Globo 2. |
| [CALLOUT_3](#CALLOUT-3) | Globo 3. |
| [CAN](#CAN) | Lata. |
| [CHART_PLUS](#CHART-PLUS) | Gráfico más. |
| [CHART_STAR](#CHART-STAR) | Gráfico estrella. |
| [CHART_X](#CHART-X) | Gráfico X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Cuerda. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Flecha circular. |
| [CLOUD](#CLOUD) | Nube. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Globo nube. |
| [CORNER](#CORNER) | Esquina. |
| [CORNER_TABS](#CORNER-TABS) | Pestañas de esquina. |
| [CUBE](#CUBE) | Cubo. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Conector curvo 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Conector curvo 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Conector curvo 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Conector curvo 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Flecha curva hacia abajo. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Flecha curva hacia la izquierda. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Flecha curva hacia la derecha. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Flecha curva hacia arriba. |
| [DECAGON](#DECAGON) | Decágono. |
| [DEFAULT](#DEFAULT) | Indica que una forma no está definida para el elemento del gráfico. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rectángulo de esquina diagonal redondeada. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Rectángulo de esquina diagonal recortada. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Raya diagonal. |
| [DIAMOND](#DIAMOND) | Rombo. |
| [DODECAGON](#DODECAGON) | Dodecágono. |
| [DONUT](#DONUT) | Rosquilla. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Onda doble. |
| [DOWN_ARROW](#DOWN-ARROW) | Flecha hacia abajo. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Globo de llamada con flecha hacia abajo. |
| [ELLIPSE](#ELLIPSE) | Elipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Cinta elíptica. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Cinta elíptica 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Flujo de proceso alternativo. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Flujo de compaginado. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Flujo de conector. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Flujo de decisión. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Flujo de retraso. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Flujo de visualización. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Flujo de documento. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Flujo de extracción. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Flujo de entrada y salida. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Flujo de almacenamiento interno. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Flujo de disco magnético. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Flujo de tambor magnético. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Flujo de cinta magnética. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Flujo de entrada manual. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Flujo de operación manual. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Flujo de fusión. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Flujo de múltiples documentos. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Flujo de almacenamiento fuera de línea. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Flujo de conector fuera de página. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Flujo de almacenamiento en línea. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Flujo OR. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Flujo de proceso predefinido. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Flujo de preparación. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Flujo de proceso. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Flujo de tarjeta perforada. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Flujo de cinta perforada. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Flujo de ordenación. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Flujo de unión sumadora. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Flujo de terminador. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Esquina doblada. |
| [FRAME](#FRAME) | Marco. |
| [FUNNEL](#FUNNEL) | Embudo. |
| [GEAR_6](#GEAR-6) | Engranaje de seis dientes. |
| [GEAR_9](#GEAR-9) | Engranaje de nueve dientes. |
| [HALF_FRAME](#HALF-FRAME) | Media marco. |
| [HEART](#HEART) | Corazón. |
| [HEPTAGON](#HEPTAGON) | Heptágono. |
| [HEXAGON](#HEXAGON) | Hexágono. |
| [HOME_PLATE](#HOME-PLATE) | Plato de home. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Desplazamiento horizontal. |
| [INVERSE_LINE](#INVERSE-LINE) | Línea inversa. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Sello irregular 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Sello irregular 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Flecha izquierda. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Llamada flecha izquierda. |
| [LEFT_BRACE](#LEFT-BRACE) | Llave izquierda. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Corchete izquierdo. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Flecha circular izquierda. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Flecha izquierda y derecha. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Llamada flecha izquierda y derecha. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Flecha circular izquierda-derecha. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Cinta izquierda-derecha. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | Flecha izquierda-derecha arriba. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | Flecha izquierda arriba. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | Rayo. |
| [LINE](#LINE) | Línea. |
| [MATH_DIVIDE](#MATH-DIVIDE) | División matemática. |
| [MATH_EQUAL](#MATH-EQUAL) | Igualdad matemática. |
| [MATH_MINUS](#MATH-MINUS) | Resta matemática. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Multiplicación matemática. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Desigualdad matemática. |
| [MATH_PLUS](#MATH-PLUS) | Suma matemática. |
| [MOON](#MOON) | Luna. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Trapecio no isósceles. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Flecha derecha con muesca. |
| [NO_SMOKING](#NO-SMOKING) | Prohibido fumar. |
| [OCTAGON](#OCTAGON) | Octágono. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Paralelogramo. |
| [PENTAGON](#PENTAGON) | Pentágono. |
| [PIE](#PIE) | Tarta. |
| [PLAQUE](#PLAQUE) | Placa. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Pestañas de placa. |
| [PLUS](#PLUS) | Más. |
| [QUAD_ARROW](#QUAD-ARROW) | Flecha cuádruple. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Flecha cuádruple de llamada. |
| [RECTANGLE](#RECTANGLE) | Rectángulo. |
| [RIBBON](#RIBBON) | Cinta. |
| [RIBBON_2](#RIBBON-2) | Cinta 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Llamada flecha derecha. |
| [RIGHT_BRACE](#RIGHT-BRACE) | Llave derecha. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Corchete derecho. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Triángulo rectángulo. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Rectángulo redondeado. |
| [SEAL_10](#SEAL-10) | Estrella de diez puntas. |
| [SEAL_12](#SEAL-12) | Estrella de doce puntas. |
| [SEAL_16](#SEAL-16) | Estrella de dieciséis puntas. |
| [SEAL_24](#SEAL-24) | Estrella de veinticuatro puntas. |
| [SEAL_32](#SEAL-32) | Estrella de treinta y dos puntas. |
| [SEAL_4](#SEAL-4) | Estrella de cuatro puntas. |
| [SEAL_6](#SEAL-6) | Estrella de seis puntas. |
| [SEAL_7](#SEAL-7) | Estrella de siete puntas. |
| [SEAL_8](#SEAL-8) | Estrella de ocho puntas. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rectángulo de una esquina redondeada. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Objeto de recorte de una esquina del rectángulo. |
| [SMILEY_FACE](#SMILEY-FACE) | Cara sonriente. |
| [SQUARE_TABS](#SQUARE-TABS) | Pestañas cuadradas. |
| [STAR](#STAR) | Estrella. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Conector recto 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Flecha derecha a rayas. |
| [SUN](#SUN) | Sol. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Flecha swoosh. |
| [TEARDROP](#TEARDROP) | Gota. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Rectángulo de una sola esquina recortada y redondeada. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rectángulo con esquinas del mismo lado redondeadas. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Rectángulo con esquina del mismo lado recortada. |
| [TRAPEZOID](#TRAPEZOID) | Trapecio. |
| [TRIANGLE](#TRIANGLE) | Triángulo. |
| [UP_ARROW](#UP-ARROW) | Flecha hacia arriba. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Flecha de llamada hacia arriba. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Flecha hacia arriba y abajo. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Flecha de llamada hacia arriba y abajo. |
| [UTURN_ARROW](#UTURN-ARROW) | Flecha de giro en U. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Desplazamiento vertical. |
| [WAVE](#WAVE) | Onda. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Cuña elíptica de llamada. |
| [WEDGE_PIE](#WEDGE-PIE) | Cuña de pastel. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Rectángulo de cuña de llamada. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Rectángulo redondeado de cuña de llamada. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Llamada de atención acentuada con borde 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Llamada de atención acentuada con borde 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Llamada de atención acentuada con borde 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Llamada de atención 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Llamada de atención 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Llamada de atención 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Botón de retroceso o anterior.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Botón de inicio.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Botón en blanco.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Botón de documento.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Botón de fin.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Botón de avance o siguiente.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Botón de ayuda.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Botón de inicio.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Botón de información.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Botón de película.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Botón de retorno.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Botón de sonido.

### ARC {#ARC}
```
public static int ARC
```


Arco.

### ARROW {#ARROW}
```
public static int ARROW
```


Flecha.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Flecha doblada.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Conector doblado 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Conector doblado 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Conector doblado 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Conector doblado 5.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


Flecha doblada hacia arriba.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


Bisel.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


Arco de bloque.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


Globo con borde 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Globo con borde 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Globo con borde 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Par de llaves.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Par de corchetes.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Globo 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Globo 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Globo 3.

### CAN {#CAN}
```
public static int CAN
```


Lata.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


Gráfico más.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Gráfico estrella.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Gráfico X.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


Chevron.

### CHORD {#CHORD}
```
public static int CHORD
```


Cuerda.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


Flecha circular.

### CLOUD {#CLOUD}
```
public static int CLOUD
```


Nube.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Globo nube.

### CORNER {#CORNER}
```
public static int CORNER
```


Esquina.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Pestañas de esquina.

### CUBE {#CUBE}
```
public static int CUBE
```


Cubo.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Conector curvo 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Conector curvo 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Conector curvo 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Conector curvo 5.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


Flecha curva hacia abajo.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


Flecha curva hacia la izquierda.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


Flecha curva hacia la derecha.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


Flecha curva hacia arriba.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Decágono.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Indica que una forma no está definida para el elemento del gráfico.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rectángulo de esquina diagonal redondeada.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Rectángulo de esquina diagonal recortada.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Raya diagonal.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Rombo.

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


Dodecágono.

### DONUT {#DONUT}
```
public static int DONUT
```


Rosquilla.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


Onda doble.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


Flecha hacia abajo.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


Globo de llamada con flecha hacia abajo.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


Elipse.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


Cinta elíptica.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


Cinta elíptica 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


Flujo de proceso alternativo.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Flujo de compaginado.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Flujo de conector.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Flujo de decisión.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Flujo de retraso.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Flujo de visualización.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Flujo de documento.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Flujo de extracción.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Flujo de entrada y salida.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Flujo de almacenamiento interno.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Flujo de disco magnético.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Flujo de tambor magnético.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Flujo de cinta magnética.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Flujo de entrada manual.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Flujo de operación manual.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Flujo de fusión.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Flujo de múltiples documentos.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Flujo de almacenamiento fuera de línea.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Flujo de conector fuera de página.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Flujo de almacenamiento en línea.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Flujo OR.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Flujo de proceso predefinido.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Flujo de preparación.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Flujo de proceso.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Flujo de tarjeta perforada.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Flujo de cinta perforada.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Flujo de ordenación.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Flujo de unión sumadora.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Flujo de terminador.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


Esquina doblada.

### FRAME {#FRAME}
```
public static int FRAME
```


Marco.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Embudo.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Engranaje de seis dientes.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Engranaje de nueve dientes.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Media marco.

### HEART {#HEART}
```
public static int HEART
```


Corazón.

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


Heptágono.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


Hexágono.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


Plato de home.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


Desplazamiento horizontal.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Línea inversa.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


Sello irregular 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


Sello irregular 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


Flecha izquierda.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


Llamada flecha izquierda.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


Llave izquierda.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


Corchete izquierdo.

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


Flecha circular izquierda.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Flecha izquierda y derecha.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Llamada flecha izquierda y derecha.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Flecha circular izquierda-derecha.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Cinta izquierda-derecha.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


Flecha izquierda-derecha arriba.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


Flecha izquierda arriba.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


Rayo.

### LINE {#LINE}
```
public static int LINE
```


Línea.

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


División matemática.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Igualdad matemática.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Resta matemática.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Multiplicación matemática.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Desigualdad matemática.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Suma matemática.

### MOON {#MOON}
```
public static int MOON
```


Luna.

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


Trapecio no isósceles.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Flecha derecha con muesca.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


Prohibido fumar.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Octágono.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


Paralelogramo.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


Pentágono.

### PIE {#PIE}
```
public static int PIE
```


Tarta.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


Placa.

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


Pestañas de placa.

### PLUS {#PLUS}
```
public static int PLUS
```


Más.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


Flecha cuádruple.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


Flecha cuádruple de llamada.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


Rectángulo.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


Cinta.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


Cinta 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


Llamada flecha derecha.

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


Llave derecha.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


Corchete derecho.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


Triángulo rectángulo.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


Rectángulo redondeado.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Estrella de diez puntas.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Estrella de doce puntas.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Estrella de dieciséis puntas.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Estrella de veinticuatro puntas.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Estrella de treinta y dos puntas.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Estrella de cuatro puntas.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Estrella de seis puntas.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Estrella de siete puntas.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Estrella de ocho puntas.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Rectángulo de una esquina redondeada.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Objeto de recorte de una esquina del rectángulo.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


Cara sonriente.

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


Pestañas cuadradas.

### STAR {#STAR}
```
public static int STAR
```


Estrella.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Conector recto 1.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


Flecha derecha a rayas.

### SUN {#SUN}
```
public static int SUN
```


Sol.

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


Flecha swoosh.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Gota.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Rectángulo de una sola esquina recortada y redondeada.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rectángulo con esquinas del mismo lado redondeadas.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Rectángulo con esquina del mismo lado recortada.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


Trapecio.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Triángulo.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


Flecha hacia arriba.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


Flecha de llamada hacia arriba.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Flecha hacia arriba y abajo.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Flecha de llamada hacia arriba y abajo.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


Flecha de giro en U.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


Desplazamiento vertical.

### WAVE {#WAVE}
```
public static int WAVE
```


Onda.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


Cuña elíptica de llamada.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Cuña de pastel.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Rectángulo de cuña de llamada.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Rectángulo redondeado de cuña de llamada.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
