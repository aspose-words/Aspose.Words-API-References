---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words für Java"
description: "Gibt den Formtyp von Diagrammelementen in Java an."
type: docs
weight: 90
url: /de/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

Gibt den Formtyp von Diagrammelementen an.

 **Examples:** 

Zeigt, wie Füllung, Kontur und Callout-Formatierung für Diagrammdatenbeschriftungen festgelegt werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Akzent-Callout mit Rand 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Akzent-Callout mit Rand 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Akzent-Callout mit Rand 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Akzent-Callout 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Akzent-Callout 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Akzent-Callout 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Zurück‑ oder Vorheriger‑Button. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Start‑Button. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Leerer Button. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Dokument‑Button. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Ende‑Button. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Vorwärts‑ oder Nächster‑Button. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Hilfe‑Button. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Home‑Button. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Informations‑Button. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Film‑Button. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Rückkehr‑Button. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Ton‑Button. |
| [ARC](#ARC) | Bogen. |
| [ARROW](#ARROW) | Pfeil. |
| [BENT_ARROW](#BENT-ARROW) | Gebogener Pfeil. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Gebogener Verbinder 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Gebogener Verbinder 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Gebogener Verbinder 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Gebogener Verbinder 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Gebogener Aufwärtspfeil. |
| [BEVEL](#BEVEL) | Fase. |
| [BLOCK_ARC](#BLOCK-ARC) | Blockbogen. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Hinweis mit Rand 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Hinweis mit Rand 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Hinweis mit Rand 3. |
| [BRACE_PAIR](#BRACE-PAIR) | Klammerpaar. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Klammerpaar. |
| [CALLOUT_1](#CALLOUT-1) | Hinweis 1. |
| [CALLOUT_2](#CALLOUT-2) | Hinweis 2. |
| [CALLOUT_3](#CALLOUT-3) | Hinweis 3. |
| [CAN](#CAN) | Dose. |
| [CHART_PLUS](#CHART-PLUS) | Diagramm Plus. |
| [CHART_STAR](#CHART-STAR) | Diagramm Stern. |
| [CHART_X](#CHART-X) | Diagramm X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Sehne. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Kreisförmiger Pfeil. |
| [CLOUD](#CLOUD) | Wolke. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Hinweiswolke. |
| [CORNER](#CORNER) | Ecke. |
| [CORNER_TABS](#CORNER-TABS) | Eckregister. |
| [CUBE](#CUBE) | Würfel. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Gebogener Verbinder 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Gebogener Verbinder 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Gebogener Verbinder 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Gebogener Verbinder 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Gebogener Pfeil nach unten. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Gebogener Pfeil nach links. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Gebogener Pfeil nach rechts. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Gebogener Pfeil nach oben. |
| [DECAGON](#DECAGON) | Zehneck. |
| [DEFAULT](#DEFAULT) | Zeigt an, dass für das Diagrammelement keine Form definiert ist. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Abgerundetes diagonales Eckrechteck. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Abgeschnittenes diagonales Eckrechteck. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Diagonaler Streifen. |
| [DIAMOND](#DIAMOND) | Raute. |
| [DODECAGON](#DODECAGON) | Zwölfeck. |
| [DONUT](#DONUT) | Donut. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Doppelte Welle. |
| [DOWN_ARROW](#DOWN-ARROW) | Pfeil nach unten. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Hinweis-Pfeil nach unten. |
| [ELLIPSE](#ELLIPSE) | Ellipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Ellipse-Band. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Ellipse-Band 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Alternativer Prozessablauf. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Zusammenstellungsfluss. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Verbindungsfluss. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Entscheidungsfluss. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Verzögerungsfluss. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Anzeigefluss. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Dokumentenfluss. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Extraktionsfluss. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Ein-/Ausgabefluss. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Interner Speicherfluss. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Magnetplattenfluss. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Magnettrommelfluss. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Magnetbandfluss. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Manueller Eingabefluss. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Manueller Betriebsfluss. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Zusammenführungsfluss. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Mehrdokumentenfluss. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Offline-Speicherfluss. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Off-Page-Connector-Fluss. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Online-Speicherfluss. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Oder-Fluss. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Vordefinierter Prozessfluss. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Vorbereitungsfluss. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Prozessfluss. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Lochkartenfluss. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Lochbandfluss. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Sortierfluss. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Summen-Knoten-Fluss. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Terminatorfluss. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Gefaltete Ecke. |
| [FRAME](#FRAME) | Rahmen. |
| [FUNNEL](#FUNNEL) | Trichter. |
| [GEAR_6](#GEAR-6) | Sechszahnrad. |
| [GEAR_9](#GEAR-9) | Neunzahnrad. |
| [HALF_FRAME](#HALF-FRAME) | Halbrahmen. |
| [HEART](#HEART) | Herz. |
| [HEPTAGON](#HEPTAGON) | Siebeneck. |
| [HEXAGON](#HEXAGON) | Sechseck. |
| [HOME_PLATE](#HOME-PLATE) | Heimatplatte. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Horizontaler Bildlauf. |
| [INVERSE_LINE](#INVERSE-LINE) | Umgekehrte Linie. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Unregelmäßige Dichtung 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Unregelmäßige Dichtung 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Pfeil nach links. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Hinweis-Pfeil nach links. |
| [LEFT_BRACE](#LEFT-BRACE) | Linke geschweifte Klammer. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Linke eckige Klammer. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Linker kreisförmiger Pfeil. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Pfeil nach links und rechts. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Hinweis-Pfeil nach links und rechts. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Links-rechts kreisförmiger Pfeil. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Links-rechts-Band. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | Links-rechts Aufwärts-Pfeil. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | Links Aufwärts-Pfeil. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | Blitz. |
| [LINE](#LINE) | Linie. |
| [MATH_DIVIDE](#MATH-DIVIDE) | Mathematisches Divisionszeichen. |
| [MATH_EQUAL](#MATH-EQUAL) | Mathematisches Gleichheitszeichen. |
| [MATH_MINUS](#MATH-MINUS) | Mathematisches Minuszeichen. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Mathematisches Malzeichen. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Mathematisches Ungleichheitszeichen. |
| [MATH_PLUS](#MATH-PLUS) | Mathematisches Pluszeichen. |
| [MOON](#MOON) | Mond. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Nicht-gleichschenkliges Trapez. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Gezackter rechter Pfeil. |
| [NO_SMOKING](#NO-SMOKING) | Rauchen verboten. |
| [OCTAGON](#OCTAGON) | Achtkant. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallelogramm. |
| [PENTAGON](#PENTAGON) | Fünfeck. |
| [PIE](#PIE) | Kuchen. |
| [PLAQUE](#PLAQUE) | Plakette. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Plaketten-Tabs. |
| [PLUS](#PLUS) | Plus. |
| [QUAD_ARROW](#QUAD-ARROW) | Vierfach-Pfeil. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Hinweis-Vierfach-Pfeil. |
| [RECTANGLE](#RECTANGLE) | Rechteck. |
| [RIBBON](#RIBBON) | Band. |
| [RIBBON_2](#RIBBON-2) | Band 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Hinweis rechter Pfeil. |
| [RIGHT_BRACE](#RIGHT-BRACE) | Rechte Klammer. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Rechte eckige Klammer. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Rechtes Dreieck. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Abgerundetes Rechteck. |
| [SEAL_10](#SEAL-10) | Zehnzackiger Stern. |
| [SEAL_12](#SEAL-12) | Zwölfzackiger Stern. |
| [SEAL_16](#SEAL-16) | Sechzehnzackiger Stern. |
| [SEAL_24](#SEAL-24) | Vierundzwanzigzackiger Stern. |
| [SEAL_32](#SEAL-32) | Zweiunddreißigzackiger Stern. |
| [SEAL_4](#SEAL-4) | Vierzackiger Stern. |
| [SEAL_6](#SEAL-6) | Sechszackiger Stern. |
| [SEAL_7](#SEAL-7) | Siebenzackiger Stern. |
| [SEAL_8](#SEAL-8) | Achtzackiger Stern. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Abgerundetes Rechteck mit einer Ecke. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Einseitiges Eckrechteck-Objekt zuschneiden. |
| [SMILEY_FACE](#SMILEY-FACE) | Smiley-Gesicht. |
| [SQUARE_TABS](#SQUARE-TABS) | Quadratische Register. |
| [STAR](#STAR) | Stern. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Gerader Verbinder 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Gestreifter rechter Pfeil. |
| [SUN](#SUN) | Sonne. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Schwungpfeil. |
| [TEARDROP](#TEARDROP) | Träne. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Abgeschnittener und abgerundeter einseitiger Rechteck. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Abgerundetes Rechteck mit Ecken auf derselben Seite. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Abgeschnittenes Rechteck mit Ecken auf derselben Seite. |
| [TRAPEZOID](#TRAPEZOID) | Trapez. |
| [TRIANGLE](#TRIANGLE) | Dreieck. |
| [UP_ARROW](#UP-ARROW) | Pfeil nach oben. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Beschriftungspfeil nach oben. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Pfeil nach oben und unten. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Beschriftungspfeil nach oben und unten. |
| [UTURN_ARROW](#UTURN-ARROW) | U-förmiger Pfeil. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Vertikaler Bildlauf. |
| [WAVE](#WAVE) | Welle. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Beschriftungskeilellipse. |
| [WEDGE_PIE](#WEDGE-PIE) | Keildiagramm. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Beschriftungskeilrechteck. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Beschriftungskeil abgerundetes Rechteck. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Akzent-Callout mit Rand 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Akzent-Callout mit Rand 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Akzent-Callout mit Rand 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Akzent-Callout 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Akzent-Callout 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Akzent-Callout 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Zurück‑ oder Vorheriger‑Button.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Start‑Button.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Leerer Button.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Dokument‑Button.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Ende‑Button.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Vorwärts‑ oder Nächster‑Button.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Hilfe‑Button.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Home‑Button.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Informations‑Button.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Film‑Button.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Rückkehr‑Button.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Ton‑Button.

### ARC {#ARC}
```
public static int ARC
```


Bogen.

### ARROW {#ARROW}
```
public static int ARROW
```


Pfeil.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Gebogener Pfeil.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Gebogener Verbinder 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Gebogener Verbinder 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Gebogener Verbinder 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Gebogener Verbinder 5.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


Gebogener Aufwärtspfeil.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


Fase.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


Blockbogen.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


Hinweis mit Rand 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Hinweis mit Rand 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Hinweis mit Rand 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Klammerpaar.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Klammerpaar.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Hinweis 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Hinweis 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Hinweis 3.

### CAN {#CAN}
```
public static int CAN
```


Dose.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


Diagramm Plus.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Diagramm Stern.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Diagramm X.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


Chevron.

### CHORD {#CHORD}
```
public static int CHORD
```


Sehne.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


Kreisförmiger Pfeil.

### CLOUD {#CLOUD}
```
public static int CLOUD
```


Wolke.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Hinweiswolke.

### CORNER {#CORNER}
```
public static int CORNER
```


Ecke.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Eckregister.

### CUBE {#CUBE}
```
public static int CUBE
```


Würfel.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Gebogener Verbinder 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Gebogener Verbinder 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Gebogener Verbinder 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Gebogener Verbinder 5.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


Gebogener Pfeil nach unten.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


Gebogener Pfeil nach links.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


Gebogener Pfeil nach rechts.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


Gebogener Pfeil nach oben.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Zehneck.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Zeigt an, dass für das Diagrammelement keine Form definiert ist.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Abgerundetes diagonales Eckrechteck.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Abgeschnittenes diagonales Eckrechteck.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Diagonaler Streifen.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Raute.

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


Zwölfeck.

### DONUT {#DONUT}
```
public static int DONUT
```


Donut.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


Doppelte Welle.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


Pfeil nach unten.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


Hinweis-Pfeil nach unten.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


Ellipse.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


Ellipse-Band.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


Ellipse-Band 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


Alternativer Prozessablauf.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Zusammenstellungsfluss.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Verbindungsfluss.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Entscheidungsfluss.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Verzögerungsfluss.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Anzeigefluss.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Dokumentenfluss.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Extraktionsfluss.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Ein-/Ausgabefluss.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Interner Speicherfluss.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Magnetplattenfluss.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Magnettrommelfluss.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Magnetbandfluss.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Manueller Eingabefluss.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Manueller Betriebsfluss.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Zusammenführungsfluss.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Mehrdokumentenfluss.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Offline-Speicherfluss.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Off-Page-Connector-Fluss.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Online-Speicherfluss.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Oder-Fluss.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Vordefinierter Prozessfluss.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Vorbereitungsfluss.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Prozessfluss.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Lochkartenfluss.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Lochbandfluss.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Sortierfluss.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Summen-Knoten-Fluss.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Terminatorfluss.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


Gefaltete Ecke.

### FRAME {#FRAME}
```
public static int FRAME
```


Rahmen.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Trichter.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Sechszahnrad.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Neunzahnrad.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Halbrahmen.

### HEART {#HEART}
```
public static int HEART
```


Herz.

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


Siebeneck.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


Sechseck.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


Heimatplatte.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


Horizontaler Bildlauf.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Umgekehrte Linie.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


Unregelmäßige Dichtung 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


Unregelmäßige Dichtung 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


Pfeil nach links.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


Hinweis-Pfeil nach links.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


Linke geschweifte Klammer.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


Linke eckige Klammer.

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


Linker kreisförmiger Pfeil.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Pfeil nach links und rechts.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Hinweis-Pfeil nach links und rechts.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Links-rechts kreisförmiger Pfeil.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Links-rechts-Band.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


Links-rechts Aufwärts-Pfeil.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


Links Aufwärts-Pfeil.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


Blitz.

### LINE {#LINE}
```
public static int LINE
```


Linie.

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


Mathematisches Divisionszeichen.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Mathematisches Gleichheitszeichen.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Mathematisches Minuszeichen.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Mathematisches Malzeichen.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Mathematisches Ungleichheitszeichen.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Mathematisches Pluszeichen.

### MOON {#MOON}
```
public static int MOON
```


Mond.

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


Nicht-gleichschenkliges Trapez.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Gezackter rechter Pfeil.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


Rauchen verboten.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Achtkant.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


Parallelogramm.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


Fünfeck.

### PIE {#PIE}
```
public static int PIE
```


Kuchen.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


Plakette.

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


Plaketten-Tabs.

### PLUS {#PLUS}
```
public static int PLUS
```


Plus.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


Vierfach-Pfeil.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


Hinweis-Vierfach-Pfeil.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


Rechteck.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


Band.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


Band 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


Hinweis rechter Pfeil.

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


Rechte Klammer.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


Rechte eckige Klammer.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


Rechtes Dreieck.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


Abgerundetes Rechteck.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Zehnzackiger Stern.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Zwölfzackiger Stern.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Sechzehnzackiger Stern.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Vierundzwanzigzackiger Stern.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Zweiunddreißigzackiger Stern.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Vierzackiger Stern.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Sechszackiger Stern.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Siebenzackiger Stern.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Achtzackiger Stern.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Abgerundetes Rechteck mit einer Ecke.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Einseitiges Eckrechteck-Objekt zuschneiden.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


Smiley-Gesicht.

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


Quadratische Register.

### STAR {#STAR}
```
public static int STAR
```


Stern.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Gerader Verbinder 1.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


Gestreifter rechter Pfeil.

### SUN {#SUN}
```
public static int SUN
```


Sonne.

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


Schwungpfeil.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Träne.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Abgeschnittener und abgerundeter einseitiger Rechteck.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Abgerundetes Rechteck mit Ecken auf derselben Seite.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Abgeschnittenes Rechteck mit Ecken auf derselben Seite.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


Trapez.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Dreieck.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


Pfeil nach oben.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


Beschriftungspfeil nach oben.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Pfeil nach oben und unten.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Beschriftungspfeil nach oben und unten.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


U-förmiger Pfeil.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


Vertikaler Bildlauf.

### WAVE {#WAVE}
```
public static int WAVE
```


Welle.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


Beschriftungskeilellipse.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Keildiagramm.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Beschriftungskeilrechteck.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Beschriftungskeil abgerundetes Rechteck.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
