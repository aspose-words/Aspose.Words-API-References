---
title: "ShapeType"
linktitle: "ShapeType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ der Form in einem Microsoft Word-Dokument in Java an."
type: docs
weight: 618
url: /de/java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

Gibt den Typ einer Form in einem Microsoft‑Word‑Dokument an.

 **Examples:** 

Zeigt, wie man eine Form mit einem Bild aus dem lokalen Dateisystem in ein Dokument einfügt.

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

Zeigt, wie Aspose.Words Formen erkennt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Akzentrahmen-Anmerkung 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Akzentrahmen-Anmerkung 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Akzentrahmen-Anmerkung 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | Akzentrahmen-Anmerkung 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Eine Akzent-Anmerkungsform mit einem Pfeil. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Eine Akzent-Anmerkungsform mit zwei Pfeilen. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Eine Akzent-Anmerkungsform mit drei Pfeilen. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | Akzent-Anmerkung 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Aktionsschaltfläche zurück vorherige. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Aktionsschaltfläche Anfang. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Aktionsschaltfläche leer. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Aktionsschaltfläche Dokument. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Aktionsschaltfläche Ende. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Aktionsschaltfläche weiter nächste. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Aktionsschaltfläche Hilfe. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Aktionsschaltfläche Start. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Aktionsschaltfläche Informationen. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Aktionsschaltfläche Film. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Aktionsschaltfläche Zurück. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Aktionsschaltfläche Ton. |
| [ARC](#ARC) | Bogen. |
| [ARROW](#ARROW) | Pfeil. |
| [BALLOON](#BALLOON) | Ballon. |
| [BENT_ARROW](#BENT-ARROW) | Gebogener Pfeil. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Eine gebogene Verbinderform mit zwei Segmenten. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Eine gebogene Verbinderform mit drei Segmenten. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Eine gebogene Verbinderform mit vier Segmenten. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Eine gebogene Verbinderform mit fünf Segmenten. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Gebogener Aufwärtspfeil. |
| [BEVEL](#BEVEL) | Fase. |
| [BLOCK_ARC](#BLOCK-ARC) | Blockbogen. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Randbeschriftung 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Randbeschriftung 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Randbeschriftung 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | Randbeschriftung 90. |
| [BRACE_PAIR](#BRACE-PAIR) | Klammerpaar |
| [BRACKET_PAIR](#BRACKET-PAIR) | Klammerpaar. |
| [CALLOUT_1](#CALLOUT-1) | Eine Beschriftungsform mit einem Pfeil. |
| [CALLOUT_2](#CALLOUT-2) | Eine Beschriftungsform mit zwei Pfeilen. |
| [CALLOUT_3](#CALLOUT-3) | Eine Beschriftungsform mit drei Pfeilen. |
| [CALLOUT_90](#CALLOUT-90) | Beschriftung 90. |
| [CAN](#CAN) | Dose. |
| [CHART_PLUS](#CHART-PLUS) | Diagramm Plus. |
| [CHART_STAR](#CHART-STAR) | Diagramm Stern. |
| [CHART_X](#CHART-X) | Diagramm X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Sehne. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Kreisförmiger Pfeil. |
| [CLOUD](#CLOUD) | Wolke. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Wolkenbeschriftung. |
| [CORNER](#CORNER) | Ecke. |
| [CORNER_TABS](#CORNER-TABS) | Eckregister. |
| [CUBE](#CUBE) | Würfel. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Eine gekrümmte Verbinderform mit zwei Segmenten. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Eine gekrümmte Verbinderform mit drei Segmenten. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Eine gekrümmte Verbinderform mit vier Segmenten. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Eine gekrümmte Verbinderform mit fünf Segmenten. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Gebogener Pfeil nach unten. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Gebogener Pfeil nach links. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Gebogener Pfeil nach rechts. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Gekrümmter Aufwärtspfeil |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | Dieser Formtyp scheint für Formen festgelegt zu sein, die nicht Teil des Standardsatzes der Autoformen in Microsoft Word sind. |
| [DECAGON](#DECAGON) | Zehneck. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rundes Rechteck mit diagonaler Ecke. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Abgeschnittenes diagonales Eckrechteck. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Diagonaler Streifen. |
| [DIAMOND](#DIAMOND) | Raute. |
| [DODECAGON](#DODECAGON) | Zwölfeck. |
| [DONUT](#DONUT) | Donut. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Doppelte Welle. |
| [DOWN_ARROW](#DOWN-ARROW) | Pfeil nach unten. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Abwärtspfeil-Anmerkung. |
| [ELLIPSE](#ELLIPSE) | Ellipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Ellipse-Band. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Ellipse-Band 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Flussdiagramm alternativer Prozess. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Flussdiagramm zusammenführen. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Flussdiagramm-Verbindung. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Flussdiagramm-Entscheidung. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Flussdiagramm-Verzögerung. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Flussdiagramm-Anzeige. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Flussdiagramm-Dokument. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Flussdiagramm-Extraktion. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Flussdiagramm Eingabe/Ausgabe. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Flussdiagramm interner Speicher. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Flussdiagramm magnetische Festplatte. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Flussdiagramm magnetische Trommel. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Flusschar magnetisches Band. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Flussdiagramm manuelle Eingabe. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Flussdiagramm manuelle Operation. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Flussdiagramm Zusammenführen. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Flussdiagramm Mehrfachdokument. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Flussdiagramm Offline-Speicherung. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Flussdiagramm Off-Page-Verbindung. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Flussdiagramm Online-Speicherung. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Flussdiagramm oder. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Flussdiagramm vordefinierter Prozess |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Flussdiagramm-Vorbereitung. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Flussdiagramm-Prozess. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Flussdiagramm-Lochkarten. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Flussdiagramm-Lochstreifen. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Flussdiagramm-Sortierung. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Flussdiagramm-Summationsknoten. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Flussdiagramm-Terminator. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Gefaltete Ecke. |
| [FRAME](#FRAME) | Rahmen. |
| [FUNNEL](#FUNNEL) | Trichter. |
| [GEAR_6](#GEAR-6) | Sechszahnrad. |
| [GEAR_9](#GEAR-9) | Neunzahnrad. |
| [GROUP](#GROUP) | Die Form ist eine Gruppenform. |
| [HALF_FRAME](#HALF-FRAME) | Halbrahmen. |
| [HEART](#HEART) | Herz. |
| [HEPTAGON](#HEPTAGON) | Siebeneck. |
| [HEXAGON](#HEXAGON) | Sechseck. |
| [HOME_PLATE](#HOME-PLATE) | Heimatplatte. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Horizontaler Bildlauf. |
| [IMAGE](#IMAGE) | Die Form ist ein Bild. |
| [INVERSE_LINE](#INVERSE-LINE) | Umgekehrte Linie. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Unregelmäßige Dichtung 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Unregelmäßige Dichtung 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Pfeil nach links. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Linker Pfeil-Anmerkung. |
| [LEFT_BRACE](#LEFT-BRACE) | Linke geschweifte Klammer. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Linke eckige Klammer. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Linker kreisförmiger Pfeil. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Links-rechts-Pfeil. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Links-rechts-Pfeil-Anmerkung. |
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
| [MIN_VALUE](#MIN-VALUE) | Für die Systemnutzung reserviert. |
| [MOON](#MOON) | Mond. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Nicht-gleichschenkliges Trapez. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | Eine vom Benutzer gezeichnete Form, die aus mehreren Segmenten und/oder Eckpunkten (Kurve, Freiform oder Kritzelei) besteht. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Gezackter rechter Pfeil. |
| [NO_SMOKING](#NO-SMOKING) | KeinRauchen. |
| [OCTAGON](#OCTAGON) | Achtkant. |
| [OLE_CONTROL](#OLE-CONTROL) | Die Form ist ein ActiveX-Steuerelement. |
| [OLE_OBJECT](#OLE-OBJECT) | Die Form ist ein OLE-Objekt. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallelogramm. |
| [PENTAGON](#PENTAGON) | Fünfeck. |
| [PIE](#PIE) | Kuchen. |
| [PLAQUE](#PLAQUE) | Plakette. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Plaketten-Tabs. |
| [PLUS](#PLUS) | Plus. |
| [QUAD_ARROW](#QUAD-ARROW) | Vierfach-Pfeil. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Vierfach-Pfeil-Anmerkung. |
| [RECTANGLE](#RECTANGLE) | Rechteck. |
| [RIBBON](#RIBBON) | Band. |
| [RIBBON_2](#RIBBON-2) | Band 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Rechter Pfeil-Anmerkung |
| [RIGHT_BRACE](#RIGHT-BRACE) | Rechte Klammer. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Rechte eckige Klammer. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Rechtes Dreieck. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Abgerundetes Rechteck. |
| [SEAL](#SEAL) | Siegel. |
| [SEAL_10](#SEAL-10) | Zehnstrahliger Stern. |
| [SEAL_12](#SEAL-12) | Zwölfstrahliger Stern. |
| [SEAL_16](#SEAL-16) | Sechzehnstrahliger Stern. |
| [SEAL_24](#SEAL-24) | Vierundzwanzigstrahliger Stern. |
| [SEAL_32](#SEAL-32) | 32-zackiger Stern. |
| [SEAL_4](#SEAL-4) | Vierzackiger Stern. |
| [SEAL_6](#SEAL-6) | Sechs-zackiger Stern. |
| [SEAL_7](#SEAL-7) | Siebenzackiger Stern. |
| [SEAL_8](#SEAL-8) | Achtzackiger Stern. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rundes Rechteck mit einer einzelnen Ecke. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Einseitiges Eckrechteck-Objekt zuschneiden. |
| [SMILEY_FACE](#SMILEY-FACE) | Smiley-Gesicht. |
| [SQUARE_TABS](#SQUARE-TABS) | Quadratische Register. |
| [STAR](#STAR) | Stern. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Ein gerades Verbindungselement. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Gestreifter rechter Pfeil. |
| [SUN](#SUN) | Sonne. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Schwungpfeil. |
| [TEARDROP](#TEARDROP) | Träne. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | Bogen nach unten gekrümmt, WordArt object. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | Bogen nach unten gefüllt, WordArt object. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | Bogen nach oben gekrümmt, WordArt object. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | Bogen nach oben gefüllt, WordArt object. |
| [TEXT_BOX](#TEXT-BOX) | Die Form ist ein Textfeld. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | Schaltfläche gekrümmt, WordArt object. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | Schaltfläche gefüllt, WordArt object. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | Dose nach unten, WordArt object. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | Dose nach oben, WordArt object. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | Kaskade nach unten, WordArt object. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | Kaskade nach oben, WordArt object. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | Chevron, WordArt object. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | Chevron invertiert, WordArt object. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | Kreis gekrümmt, WordArt object. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | Kreis gefüllt, WordArt object. |
| [TEXT_CURVE](#TEXT-CURVE) | Text gekrümmt. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | Kurve nach unten, WordArt object. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | Kurve nach oben, WordArt object. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | Zusammenziehen, WordArt-Objekt. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | Zusammenziehen unten, WordArt-Objekt. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | Zusammenziehen ausdehnen, WordArt-Objekt. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | Zusammenziehen ausdehnen zusammenziehen, WordArt-Objekt. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | Zusammenziehen oben, WordArt-Objekt. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | Ausblenden nach unten, WordArt-Objekt. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | Ausblenden nach links, WordArt-Objekt. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | Ausblenden nach rechts, WordArt-Objekt. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | Ausblenden nach oben, WordArt-Objekt. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | Text Hexagon. |
| [TEXT_INFLATE](#TEXT-INFLATE) | Aufblähen, WordArt-Objekt. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | Aufblähen unten, WordArt-Objekt. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | Aufblähen oben, WordArt-Objekt. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | Text Octagon. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | Text auf Kurve. |
| [TEXT_ON_RING](#TEXT-ON-RING) | Text auf Ring. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | Einfacher Text, WordArt-Objekt. |
| [TEXT_RING](#TEXT-RING) | Text Ring. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | Ring innen, WordArt-Objekt. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | Ring außen, WordArt-Objekt. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | Einfacher Text. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | Schräg nach unten, WordArt-Objekt. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | Schräg nach oben, WordArt-Objekt. |
| [TEXT_STOP](#TEXT-STOP) | Stopp, WordArt-Objekt. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | Dreieck, WordArt-Objekt. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | Umgekehrtes Dreieck, WordArt-Objekt. |
| [TEXT_WAVE](#TEXT-WAVE) | Textwelle. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | Welle 1, WordArt-Objekt. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | Welle 2, WordArt-Objekt. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | Welle 3, WordArt-Objekt. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | Welle 4, WordArt-Objekt. |
| [THICK_ARROW](#THICK-ARROW) | Dicker Pfeil. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Abgeschnittener und abgerundeter einseitiger Rechteck. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rundes Rechteck mit gleicher Seitenkante. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Abgeschnittenes Rechteck mit Ecken auf derselben Seite. |
| [TRAPEZOID](#TRAPEZOID) | Trapez. |
| [TRIANGLE](#TRIANGLE) | Dreieck. |
| [UP_ARROW](#UP-ARROW) | Pfeil nach oben. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Aufwärts-Pfeil-Anmerkung. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Auf-Ab-Pfeil. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Auf-Ab-Pfeil-Anmerkung. |
| [UTURN_ARROW](#UTURN-ARROW) | U-Wendepfeil. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Vertikaler Bildlauf. |
| [WAVE](#WAVE) | Welle. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Keilellipse-Anmerkung. |
| [WEDGE_PIE](#WEDGE-PIE) | Keildiagramm. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Keilrechteck-Anmerkung. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Keil-R-Rechteck-Anmerkung. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Akzentrahmen-Anmerkung 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Akzentrahmen-Anmerkung 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Akzentrahmen-Anmerkung 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


Akzentrahmen-Anmerkung 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Eine Akzent-Anmerkungsform mit einem Pfeil.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Eine Akzent-Anmerkungsform mit zwei Pfeilen.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Eine Akzent-Anmerkungsform mit drei Pfeilen.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


Akzent-Anmerkung 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Aktionsschaltfläche zurück vorherige.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Aktionsschaltfläche Anfang.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Aktionsschaltfläche leer.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Aktionsschaltfläche Dokument.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Aktionsschaltfläche Ende.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Aktionsschaltfläche weiter nächste.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Aktionsschaltfläche Hilfe.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Aktionsschaltfläche Start.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Aktionsschaltfläche Informationen.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Aktionsschaltfläche Film.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Aktionsschaltfläche Zurück.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Aktionsschaltfläche Ton.

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

### BALLOON {#BALLOON}
```
public static int BALLOON
```


Ballon.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Gebogener Pfeil.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Eine gebogene Verbinderform mit zwei Segmenten.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Eine gebogene Verbinderform mit drei Segmenten.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Eine gebogene Verbinderform mit vier Segmenten.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Eine gebogene Verbinderform mit fünf Segmenten.

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


Randbeschriftung 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Randbeschriftung 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Randbeschriftung 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


Randbeschriftung 90.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Klammerpaar

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Klammerpaar.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Eine Beschriftungsform mit einem Pfeil.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Eine Beschriftungsform mit zwei Pfeilen.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Eine Beschriftungsform mit drei Pfeilen.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


Beschriftung 90.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Diagramm Stern.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Diagramm X.

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Wolkenbeschriftung.

### CORNER {#CORNER}
```
public static int CORNER
```


Ecke.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Eckregister.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### CUBE {#CUBE}
```
public static int CUBE
```


Würfel.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Eine gekrümmte Verbinderform mit zwei Segmenten.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Eine gekrümmte Verbinderform mit drei Segmenten.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Eine gekrümmte Verbinderform mit vier Segmenten.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Eine gekrümmte Verbinderform mit fünf Segmenten.

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


Gekrümmter Aufwärtspfeil

### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


Dieser Formtyp scheint für Formen festgelegt zu sein, die nicht Teil des Standard-Sets der Autoformen in Microsoft Word sind. Zum Beispiel, wenn Sie eine neue Autoform aus ClipArt einfügen.

Sie können in dem Dokument keine Formen dieses Typs erstellen.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Zehneck.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rundes Rechteck mit diagonaler Ecke.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Abgeschnittenes diagonales Eckrechteck.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Diagonaler Streifen.

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

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


Abwärtspfeil-Anmerkung.

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


Flussdiagramm alternativer Prozess.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Flussdiagramm zusammenführen.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Flussdiagramm-Verbindung.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Flussdiagramm-Entscheidung.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Flussdiagramm-Verzögerung.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Flussdiagramm-Anzeige.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Flussdiagramm-Dokument.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Flussdiagramm-Extraktion.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Flussdiagramm Eingabe/Ausgabe.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Flussdiagramm interner Speicher.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Flussdiagramm magnetische Festplatte.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Flussdiagramm magnetische Trommel.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Flusschar magnetisches Band.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Flussdiagramm manuelle Eingabe.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Flussdiagramm manuelle Operation.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Flussdiagramm Zusammenführen.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Flussdiagramm Mehrfachdokument.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Flussdiagramm Offline-Speicherung.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Flussdiagramm Off-Page-Verbindung.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Flussdiagramm Online-Speicherung.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Flussdiagramm oder.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Flussdiagramm vordefinierter Prozess

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Flussdiagramm-Vorbereitung.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Flussdiagramm-Prozess.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Flussdiagramm-Lochkarten.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Flussdiagramm-Lochstreifen.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Flussdiagramm-Sortierung.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Flussdiagramm-Summationsknoten.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Flussdiagramm-Terminator.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Trichter.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Sechszahnrad.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Neunzahnrad.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### GROUP {#GROUP}
```
public static int GROUP
```


Die Form ist eine Gruppenform.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Halbrahmen.

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Die Form ist ein Bild.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Umgekehrte Linie.

 **Remarks:** 

Nur für DML-Formen anwendbar.

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


Linker Pfeil-Anmerkung.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Links-rechts-Pfeil.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Links-rechts-Pfeil-Anmerkung.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Links-rechts kreisförmiger Pfeil.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Links-rechts-Band.

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Mathematisches Gleichheitszeichen.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Mathematisches Minuszeichen.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Mathematisches Malzeichen.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Mathematisches Ungleichheitszeichen.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Mathematisches Pluszeichen.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


Für die Systemnutzung reserviert.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


Eine vom Benutzer gezeichnete Form, die aus mehreren Segmenten und/oder Eckpunkten (Kurve, Freiform oder Kritzelei) besteht.

Sie können in dem Dokument keine Formen dieses Typs erstellen.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Gezackter rechter Pfeil.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


KeinRauchen.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Achtkant.

### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


Die Form ist ein ActiveX-Steuerelement.

Sie können in dem Dokument keine Formen dieses Typs erstellen.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


Die Form ist ein OLE-Objekt.

Sie können in dem Dokument keine Formen dieses Typs erstellen.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

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


Vierfach-Pfeil-Anmerkung.

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


Rechter Pfeil-Anmerkung

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

### SEAL {#SEAL}
```
public static int SEAL
```


Siegel.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Zehnstrahliger Stern.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Zwölfstrahliger Stern.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Sechzehnstrahliger Stern.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Vierundzwanzigstrahliger Stern.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


32-zackiger Stern.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Vierzackiger Stern.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Sechs-zackiger Stern.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Siebenzackiger Stern.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Achtzackiger Stern.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Rundes Rechteck mit einer einzelnen Ecke.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Einseitiges Eckrechteck-Objekt zuschneiden.

 **Remarks:** 

Nur für DML-Formen anwendbar.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### STAR {#STAR}
```
public static int STAR
```


Stern.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Ein gerades Verbindungselement.

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

 **Remarks:** 

Nur für DML-Formen anwendbar.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Träne.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


Bogen nach unten gekrümmt, WordArt object.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


Bogen nach unten gefüllt, WordArt object.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


Bogen nach oben gekrümmt, WordArt object.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


Bogen nach oben gefüllt, WordArt object.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Die Form ist ein Textfeld. Beachten Sie, dass Formen vieler anderer Typen ebenfalls Text enthalten können. Eine Form muss nicht diesen Typ haben, um Text zu enthalten.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


Schaltfläche gekrümmt, WordArt object.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


Schaltfläche gefüllt, WordArt object.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


Dose nach unten, WordArt object.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


Dose nach oben, WordArt object.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


Kaskade nach unten, WordArt object.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


Kaskade nach oben, WordArt object.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


Chevron, WordArt object.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


Chevron invertiert, WordArt object.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


Kreis gekrümmt, WordArt object.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


Kreis gefüllt, WordArt object.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


Text gekrümmt.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


Kurve nach unten, WordArt object.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


Kurve nach oben, WordArt object.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


Zusammenziehen, WordArt-Objekt.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


Zusammenziehen unten, WordArt-Objekt.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


Zusammenziehen ausdehnen, WordArt-Objekt.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


Zusammenziehen ausdehnen zusammenziehen, WordArt-Objekt.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


Zusammenziehen oben, WordArt-Objekt.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


Ausblenden nach unten, WordArt-Objekt.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


Ausblenden nach links, WordArt-Objekt.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


Ausblenden nach rechts, WordArt-Objekt.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


Ausblenden nach oben, WordArt-Objekt.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


Text Hexagon.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


Aufblähen, WordArt-Objekt.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


Aufblähen unten, WordArt-Objekt.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


Aufblähen oben, WordArt-Objekt.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


Text Octagon.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


Text auf Kurve.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


Text auf Ring.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


Einfacher Text, WordArt-Objekt.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


Text Ring.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


Ring innen, WordArt-Objekt.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


Ring außen, WordArt-Objekt.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


Einfacher Text.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


Schräg nach unten, WordArt-Objekt.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


Schräg nach oben, WordArt-Objekt.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


Stopp, WordArt-Objekt.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


Dreieck, WordArt-Objekt.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


Umgekehrtes Dreieck, WordArt-Objekt.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


Textwelle.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


Welle 1, WordArt-Objekt.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


Welle 2, WordArt-Objekt.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


Welle 3, WordArt-Objekt.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


Welle 4, WordArt-Objekt.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


Dicker Pfeil.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Abgeschnittener und abgerundeter einseitiger Rechteck.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rundes Rechteck mit gleicher Seitenkante.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Abgeschnittenes Rechteck mit Ecken auf derselben Seite.

 **Remarks:** 

Nur für DML-Formen anwendbar.

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


Aufwärts-Pfeil-Anmerkung.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Auf-Ab-Pfeil.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Auf-Ab-Pfeil-Anmerkung.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


U-Wendepfeil.

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


Keilellipse-Anmerkung.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Keildiagramm.

 **Remarks:** 

Nur für DML-Formen anwendbar.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Keilrechteck-Anmerkung.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Keil-R-Rechteck-Anmerkung.

### length {#length}
```
public static int length
```


### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
