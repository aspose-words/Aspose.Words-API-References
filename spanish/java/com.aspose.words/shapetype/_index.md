---
title: "ShapeType"
linktitle: "ShapeType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de forma en un documento de Microsoft Word en Java."
type: docs
weight: 618
url: /es/java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

Especifica el tipo de forma en un documento Microsoft Word.

 **Examples:** 

Muestra cómo insertar una forma con una imagen del sistema de archivos local en un documento.

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

Muestra cómo Aspose.Words identifica formas.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Llamada de borde acentuado 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Llamada de borde acentuado 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Llamada de borde acentuado 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | Llamada de borde acentuado 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Una forma de llamada acentuada con una flecha. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Una forma de llamada acentuada con dos flechas. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Una forma de llamada acentuada con tres flechas. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | Llamada acentuada 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Botón de acción retroceder anterior. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Botón de acción inicio. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Botón de acción vacío. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Botón de acción documento. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Botón de acción fin. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Botón de acción avanzar siguiente. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Botón de acción de ayuda. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Botón de acción de inicio. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Botón de acción de información. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Botón de acción de película. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Botón de acción de retorno. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Botón de acción de sonido. |
| [ARC](#ARC) | Arco. |
| [ARROW](#ARROW) | Flecha. |
| [BALLOON](#BALLOON) | Globo. |
| [BENT_ARROW](#BENT-ARROW) | Flecha doblada. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Una forma de conector doblado con dos segmentos. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Una forma de conector doblado con tres segmentos. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Una forma de conector doblado con cuatro segmentos. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Una forma de conector doblado con cinco segmentos. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Flecha doblada hacia arriba. |
| [BEVEL](#BEVEL) | Bisel. |
| [BLOCK_ARC](#BLOCK-ARC) | Arco de bloque. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Globo de borde 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Globo de borde 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Globo de borde 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | Globo de borde 90. |
| [BRACE_PAIR](#BRACE-PAIR) | Par de llaves. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Par de corchetes. |
| [CALLOUT_1](#CALLOUT-1) | Una forma de globo con una flecha. |
| [CALLOUT_2](#CALLOUT-2) | Una forma de globo con dos flechas. |
| [CALLOUT_3](#CALLOUT-3) | Una forma de globo con tres flechas. |
| [CALLOUT_90](#CALLOUT-90) | Globo 90. |
| [CAN](#CAN) | Lata. |
| [CHART_PLUS](#CHART-PLUS) | Gráfico más. |
| [CHART_STAR](#CHART-STAR) | Gráfico estrella. |
| [CHART_X](#CHART-X) | Gráfico X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Cuerda. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Flecha circular. |
| [CLOUD](#CLOUD) | Nube. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Globo de nube. |
| [CORNER](#CORNER) | Esquina. |
| [CORNER_TABS](#CORNER-TABS) | Pestañas de esquina. |
| [CUBE](#CUBE) | Cubo. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Una forma de conector curvo con dos segmentos. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Una forma de conector curvo con tres segmentos. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Una forma de conector curvo con cuatro segmentos. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Una forma de conector curvo con cinco segmentos. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Flecha curva hacia abajo. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Flecha curva hacia la izquierda. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Flecha curva hacia la derecha. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Flecha curva hacia arriba |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | Este tipo de forma parece estar configurado para formas que no forman parte del conjunto estándar de formas automáticas en Microsoft Word. |
| [DECAGON](#DECAGON) | Decágono. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rectángulo con esquina diagonal redondeada. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Rectángulo de esquina diagonal recortada. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Raya diagonal. |
| [DIAMOND](#DIAMOND) | Rombo. |
| [DODECAGON](#DODECAGON) | Dodecágono. |
| [DONUT](#DONUT) | Rosquilla. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Onda doble. |
| [DOWN_ARROW](#DOWN-ARROW) | Flecha hacia abajo. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Llamada de flecha hacia abajo. |
| [ELLIPSE](#ELLIPSE) | Elipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Cinta elíptica. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Cinta elíptica 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Diagrama de flujo proceso alternativo. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Diagrama de flujo compilar. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Conector de diagrama de flujo. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Decisión de diagrama de flujo. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Retraso de diagrama de flujo. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Visualización de diagrama de flujo. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Documento de diagrama de flujo. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Extracción de diagrama de flujo. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Entrada y salida de diagrama de flujo. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Almacenamiento interno de diagrama de flujo. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Disco magnético de diagrama de flujo. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Tambor magnético de diagrama de flujo. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Cinta magnética de flujo char. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Entrada manual de diagrama de flujo. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Operación manual de diagrama de flujo. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Fusión de diagrama de flujo. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Documento múltiple de diagrama de flujo. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Almacenamiento fuera de línea de diagrama de flujo. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Conector fuera de página de diagrama de flujo. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Almacenamiento en línea de diagrama de flujo. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Diagrama de flujo o. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Proceso predefinido de diagrama de flujo |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Preparación del diagrama de flujo. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Proceso del diagrama de flujo. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Tarjeta perforada del diagrama de flujo. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Cinta perforada del diagrama de flujo. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Ordenamiento del diagrama de flujo. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Unión sumadora del diagrama de flujo. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Terminador del diagrama de flujo. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Esquina doblada. |
| [FRAME](#FRAME) | Marco. |
| [FUNNEL](#FUNNEL) | Embudo. |
| [GEAR_6](#GEAR-6) | Engranaje de seis dientes. |
| [GEAR_9](#GEAR-9) | Engranaje de nueve dientes. |
| [GROUP](#GROUP) | La forma es una forma de grupo. |
| [HALF_FRAME](#HALF-FRAME) | Media marco. |
| [HEART](#HEART) | Corazón. |
| [HEPTAGON](#HEPTAGON) | Heptágono. |
| [HEXAGON](#HEXAGON) | Hexágono. |
| [HOME_PLATE](#HOME-PLATE) | Plato de home. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Desplazamiento horizontal. |
| [IMAGE](#IMAGE) | La forma es una imagen. |
| [INVERSE_LINE](#INVERSE-LINE) | Línea inversa. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Sello irregular 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Sello irregular 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Flecha izquierda. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Llamada de flecha izquierda. |
| [LEFT_BRACE](#LEFT-BRACE) | Llave izquierda. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Corchete izquierdo. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Flecha circular izquierda. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Flecha izquierda derecha. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Llamada de flecha izquierda derecha. |
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
| [MIN_VALUE](#MIN-VALUE) | Reservado para uso del sistema. |
| [MOON](#MOON) | Luna. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Trapecio no isósceles. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | Una forma dibujada por el usuario y que consta de varios segmentos y/o vértices (curva, forma libre o garabato). |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Flecha derecha con muesca. |
| [NO_SMOKING](#NO-SMOKING) | NoFumar. |
| [OCTAGON](#OCTAGON) | Octágono. |
| [OLE_CONTROL](#OLE-CONTROL) | La forma es un control ActiveX. |
| [OLE_OBJECT](#OLE-OBJECT) | La forma es un objeto OLE. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Paralelogramo. |
| [PENTAGON](#PENTAGON) | Pentágono. |
| [PIE](#PIE) | Tarta. |
| [PLAQUE](#PLAQUE) | Placa. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Pestañas de placa. |
| [PLUS](#PLUS) | Más. |
| [QUAD_ARROW](#QUAD-ARROW) | Flecha cuádruple. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Llamada de flecha cuádruple. |
| [RECTANGLE](#RECTANGLE) | Rectángulo. |
| [RIBBON](#RIBBON) | Cinta. |
| [RIBBON_2](#RIBBON-2) | Cinta 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Llamada de flecha derecha |
| [RIGHT_BRACE](#RIGHT-BRACE) | Llave derecha. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Corchete derecho. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Triángulo rectángulo. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Rectángulo redondeado. |
| [SEAL](#SEAL) | Sello. |
| [SEAL_10](#SEAL-10) | Estrella de diez puntas. |
| [SEAL_12](#SEAL-12) | Estrella de doce puntas. |
| [SEAL_16](#SEAL-16) | Estrella de 16 puntas. |
| [SEAL_24](#SEAL-24) | Estrella de 24 puntas. |
| [SEAL_32](#SEAL-32) | Estrella de 32 puntas. |
| [SEAL_4](#SEAL-4) | Estrella de cuatro puntas. |
| [SEAL_6](#SEAL-6) | Estrella de seis puntas. |
| [SEAL_7](#SEAL-7) | Estrella de siete puntas. |
| [SEAL_8](#SEAL-8) | Estrella de ocho puntas. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rectángulo redondeado de una sola esquina. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Objeto de recorte de una esquina del rectángulo. |
| [SMILEY_FACE](#SMILEY-FACE) | Cara sonriente. |
| [SQUARE_TABS](#SQUARE-TABS) | Pestañas cuadradas. |
| [STAR](#STAR) | Estrella. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Una forma de conector recto. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Flecha derecha a rayas. |
| [SUN](#SUN) | Sol. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Flecha swoosh. |
| [TEARDROP](#TEARDROP) | Gota. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | Arco descendente curvo, objeto WordArt. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | Arco descendente de vertido, objeto WordArt. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | Arco ascendente curvo, objeto WordArt. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | Arco ascendente de vertido, objeto WordArt. |
| [TEXT_BOX](#TEXT-BOX) | La forma es un cuadro de texto. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | Curva de botón, objeto WordArt. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | Vertido de botón, objeto WordArt. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | Lata descendente, objeto WordArt. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | Lata ascendente, objeto WordArt. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | Cascada descendente, objeto WordArt. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | Cascada ascendente, objeto WordArt. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | Chevron, objeto WordArt. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | Chevron invertido, objeto WordArt. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | Curva circular, objeto WordArt. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | Vertido circular, objeto WordArt. |
| [TEXT_CURVE](#TEXT-CURVE) | Curva de texto. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | Curva descendente, objeto WordArt. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | Curva hacia arriba, objeto WordArt. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | Desinflar, objeto WordArt. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | Desinflar abajo, objeto WordArt. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | Desinflar inflar, objeto WordArt. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | Desinflar inflar desinflar, objeto WordArt. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | Desinflar arriba, objeto WordArt. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | Desvanecer hacia abajo, objeto WordArt. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | Desvanecer a la izquierda, objeto WordArt. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | Desvanecer a la derecha, objeto WordArt. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | Desvanecer hacia arriba, objeto WordArt. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | Texto hexágono. |
| [TEXT_INFLATE](#TEXT-INFLATE) | Inflar, objeto WordArt. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | Inflar abajo, objeto WordArt. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | Inflar arriba, objeto WordArt. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | Texto octágono. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | Texto en curva. |
| [TEXT_ON_RING](#TEXT-ON-RING) | Texto en anillo. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | Texto sin formato, objeto WordArt. |
| [TEXT_RING](#TEXT-RING) | Anillo de texto. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | Anillo interior, objeto WordArt. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | Anillo exterior, objeto WordArt. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | Texto simple. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | Inclinación hacia abajo, objeto WordArt. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | Inclinación hacia arriba, objeto WordArt. |
| [TEXT_STOP](#TEXT-STOP) | Detener, objeto WordArt. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | Triángulo, objeto WordArt. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | Triángulo invertido, objeto WordArt. |
| [TEXT_WAVE](#TEXT-WAVE) | Onda de texto. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | Onda 1, objeto WordArt. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | Onda 2, objeto WordArt. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | Onda 3, objeto WordArt. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | Onda 4, objeto WordArt. |
| [THICK_ARROW](#THICK-ARROW) | Flecha gruesa. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Rectángulo de una sola esquina recortada y redondeada. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rectángulo de esquina redondeada del mismo lado. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Rectángulo con esquina del mismo lado recortada. |
| [TRAPEZOID](#TRAPEZOID) | Trapecio. |
| [TRIANGLE](#TRIANGLE) | Triángulo. |
| [UP_ARROW](#UP-ARROW) | Flecha hacia arriba. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Llamada de flecha hacia arriba. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Flecha arriba y abajo. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Llamada de flecha arriba y abajo. |
| [UTURN_ARROW](#UTURN-ARROW) | Flecha de giro en U. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Desplazamiento vertical. |
| [WAVE](#WAVE) | Onda. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Llamada de cuña elíptica. |
| [WEDGE_PIE](#WEDGE-PIE) | Cuña de pastel. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Llamada de cuña rectangular. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Llamada de cuña rectangular R. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Llamada de borde acentuado 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Llamada de borde acentuado 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Llamada de borde acentuado 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


Llamada de borde acentuado 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Una forma de llamada acentuada con una flecha.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Una forma de llamada acentuada con dos flechas.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Una forma de llamada acentuada con tres flechas.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


Llamada acentuada 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Botón de acción retroceder anterior.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Botón de acción inicio.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Botón de acción vacío.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Botón de acción documento.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Botón de acción fin.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Botón de acción avanzar siguiente.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Botón de acción de ayuda.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Botón de acción de inicio.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Botón de acción de información.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Botón de acción de película.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Botón de acción de retorno.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Botón de acción de sonido.

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

### BALLOON {#BALLOON}
```
public static int BALLOON
```


Globo.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Flecha doblada.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Una forma de conector doblado con dos segmentos.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Una forma de conector doblado con tres segmentos.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Una forma de conector doblado con cuatro segmentos.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Una forma de conector doblado con cinco segmentos.

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


Globo de borde 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Globo de borde 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Globo de borde 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


Globo de borde 90.

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


Una forma de globo con una flecha.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Una forma de globo con dos flechas.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Una forma de globo con tres flechas.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


Globo 90.

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

 **Remarks:** 

Aplicable solo a formas DML.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Gráfico estrella.

 **Remarks:** 

Aplicable solo a formas DML.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Gráfico X.

 **Remarks:** 

Aplicable solo a formas DML.

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

 **Remarks:** 

Aplicable solo a formas DML.

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

 **Remarks:** 

Aplicable solo a formas DML.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Globo de nube.

### CORNER {#CORNER}
```
public static int CORNER
```


Esquina.

 **Remarks:** 

Aplicable solo a formas DML.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Pestañas de esquina.

 **Remarks:** 

Aplicable solo a formas DML.

### CUBE {#CUBE}
```
public static int CUBE
```


Cubo.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Una forma de conector curvo con dos segmentos.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Una forma de conector curvo con tres segmentos.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Una forma de conector curvo con cuatro segmentos.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Una forma de conector curvo con cinco segmentos.

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


Flecha curva hacia arriba

### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


Este tipo de forma parece estar destinado a formas que no forman parte del conjunto estándar de formas automáticas en Microsoft Word. Por ejemplo, si insertas una nueva forma automática desde ClipArt.

No puedes crear formas de este tipo en el documento.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Decágono.

 **Remarks:** 

Aplicable solo a formas DML.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rectángulo con esquina diagonal redondeada.

 **Remarks:** 

Aplicable solo a formas DML.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Rectángulo de esquina diagonal recortada.

 **Remarks:** 

Aplicable solo a formas DML.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Raya diagonal.

 **Remarks:** 

Aplicable solo a formas DML.

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

 **Remarks:** 

Aplicable solo a formas DML.

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


Llamada de flecha hacia abajo.

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


Diagrama de flujo proceso alternativo.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Diagrama de flujo compilar.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Conector de diagrama de flujo.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Decisión de diagrama de flujo.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Retraso de diagrama de flujo.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Visualización de diagrama de flujo.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Documento de diagrama de flujo.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Extracción de diagrama de flujo.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Entrada y salida de diagrama de flujo.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Almacenamiento interno de diagrama de flujo.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Disco magnético de diagrama de flujo.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Tambor magnético de diagrama de flujo.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Cinta magnética de flujo char.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Entrada manual de diagrama de flujo.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Operación manual de diagrama de flujo.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Fusión de diagrama de flujo.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Documento múltiple de diagrama de flujo.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Almacenamiento fuera de línea de diagrama de flujo.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Conector fuera de página de diagrama de flujo.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Almacenamiento en línea de diagrama de flujo.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Diagrama de flujo o.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Proceso predefinido de diagrama de flujo

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Preparación del diagrama de flujo.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Proceso del diagrama de flujo.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Tarjeta perforada del diagrama de flujo.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Cinta perforada del diagrama de flujo.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Ordenamiento del diagrama de flujo.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Unión sumadora del diagrama de flujo.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Terminador del diagrama de flujo.

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

 **Remarks:** 

Aplicable solo a formas DML.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Embudo.

 **Remarks:** 

Aplicable solo a formas DML.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Engranaje de seis dientes.

 **Remarks:** 

Aplicable solo a formas DML.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Engranaje de nueve dientes.

 **Remarks:** 

Aplicable solo a formas DML.

### GROUP {#GROUP}
```
public static int GROUP
```


La forma es una forma de grupo.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Media marco.

 **Remarks:** 

Aplicable solo a formas DML.

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

 **Remarks:** 

Aplicable solo a formas DML.

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

### IMAGE {#IMAGE}
```
public static int IMAGE
```


La forma es una imagen.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Línea inversa.

 **Remarks:** 

Aplicable solo a formas DML.

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


Llamada de flecha izquierda.

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

 **Remarks:** 

Aplicable solo a formas DML.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Flecha izquierda derecha.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Llamada de flecha izquierda derecha.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Flecha circular izquierda-derecha.

 **Remarks:** 

Aplicable solo a formas DML.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Cinta izquierda-derecha.

 **Remarks:** 

Aplicable solo a formas DML.

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

 **Remarks:** 

Aplicable solo a formas DML.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Igualdad matemática.

 **Remarks:** 

Aplicable solo a formas DML.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Resta matemática.

 **Remarks:** 

Aplicable solo a formas DML.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Multiplicación matemática.

 **Remarks:** 

Aplicable solo a formas DML.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Desigualdad matemática.

 **Remarks:** 

Aplicable solo a formas DML.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Suma matemática.

 **Remarks:** 

Aplicable solo a formas DML.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


Reservado para uso del sistema.

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

 **Remarks:** 

Aplicable solo a formas DML.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


Una forma dibujada por el usuario y que consta de varios segmentos y/o vértices (curva, forma libre o garabato).

No puedes crear formas de este tipo en el documento.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Flecha derecha con muesca.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


NoFumar.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Octágono.

### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


La forma es un control ActiveX.

No puedes crear formas de este tipo en el documento.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


La forma es un objeto OLE.

No puedes crear formas de este tipo en el documento.

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

 **Remarks:** 

Aplicable solo a formas DML.

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

 **Remarks:** 

Aplicable solo a formas DML.

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


Llamada de flecha cuádruple.

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


Llamada de flecha derecha

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

### SEAL {#SEAL}
```
public static int SEAL
```


Sello.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Estrella de diez puntas.

 **Remarks:** 

Aplicable solo a formas DML.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Estrella de doce puntas.

 **Remarks:** 

Aplicable solo a formas DML.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Estrella de 16 puntas.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Estrella de 24 puntas.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Estrella de 32 puntas.

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

 **Remarks:** 

Aplicable solo a formas DML.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Estrella de siete puntas.

 **Remarks:** 

Aplicable solo a formas DML.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Estrella de ocho puntas.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Rectángulo redondeado de una sola esquina.

 **Remarks:** 

Aplicable solo a formas DML.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Objeto de recorte de una esquina del rectángulo.

 **Remarks:** 

Aplicable solo a formas DML.

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

 **Remarks:** 

Aplicable solo a formas DML.

### STAR {#STAR}
```
public static int STAR
```


Estrella.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Una forma de conector recto.

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

 **Remarks:** 

Aplicable solo a formas DML.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Gota.

 **Remarks:** 

Aplicable solo a formas DML.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


Arco descendente curvo, objeto WordArt.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


Arco descendente de vertido, objeto WordArt.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


Arco ascendente curvo, objeto WordArt.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


Arco ascendente de vertido, objeto WordArt.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


La forma es un cuadro de texto. Ten en cuenta que las formas de muchos otros tipos también pueden contener texto. Una forma no tiene que ser de este tipo para contener texto.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


Curva de botón, objeto WordArt.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


Vertido de botón, objeto WordArt.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


Lata descendente, objeto WordArt.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


Lata ascendente, objeto WordArt.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


Cascada descendente, objeto WordArt.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


Cascada ascendente, objeto WordArt.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


Chevron, objeto WordArt.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


Chevron invertido, objeto WordArt.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


Curva circular, objeto WordArt.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


Vertido circular, objeto WordArt.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


Curva de texto.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


Curva descendente, objeto WordArt.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


Curva hacia arriba, objeto WordArt.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


Desinflar, objeto WordArt.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


Desinflar abajo, objeto WordArt.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


Desinflar inflar, objeto WordArt.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


Desinflar inflar desinflar, objeto WordArt.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


Desinflar arriba, objeto WordArt.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


Desvanecer hacia abajo, objeto WordArt.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


Desvanecer a la izquierda, objeto WordArt.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


Desvanecer a la derecha, objeto WordArt.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


Desvanecer hacia arriba, objeto WordArt.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


Texto hexágono.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


Inflar, objeto WordArt.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


Inflar abajo, objeto WordArt.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


Inflar arriba, objeto WordArt.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


Texto octágono.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


Texto en curva.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


Texto en anillo.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


Texto sin formato, objeto WordArt.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


Anillo de texto.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


Anillo interior, objeto WordArt.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


Anillo exterior, objeto WordArt.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


Texto simple.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


Inclinación hacia abajo, objeto WordArt.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


Inclinación hacia arriba, objeto WordArt.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


Detener, objeto WordArt.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


Triángulo, objeto WordArt.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


Triángulo invertido, objeto WordArt.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


Onda de texto.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


Onda 1, objeto WordArt.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


Onda 2, objeto WordArt.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


Onda 3, objeto WordArt.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


Onda 4, objeto WordArt.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


Flecha gruesa.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Rectángulo de una sola esquina recortada y redondeada.

 **Remarks:** 

Aplicable solo a formas DML.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rectángulo de esquina redondeada del mismo lado.

 **Remarks:** 

Aplicable solo a formas DML.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Rectángulo con esquina del mismo lado recortada.

 **Remarks:** 

Aplicable solo a formas DML.

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


Llamada de flecha hacia arriba.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Flecha arriba y abajo.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Llamada de flecha arriba y abajo.

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


Llamada de cuña elíptica.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Cuña de pastel.

 **Remarks:** 

Aplicable solo a formas DML.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Llamada de cuña rectangular.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Llamada de cuña rectangular R.

### length {#length}
```
public static int length
```


### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
