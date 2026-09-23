---
title: "ShapeType"
linktitle: "ShapeType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di forma in un documento Microsoft Word in Java."
type: docs
weight: 618
url: /it/java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

Specifica il tipo di forma in un documento Microsoft Word.

 **Examples:** 

Mostra come inserire una forma con un'immagine dal file system locale in un documento.

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

Mostra come Aspose.Words identifica le forme.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Callout di bordo accentato 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Callout di bordo accentato 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Callout di bordo accentato 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | Callout di bordo accentato 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Una forma di callout accentato con una freccia. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Una forma di callout accentato con due frecce. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Una forma di callout accentato con tre frecce. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | Callout accentato 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Pulsante di azione indietro precedente. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Pulsante di azione inizio. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Pulsante di azione vuoto. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Pulsante di azione documento. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Pulsante di azione fine. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Pulsante di azione avanti successivo. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Pulsante azione aiuto. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Pulsante azione home. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Pulsante azione informazioni. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Pulsante azione film. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Pulsante azione ritorno. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Pulsante azione suono. |
| [ARC](#ARC) | Arco. |
| [ARROW](#ARROW) | Freccia. |
| [BALLOON](#BALLOON) | Bolla. |
| [BENT_ARROW](#BENT-ARROW) | Freccia piegata. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Una forma di connettore piegato con due segmenti. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Una forma di connettore piegato con tre segmenti. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Una forma di connettore piegato con quattro segmenti. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Una forma di connettore piegato con cinque segmenti. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Freccia piegata verso l'alto. |
| [BEVEL](#BEVEL) | Smussatura. |
| [BLOCK_ARC](#BLOCK-ARC) | Arco a blocco. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Didascalia bordo 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Didascalia bordo 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Didascalia bordo 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | Didascalia bordo 90. |
| [BRACE_PAIR](#BRACE-PAIR) | Coppia di parentesi graffe. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Coppia di parentesi quadre. |
| [CALLOUT_1](#CALLOUT-1) | Una forma di didascalia con una freccia. |
| [CALLOUT_2](#CALLOUT-2) | Una forma di didascalia con due frecce. |
| [CALLOUT_3](#CALLOUT-3) | Una forma di didascalia con tre frecce. |
| [CALLOUT_90](#CALLOUT-90) | Didascalia 90. |
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
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Una forma di connettore curvo con due segmenti. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Una forma di connettore curvo con tre segmenti. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Una forma di connettore curvo con quattro segmenti. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Una forma di connettore curvo con cinque segmenti. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Freccia curva verso il basso. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Freccia curva verso sinistra. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Freccia curva verso destra. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Freccia curva verso l'alto |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | Questo tipo di forma sembra essere impostato per forme che non fanno parte del set standard delle forme automatiche in Microsoft Word. |
| [DECAGON](#DECAGON) | Decagono. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rettangolo con angolo diagonale arrotondato. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Rettangolo con angolo diagonale tagliato. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Striscia diagonale. |
| [DIAMOND](#DIAMOND) | Diamante. |
| [DODECAGON](#DODECAGON) | Dodecagono. |
| [DONUT](#DONUT) | Ciambella. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Onda doppia. |
| [DOWN_ARROW](#DOWN-ARROW) | Freccia verso il basso. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Didascalia con freccia verso il basso. |
| [ELLIPSE](#ELLIPSE) | Ellisse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Nastro ellittico. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Nastro ellittico 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Diagramma di flusso processo alternativo. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Diagramma di flusso collazione. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Diagramma di flusso connettore. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Diagramma di flusso decisione. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Diagramma di flusso ritardo. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Diagramma di flusso visualizzazione. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Diagramma di flusso documento. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Diagramma di flusso estrazione. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Diagramma di flusso ingresso uscita. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Diagramma di flusso archiviazione interna. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Diagramma di flusso disco magnetico. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Diagramma di flusso tamburo magnetico. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Diagramma di flusso nastro magnetico. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Diagramma di flusso input manuale. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Diagramma di flusso operazione manuale. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Diagramma di flusso unione. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Diagramma di flusso multi documento. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Diagramma di flusso archiviazione offline. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Diagramma di flusso connettore fuori pagina. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Diagramma di flusso archiviazione online. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Diagramma di flusso o. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Processo predefinito del diagramma di flusso |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Preparazione del diagramma di flusso. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Processo del diagramma di flusso. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Scheda perforata del diagramma di flusso. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Nastro perforato del diagramma di flusso. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Ordinamento del diagramma di flusso. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Giunzione di somma del diagramma di flusso. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Terminatore del diagramma di flusso. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Angolo piegato. |
| [FRAME](#FRAME) | Cornice. |
| [FUNNEL](#FUNNEL) | Imbuto. |
| [GEAR_6](#GEAR-6) | Ingranaggio a sei denti. |
| [GEAR_9](#GEAR-9) | Ingranaggio a nove denti. |
| [GROUP](#GROUP) | La forma è una forma di gruppo. |
| [HALF_FRAME](#HALF-FRAME) | Mezza cornice. |
| [HEART](#HEART) | Cuore. |
| [HEPTAGON](#HEPTAGON) | Ettagono. |
| [HEXAGON](#HEXAGON) | Esagono. |
| [HOME_PLATE](#HOME-PLATE) | Casa base. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Scorrimento orizzontale. |
| [IMAGE](#IMAGE) | La forma è un'immagine. |
| [INVERSE_LINE](#INVERSE-LINE) | Linea inversa. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Sigillo irregolare 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Sigillo irregolare 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Freccia sinistra. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Chiamata a freccia sinistra. |
| [LEFT_BRACE](#LEFT-BRACE) | Graffa sinistra. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Parentesi quadra sinistra. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Freccia circolare sinistra. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Freccia sinistra destra. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Chiamata a freccia sinistra destra. |
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
| [MIN_VALUE](#MIN-VALUE) | Riservato per l'uso del sistema. |
| [MOON](#MOON) | Luna. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Trapezio non isoscele. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | Una forma disegnata dall'utente e composta da più segmenti e/o vertici (curva, forma libera o scarabocchio). |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Freccia destra dentata. |
| [NO_SMOKING](#NO-SMOKING) | Divieto di fumo. |
| [OCTAGON](#OCTAGON) | Ottagono. |
| [OLE_CONTROL](#OLE-CONTROL) | La forma è un controllo ActiveX. |
| [OLE_OBJECT](#OLE-OBJECT) | La forma è un oggetto OLE. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallelogramma. |
| [PENTAGON](#PENTAGON) | Pentagono. |
| [PIE](#PIE) | Torta. |
| [PLAQUE](#PLAQUE) | Targa. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Schede della targa. |
| [PLUS](#PLUS) | Più. |
| [QUAD_ARROW](#QUAD-ARROW) | Freccia a quattro punte. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Chiamata a freccia quadrupla. |
| [RECTANGLE](#RECTANGLE) | Rettangolo. |
| [RIBBON](#RIBBON) | Nastro. |
| [RIBBON_2](#RIBBON-2) | Nastro 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Chiamata a freccia destra |
| [RIGHT_BRACE](#RIGHT-BRACE) | Graffa destra. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Parentesi destra. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Triangolo rettangolo. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Rettangolo arrotondato. |
| [SEAL](#SEAL) | Sigillo. |
| [SEAL_10](#SEAL-10) | Stella a dieci punte. |
| [SEAL_12](#SEAL-12) | Stella a dodici punte. |
| [SEAL_16](#SEAL-16) | Stella a 16 punte. |
| [SEAL_24](#SEAL-24) | Stella a 24 punte. |
| [SEAL_32](#SEAL-32) | Stella a 32 punte. |
| [SEAL_4](#SEAL-4) | Stella a quattro punte. |
| [SEAL_6](#SEAL-6) | Stella a sei punte. |
| [SEAL_7](#SEAL-7) | Stella a sette punte. |
| [SEAL_8](#SEAL-8) | Stella a otto punte. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rettangolo con un angolo arrotondato. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Oggetto rettangolo a un angolo tagliato. |
| [SMILEY_FACE](#SMILEY-FACE) | Faccina sorridente. |
| [SQUARE_TABS](#SQUARE-TABS) | Schede quadrate. |
| [STAR](#STAR) | Stella. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Una forma di connettore dritto. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Freccia destra a strisce. |
| [SUN](#SUN) | Sole. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Freccia a scatto. |
| [TEARDROP](#TEARDROP) | Goccia. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | Arco curvo verso il basso, oggetto WordArt. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | Arco verso il basso riempito, oggetto WordArt. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | Arco curvo verso l'alto, oggetto WordArt. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | Arco verso l'alto riempito, oggetto WordArt. |
| [TEXT_BOX](#TEXT-BOX) | La forma è una textbox. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | Pulsante curvo, oggetto WordArt. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | Pulsante riempito, oggetto WordArt. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | Lattina verso il basso, oggetto WordArt. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | Lattina verso l'alto, oggetto WordArt. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | Cascata verso il basso, oggetto WordArt. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | Cascata verso l'alto, oggetto WordArt. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | Chevron, oggetto WordArt. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | Chevron invertito, oggetto WordArt. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | Cerchio curvo, oggetto WordArt. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | Cerchio riempito, oggetto WordArt. |
| [TEXT_CURVE](#TEXT-CURVE) | Curva di testo. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | Curva verso il basso, oggetto WordArt. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | Curva verso l'alto, oggetto WordArt. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | Sgonfia, oggetto WordArt. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | Sgonfia in basso, oggetto WordArt. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | Sgonfia gonfia, oggetto WordArt. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | Sgonfia gonfia sgonfia, oggetto WordArt. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | Sgonfia in alto, oggetto WordArt. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | Sfuma verso il basso, oggetto WordArt. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | Sfuma a sinistra, oggetto WordArt. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | Sfuma a destra, oggetto WordArt. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | Sfuma verso l'alto, oggetto WordArt. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | Testo esagono. |
| [TEXT_INFLATE](#TEXT-INFLATE) | Gonfia, oggetto WordArt. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | Gonfia in basso, oggetto WordArt. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | Gonfia in alto, oggetto WordArt. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | Testo ottagono. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | Testo su curva. |
| [TEXT_ON_RING](#TEXT-ON-RING) | Testo su anello. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | Testo semplice, oggetto WordArt. |
| [TEXT_RING](#TEXT-RING) | Anello di testo. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | Anello interno, oggetto WordArt. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | Anello esterno, oggetto WordArt. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | Testo semplice. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | Inclina verso il basso, oggetto WordArt. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | Inclina verso l'alto, oggetto WordArt. |
| [TEXT_STOP](#TEXT-STOP) | Ferma, oggetto WordArt. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | Triangolo, oggetto WordArt. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | Triangolo invertito, oggetto WordArt. |
| [TEXT_WAVE](#TEXT-WAVE) | Onda di testo. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | Onda 1, oggetto WordArt. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | Onda 2, oggetto WordArt. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | Onda 3, oggetto WordArt. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | Onda 4, oggetto WordArt. |
| [THICK_ARROW](#THICK-ARROW) | Freccia spessa. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Rettangolo a singolo angolo ritagliato e arrotondato. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rettangolo con angolo arrotondato sullo stesso lato. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Rettangolo con angolo ritagliato sullo stesso lato. |
| [TRAPEZOID](#TRAPEZOID) | Trapezio. |
| [TRIANGLE](#TRIANGLE) | Triangolo. |
| [UP_ARROW](#UP-ARROW) | Freccia verso l'alto. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Freccia su con richiamo. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Freccia su/giù. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Freccia su/giù con richiamo. |
| [UTURN_ARROW](#UTURN-ARROW) | Freccia a U. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Scorrimento verticale. |
| [WAVE](#WAVE) | Onda. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Richiamo a cuneo ellittico. |
| [WEDGE_PIE](#WEDGE-PIE) | Fetta di torta. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Richiamo a cuneo rettangolare. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Richiamo a cuneo R rettangolare. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Callout di bordo accentato 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Callout di bordo accentato 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Callout di bordo accentato 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


Callout di bordo accentato 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Una forma di callout accentato con una freccia.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Una forma di callout accentato con due frecce.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Una forma di callout accentato con tre frecce.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


Callout accentato 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Pulsante di azione indietro precedente.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Pulsante di azione inizio.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Pulsante di azione vuoto.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Pulsante di azione documento.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Pulsante di azione fine.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Pulsante di azione avanti successivo.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Pulsante azione aiuto.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Pulsante azione home.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Pulsante azione informazioni.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Pulsante azione film.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Pulsante azione ritorno.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Pulsante azione suono.

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

### BALLOON {#BALLOON}
```
public static int BALLOON
```


Bolla.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Freccia piegata.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Una forma di connettore piegato con due segmenti.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Una forma di connettore piegato con tre segmenti.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Una forma di connettore piegato con quattro segmenti.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Una forma di connettore piegato con cinque segmenti.

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


Didascalia bordo 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Didascalia bordo 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Didascalia bordo 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


Didascalia bordo 90.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Coppia di parentesi graffe.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Coppia di parentesi quadre.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Una forma di didascalia con una freccia.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Una forma di didascalia con due frecce.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Una forma di didascalia con tre frecce.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


Didascalia 90.

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

 **Remarks:** 

Applicabile solo per forme DML.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Grafico stella.

 **Remarks:** 

Applicabile solo per forme DML.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Grafico X.

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Schede d'angolo.

 **Remarks:** 

Applicabile solo per forme DML.

### CUBE {#CUBE}
```
public static int CUBE
```


Cubo.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Una forma di connettore curvo con due segmenti.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Una forma di connettore curvo con tre segmenti.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Una forma di connettore curvo con quattro segmenti.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Una forma di connettore curvo con cinque segmenti.

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


Freccia curva verso l'alto

### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


Questo tipo di forma sembra essere impostato per forme che non fanno parte del set standard delle forme automatiche in Microsoft Word. Ad esempio, se inserisci una nuova forma automatica da ClipArt.

Non è possibile creare forme di questo tipo nel documento.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Decagono.

 **Remarks:** 

Applicabile solo per forme DML.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rettangolo con angolo diagonale arrotondato.

 **Remarks:** 

Applicabile solo per forme DML.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Rettangolo con angolo diagonale tagliato.

 **Remarks:** 

Applicabile solo per forme DML.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Striscia diagonale.

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

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


Didascalia con freccia verso il basso.

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


Diagramma di flusso processo alternativo.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Diagramma di flusso collazione.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Diagramma di flusso connettore.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Diagramma di flusso decisione.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Diagramma di flusso ritardo.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Diagramma di flusso visualizzazione.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Diagramma di flusso documento.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Diagramma di flusso estrazione.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Diagramma di flusso ingresso uscita.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Diagramma di flusso archiviazione interna.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Diagramma di flusso disco magnetico.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Diagramma di flusso tamburo magnetico.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Diagramma di flusso nastro magnetico.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Diagramma di flusso input manuale.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Diagramma di flusso operazione manuale.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Diagramma di flusso unione.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Diagramma di flusso multi documento.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Diagramma di flusso archiviazione offline.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Diagramma di flusso connettore fuori pagina.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Diagramma di flusso archiviazione online.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Diagramma di flusso o.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Processo predefinito del diagramma di flusso

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Preparazione del diagramma di flusso.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Processo del diagramma di flusso.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Scheda perforata del diagramma di flusso.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Nastro perforato del diagramma di flusso.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Ordinamento del diagramma di flusso.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Giunzione di somma del diagramma di flusso.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Terminatore del diagramma di flusso.

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

 **Remarks:** 

Applicabile solo per forme DML.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Imbuto.

 **Remarks:** 

Applicabile solo per forme DML.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Ingranaggio a sei denti.

 **Remarks:** 

Applicabile solo per forme DML.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Ingranaggio a nove denti.

 **Remarks:** 

Applicabile solo per forme DML.

### GROUP {#GROUP}
```
public static int GROUP
```


La forma è una forma di gruppo.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Mezza cornice.

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

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

### IMAGE {#IMAGE}
```
public static int IMAGE
```


La forma è un'immagine.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Linea inversa.

 **Remarks:** 

Applicabile solo per forme DML.

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


Chiamata a freccia sinistra.

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

 **Remarks:** 

Applicabile solo per forme DML.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Freccia sinistra destra.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Chiamata a freccia sinistra destra.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Freccia circolare sinistra-destra.

 **Remarks:** 

Applicabile solo per forme DML.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Nastro sinistra-destra.

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Uguale matematico.

 **Remarks:** 

Applicabile solo per forme DML.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Meno matematico.

 **Remarks:** 

Applicabile solo per forme DML.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Moltiplicazione matematica.

 **Remarks:** 

Applicabile solo per forme DML.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Diverso matematico.

 **Remarks:** 

Applicabile solo per forme DML.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Più matematico.

 **Remarks:** 

Applicabile solo per forme DML.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


Riservato per l'uso del sistema.

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

 **Remarks:** 

Applicabile solo per forme DML.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


Una forma disegnata dall'utente e composta da più segmenti e/o vertici (curva, forma libera o scarabocchio).

Non è possibile creare forme di questo tipo nel documento.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Freccia destra dentata.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


Divieto di fumo.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Ottagono.

### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


La forma è un controllo ActiveX.

Non è possibile creare forme di questo tipo nel documento.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


La forma è un oggetto OLE.

Non è possibile creare forme di questo tipo nel documento.

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

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

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


Chiamata a freccia quadrupla.

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


Chiamata a freccia destra

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

### SEAL {#SEAL}
```
public static int SEAL
```


Sigillo.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Stella a dieci punte.

 **Remarks:** 

Applicabile solo per forme DML.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Stella a dodici punte.

 **Remarks:** 

Applicabile solo per forme DML.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Stella a 16 punte.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Stella a 24 punte.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Stella a 32 punte.

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

 **Remarks:** 

Applicabile solo per forme DML.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Stella a sette punte.

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Oggetto rettangolo a un angolo tagliato.

 **Remarks:** 

Applicabile solo per forme DML.

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

 **Remarks:** 

Applicabile solo per forme DML.

### STAR {#STAR}
```
public static int STAR
```


Stella.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Una forma di connettore dritto.

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

 **Remarks:** 

Applicabile solo per forme DML.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Goccia.

 **Remarks:** 

Applicabile solo per forme DML.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


Arco curvo verso il basso, oggetto WordArt.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


Arco verso il basso riempito, oggetto WordArt.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


Arco curvo verso l'alto, oggetto WordArt.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


Arco verso l'alto riempito, oggetto WordArt.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


La forma è una casella di testo. Nota che le forme di molti altri tipi possono anche contenere testo al loro interno. Una forma non deve avere questo tipo per contenere testo.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


Pulsante curvo, oggetto WordArt.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


Pulsante riempito, oggetto WordArt.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


Lattina verso il basso, oggetto WordArt.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


Lattina verso l'alto, oggetto WordArt.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


Cascata verso il basso, oggetto WordArt.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


Cascata verso l'alto, oggetto WordArt.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


Chevron, oggetto WordArt.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


Chevron invertito, oggetto WordArt.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


Cerchio curvo, oggetto WordArt.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


Cerchio riempito, oggetto WordArt.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


Curva di testo.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


Curva verso il basso, oggetto WordArt.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


Curva verso l'alto, oggetto WordArt.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


Sgonfia, oggetto WordArt.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


Sgonfia in basso, oggetto WordArt.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


Sgonfia gonfia, oggetto WordArt.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


Sgonfia gonfia sgonfia, oggetto WordArt.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


Sgonfia in alto, oggetto WordArt.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


Sfuma verso il basso, oggetto WordArt.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


Sfuma a sinistra, oggetto WordArt.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


Sfuma a destra, oggetto WordArt.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


Sfuma verso l'alto, oggetto WordArt.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


Testo esagono.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


Gonfia, oggetto WordArt.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


Gonfia in basso, oggetto WordArt.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


Gonfia in alto, oggetto WordArt.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


Testo ottagono.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


Testo su curva.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


Testo su anello.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


Testo semplice, oggetto WordArt.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


Anello di testo.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


Anello interno, oggetto WordArt.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


Anello esterno, oggetto WordArt.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


Testo semplice.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


Inclina verso il basso, oggetto WordArt.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


Inclina verso l'alto, oggetto WordArt.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


Ferma, oggetto WordArt.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


Triangolo, oggetto WordArt.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


Triangolo invertito, oggetto WordArt.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


Onda di testo.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


Onda 1, oggetto WordArt.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


Onda 2, oggetto WordArt.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


Onda 3, oggetto WordArt.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


Onda 4, oggetto WordArt.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


Freccia spessa.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Rettangolo a singolo angolo ritagliato e arrotondato.

 **Remarks:** 

Applicabile solo per forme DML.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rettangolo con angolo arrotondato sullo stesso lato.

 **Remarks:** 

Applicabile solo per forme DML.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Rettangolo con angolo ritagliato sullo stesso lato.

 **Remarks:** 

Applicabile solo per forme DML.

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


Freccia su con richiamo.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Freccia su/giù.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Freccia su/giù con richiamo.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


Freccia a U.

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


Richiamo a cuneo ellittico.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Fetta di torta.

 **Remarks:** 

Applicabile solo per forme DML.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Richiamo a cuneo rettangolare.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Richiamo a cuneo R rettangolare.

### length {#length}
```
public static int length
```


### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
