---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di forma degli elementi del grafico in Java."
type: docs
weight: 90
url: /it/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

Specifica il tipo di forma degli elementi del grafico.

 **Examples:** 

Mostra come impostare il riempimento, il tratto e la formattazione delle note a margine per le etichette dei dati del grafico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Nota a margine accentuata con bordo 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Nota a margine accentuata con bordo 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Nota a margine accentuata con bordo 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Nota a margine accentuata 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Nota a margine accentuata 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Nota a margine accentuata 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Pulsante Indietro o Precedente. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Pulsante Inizio. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Pulsante Vuoto. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Pulsante Documento. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Pulsante Fine. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Pulsante Avanti o Successivo. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Pulsante Aiuto. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Pulsante Home. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Pulsante Informazioni. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Pulsante Film. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Pulsante Ritorno. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Pulsante Suono. |
| [ARC](#ARC) | Arco. |
| [ARROW](#ARROW) | Freccia. |
| [BENT_ARROW](#BENT-ARROW) | Freccia piegata. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Connettore piegato 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Connettore piegato 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Connettore piegato 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Connettore piegato 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Freccia piegata verso l'alto. |
| [BEVEL](#BEVEL) | Smussatura. |
| [BLOCK_ARC](#BLOCK-ARC) | Arco a blocco. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Didascalia con bordo 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Didascalia con bordo 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Didascalia con bordo 3. |
| [BRACE_PAIR](#BRACE-PAIR) | Coppia di graffe. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Coppia di parentesi quadre. |
| [CALLOUT_1](#CALLOUT-1) | Didascalia 1. |
| [CALLOUT_2](#CALLOUT-2) | Didascalia 2. |
| [CALLOUT_3](#CALLOUT-3) | Didascalia 3. |
| [CAN](#CAN) | Lattina. |
| [CHART_PLUS](#CHART-PLUS) | Grafico più. |
| [CHART_STAR](#CHART-STAR) | Grafico stella. |
| [CHART_X](#CHART-X) | Grafico X. |
| [CHEVRON](#CHEVRON) | Freccia a V. |
| [CHORD](#CHORD) | Corda. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Freccia circolare. |
| [CLOUD](#CLOUD) | Nuvola. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Didascalia nuvola. |
| [CORNER](#CORNER) | Angolo. |
| [CORNER_TABS](#CORNER-TABS) | Schede d'angolo. |
| [CUBE](#CUBE) | Cubo. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Connettore curvo 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Connettore curvo 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Connettore curvo 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Connettore curvo 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Freccia curva verso il basso. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Freccia curva verso sinistra. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Freccia curva verso destra. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Freccia curva verso l'alto. |
| [DECAGON](#DECAGON) | Decagono. |
| [DEFAULT](#DEFAULT) | Indica che una forma non è definita per l'elemento del grafico. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rettangolo con angolo diagonale arrotondato. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Rettangolo con angolo diagonale tagliato. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Striscia diagonale. |
| [DIAMOND](#DIAMOND) | Diamante. |
| [DODECAGON](#DODECAGON) | Dodecagono. |
| [DONUT](#DONUT) | Ciambella. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Onda doppia. |
| [DOWN_ARROW](#DOWN-ARROW) | Freccia verso il basso. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Freccia verso il basso con callout. |
| [ELLIPSE](#ELLIPSE) | Ellisse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Nastro ellittico. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Nastro ellittico 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Flusso di processo alternativo. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Flusso di raggruppamento. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Flusso di connettore. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Flusso decisionale. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Flusso di ritardo. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Flusso di visualizzazione. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Flusso di documento. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Flusso di estrazione. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Flusso di input/output. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Flusso di archiviazione interna. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Flusso di disco magnetico. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Flusso di tamburo magnetico. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Flusso di nastro magnetico. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Flusso di input manuale. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Flusso di operazione manuale. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Flusso di unione. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Flusso multi-documento. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Flusso di archiviazione offline. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Flusso di connettore fuori pagina. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Flusso di archiviazione online. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Flusso OR. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Flusso di processo predefinito. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Flusso di preparazione. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Flusso di processo. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Flusso di scheda perforata. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Flusso di nastro perforato. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Flusso di ordinamento. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Flusso di giunzione di somma. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Flusso di terminatore. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Angolo piegato. |
| [FRAME](#FRAME) | Cornice. |
| [FUNNEL](#FUNNEL) | Imbuto. |
| [GEAR_6](#GEAR-6) | Ingranaggio a sei denti. |
| [GEAR_9](#GEAR-9) | Ingranaggio a nove denti. |
| [HALF_FRAME](#HALF-FRAME) | Mezza cornice. |
| [HEART](#HEART) | Cuore. |
| [HEPTAGON](#HEPTAGON) | Ettagono. |
| [HEXAGON](#HEXAGON) | Esagono. |
| [HOME_PLATE](#HOME-PLATE) | Casa base. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Scorrimento orizzontale. |
| [INVERSE_LINE](#INVERSE-LINE) | Linea inversa. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Sigillo irregolare 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Sigillo irregolare 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Freccia sinistra. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Freccia sinistra di richiamo. |
| [LEFT_BRACE](#LEFT-BRACE) | Graffa sinistra. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Parentesi quadra sinistra. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Freccia circolare sinistra. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Freccia sinistra e destra. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Freccia sinistra e destra di richiamo. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Freccia circolare sinistra-destra. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Nastro sinistra-destra. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | Freccia sinistra-destra verso l'alto. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | Freccia sinistra verso l'alto. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | Fulmine. |
| [LINE](#LINE) | Linea. |
| [MATH_DIVIDE](#MATH-DIVIDE) | Divisione matematica. |
| [MATH_EQUAL](#MATH-EQUAL) | Uguale matematico. |
| [MATH_MINUS](#MATH-MINUS) | Meno matematico. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Moltiplicazione matematica. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Diverso matematico. |
| [MATH_PLUS](#MATH-PLUS) | Più matematico. |
| [MOON](#MOON) | Luna. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Trapezio non isoscele. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Freccia destra dentata. |
| [NO_SMOKING](#NO-SMOKING) | Divieto di fumare. |
| [OCTAGON](#OCTAGON) | Ottagono. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallelogramma. |
| [PENTAGON](#PENTAGON) | Pentagono. |
| [PIE](#PIE) | Torta. |
| [PLAQUE](#PLAQUE) | Targa. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Schede della targa. |
| [PLUS](#PLUS) | Più. |
| [QUAD_ARROW](#QUAD-ARROW) | Freccia a quattro punte. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Richiamo con freccia a quattro punte. |
| [RECTANGLE](#RECTANGLE) | Rettangolo. |
| [RIBBON](#RIBBON) | Nastro. |
| [RIBBON_2](#RIBBON-2) | Nastro 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Freccia a destra della didascalia. |
| [RIGHT_BRACE](#RIGHT-BRACE) | Graffa destra. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Parentesi destra. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Triangolo rettangolo. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Rettangolo arrotondato. |
| [SEAL_10](#SEAL-10) | Stella a dieci punte. |
| [SEAL_12](#SEAL-12) | Stella a dodici punte. |
| [SEAL_16](#SEAL-16) | Stella a sedici punte. |
| [SEAL_24](#SEAL-24) | Stella a ventiquattro punte. |
| [SEAL_32](#SEAL-32) | Stella a trentadue punte. |
| [SEAL_4](#SEAL-4) | Stella a quattro punte. |
| [SEAL_6](#SEAL-6) | Stella a sei punte. |
| [SEAL_7](#SEAL-7) | Stella a sette punte. |
| [SEAL_8](#SEAL-8) | Stella a otto punte. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rettangolo con un angolo arrotondato. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Oggetto rettangolo a un angolo tagliato. |
| [SMILEY_FACE](#SMILEY-FACE) | Faccina sorridente. |
| [SQUARE_TABS](#SQUARE-TABS) | Schede quadrate. |
| [STAR](#STAR) | Stella. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Connettore dritto 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Freccia destra a strisce. |
| [SUN](#SUN) | Sole. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Freccia a scatto. |
| [TEARDROP](#TEARDROP) | Goccia. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Rettangolo a singolo angolo ritagliato e arrotondato. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rettangolo con angolo arrotondato sullo stesso lato. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Rettangolo con angolo ritagliato sullo stesso lato. |
| [TRAPEZOID](#TRAPEZOID) | Trapezio. |
| [TRIANGLE](#TRIANGLE) | Triangolo. |
| [UP_ARROW](#UP-ARROW) | Freccia verso l'alto. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Freccia di richiamo verso l'alto. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Freccia su e giù. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Freccia di richiamo su e giù. |
| [UTURN_ARROW](#UTURN-ARROW) | Freccia a inversione a U. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Scorrimento verticale. |
| [WAVE](#WAVE) | Onda. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Fetta ellittica di richiamo. |
| [WEDGE_PIE](#WEDGE-PIE) | Fetta di torta. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Fetta rettangolare di richiamo. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Fetta rettangolare arrotondata di richiamo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Nota a margine accentuata con bordo 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Nota a margine accentuata con bordo 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Nota a margine accentuata con bordo 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Nota a margine accentuata 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Nota a margine accentuata 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Nota a margine accentuata 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Pulsante Indietro o Precedente.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Pulsante Inizio.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Pulsante Vuoto.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Pulsante Documento.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Pulsante Fine.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Pulsante Avanti o Successivo.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Pulsante Aiuto.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Pulsante Home.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Pulsante Informazioni.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Pulsante Film.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Pulsante Ritorno.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Pulsante Suono.

### ARC {#ARC}
```
public static int ARC
```


Arco.

### ARROW {#ARROW}
```
public static int ARROW
```


Freccia.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Freccia piegata.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Connettore piegato 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Connettore piegato 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Connettore piegato 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Connettore piegato 5.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


Freccia piegata verso l'alto.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


Smussatura.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


Arco a blocco.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


Didascalia con bordo 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Didascalia con bordo 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Didascalia con bordo 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Coppia di graffe.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Coppia di parentesi quadre.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Didascalia 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Didascalia 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Didascalia 3.

### CAN {#CAN}
```
public static int CAN
```


Lattina.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


Grafico più.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Grafico stella.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Grafico X.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


Freccia a V.

### CHORD {#CHORD}
```
public static int CHORD
```


Corda.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


Freccia circolare.

### CLOUD {#CLOUD}
```
public static int CLOUD
```


Nuvola.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Didascalia nuvola.

### CORNER {#CORNER}
```
public static int CORNER
```


Angolo.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Schede d'angolo.

### CUBE {#CUBE}
```
public static int CUBE
```


Cubo.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Connettore curvo 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Connettore curvo 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Connettore curvo 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Connettore curvo 5.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


Freccia curva verso il basso.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


Freccia curva verso sinistra.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


Freccia curva verso destra.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


Freccia curva verso l'alto.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Decagono.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Indica che una forma non è definita per l'elemento del grafico.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rettangolo con angolo diagonale arrotondato.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Rettangolo con angolo diagonale tagliato.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Striscia diagonale.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Diamante.

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


Dodecagono.

### DONUT {#DONUT}
```
public static int DONUT
```


Ciambella.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


Onda doppia.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


Freccia verso il basso.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


Freccia verso il basso con callout.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


Ellisse.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


Nastro ellittico.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


Nastro ellittico 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


Flusso di processo alternativo.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Flusso di raggruppamento.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Flusso di connettore.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Flusso decisionale.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Flusso di ritardo.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Flusso di visualizzazione.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Flusso di documento.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Flusso di estrazione.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Flusso di input/output.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Flusso di archiviazione interna.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Flusso di disco magnetico.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Flusso di tamburo magnetico.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Flusso di nastro magnetico.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Flusso di input manuale.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Flusso di operazione manuale.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Flusso di unione.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Flusso multi-documento.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Flusso di archiviazione offline.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Flusso di connettore fuori pagina.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Flusso di archiviazione online.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Flusso OR.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Flusso di processo predefinito.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Flusso di preparazione.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Flusso di processo.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Flusso di scheda perforata.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Flusso di nastro perforato.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Flusso di ordinamento.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Flusso di giunzione di somma.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Flusso di terminatore.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


Angolo piegato.

### FRAME {#FRAME}
```
public static int FRAME
```


Cornice.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Imbuto.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Ingranaggio a sei denti.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Ingranaggio a nove denti.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Mezza cornice.

### HEART {#HEART}
```
public static int HEART
```


Cuore.

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


Ettagono.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


Esagono.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


Casa base.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


Scorrimento orizzontale.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Linea inversa.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


Sigillo irregolare 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


Sigillo irregolare 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


Freccia sinistra.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


Freccia sinistra di richiamo.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


Graffa sinistra.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


Parentesi quadra sinistra.

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


Freccia circolare sinistra.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Freccia sinistra e destra.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Freccia sinistra e destra di richiamo.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Freccia circolare sinistra-destra.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Nastro sinistra-destra.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


Freccia sinistra-destra verso l'alto.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


Freccia sinistra verso l'alto.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


Fulmine.

### LINE {#LINE}
```
public static int LINE
```


Linea.

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


Divisione matematica.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Uguale matematico.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Meno matematico.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Moltiplicazione matematica.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Diverso matematico.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Più matematico.

### MOON {#MOON}
```
public static int MOON
```


Luna.

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


Trapezio non isoscele.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Freccia destra dentata.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


Divieto di fumare.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Ottagono.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


Parallelogramma.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


Pentagono.

### PIE {#PIE}
```
public static int PIE
```


Torta.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


Targa.

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


Schede della targa.

### PLUS {#PLUS}
```
public static int PLUS
```


Più.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


Freccia a quattro punte.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


Richiamo con freccia a quattro punte.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


Rettangolo.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


Nastro.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


Nastro 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


Freccia a destra della didascalia.

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


Graffa destra.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


Parentesi destra.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


Triangolo rettangolo.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


Rettangolo arrotondato.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Stella a dieci punte.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Stella a dodici punte.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Stella a sedici punte.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Stella a ventiquattro punte.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Stella a trentadue punte.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Stella a quattro punte.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Stella a sei punte.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Stella a sette punte.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Stella a otto punte.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Rettangolo con un angolo arrotondato.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Oggetto rettangolo a un angolo tagliato.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


Faccina sorridente.

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


Schede quadrate.

### STAR {#STAR}
```
public static int STAR
```


Stella.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Connettore dritto 1.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


Freccia destra a strisce.

### SUN {#SUN}
```
public static int SUN
```


Sole.

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


Freccia a scatto.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Goccia.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Rettangolo a singolo angolo ritagliato e arrotondato.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rettangolo con angolo arrotondato sullo stesso lato.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Rettangolo con angolo ritagliato sullo stesso lato.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


Trapezio.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Triangolo.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


Freccia verso l'alto.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


Freccia di richiamo verso l'alto.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Freccia su e giù.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Freccia di richiamo su e giù.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


Freccia a inversione a U.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


Scorrimento verticale.

### WAVE {#WAVE}
```
public static int WAVE
```


Onda.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


Fetta ellittica di richiamo.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Fetta di torta.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Fetta rettangolare di richiamo.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Fetta rettangolare arrotondata di richiamo.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
