---
title: "ShapeType"
linktitle: "ShapeType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de forme dans un document Microsoft Word en Java."
type: docs
weight: 618
url: /fr/java/com.aspose.words/shapetype/
---

**Inheritance:**
java.lang.Object
```
public class ShapeType
```

Spécifie le type de forme dans un document Microsoft Word.

 **Examples:** 

Montre comment insérer une forme avec une image du système de fichiers local dans un document.

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

Montre comment Aspose.Words identifie les formes.

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
## Champs

| Champ | Description |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Appel de bordure accentuée 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Appel de bordure accentuée 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Appel de bordure accentuée 3. |
| [ACCENT_BORDER_CALLOUT_90](#ACCENT-BORDER-CALLOUT-90) | Appel de bordure accentuée 90. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Une forme d'appel accentué avec une flèche. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Une forme d'appel accentué avec deux flèches. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Une forme d'appel accentué avec trois flèches. |
| [ACCENT_CALLOUT_90](#ACCENT-CALLOUT-90) | Appel accentué 90. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Bouton d'action retour précédent. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Bouton d'action début. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Bouton d'action vierge. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Bouton d'action document. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Bouton d'action fin. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Bouton d'action avancer suivant. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Bouton d'action d'aide. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Bouton d'action accueil. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Bouton d'action information. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Bouton d'action film. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Bouton d'action retour. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Bouton d'action son. |
| [ARC](#ARC) | Arc. |
| [ARROW](#ARROW) | Flèche. |
| [BALLOON](#BALLOON) | Bulle. |
| [BENT_ARROW](#BENT-ARROW) | Flèche courbée. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Une forme de connecteur coudé avec deux segments. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Une forme de connecteur coudé avec trois segments. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Une forme de connecteur coudé avec quatre segments. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Une forme de connecteur coudé avec cinq segments. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Flèche courbée vers le haut. |
| [BEVEL](#BEVEL) | Biseau. |
| [BLOCK_ARC](#BLOCK-ARC) | Arc de bloc. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Appel de bordure 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Appel de bordure 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Appel de bordure 3. |
| [BORDER_CALLOUT_90](#BORDER-CALLOUT-90) | Appel de bordure 90. |
| [BRACE_PAIR](#BRACE-PAIR) | Paire d'accolades |
| [BRACKET_PAIR](#BRACKET-PAIR) | Paire de crochets. |
| [CALLOUT_1](#CALLOUT-1) | Une forme d'annotation avec une flèche. |
| [CALLOUT_2](#CALLOUT-2) | Une forme d'annotation avec deux flèches. |
| [CALLOUT_3](#CALLOUT-3) | Une forme d'annotation avec trois flèches. |
| [CALLOUT_90](#CALLOUT-90) | Annotation 90. |
| [CAN](#CAN) | Boîte. |
| [CHART_PLUS](#CHART-PLUS) | Graphique plus. |
| [CHART_STAR](#CHART-STAR) | Graphique étoile. |
| [CHART_X](#CHART-X) | Graphique X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Corde. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Flèche circulaire. |
| [CLOUD](#CLOUD) | Nuage. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Annotation nuage. |
| [CORNER](#CORNER) | Coin. |
| [CORNER_TABS](#CORNER-TABS) | Onglets d'angle. |
| [CUBE](#CUBE) | Cube. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Une forme de connecteur courbé avec deux segments. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Une forme de connecteur courbé avec trois segments. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Une forme de connecteur courbé avec quatre segments. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Une forme de connecteur courbé avec cinq segments. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Flèche courbée vers le bas. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Flèche courbée vers la gauche. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Flèche courbée vers la droite. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Flèche courbée vers le haut |
| [CUSTOM_SHAPE](#CUSTOM-SHAPE) | Ce type de forme semble être destiné aux formes qui ne font pas partie de l'ensemble standard des formes automatiques dans Microsoft Word. |
| [DECAGON](#DECAGON) | Décagone. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rectangle à coins diagonaux arrondis. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Rectangle à coins diagonaux découpés. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Bande diagonale. |
| [DIAMOND](#DIAMOND) | Losange. |
| [DODECAGON](#DODECAGON) | Dodécagone. |
| [DONUT](#DONUT) | Beignet. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Double vague. |
| [DOWN_ARROW](#DOWN-ARROW) | Flèche vers le bas. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Appel de flèche vers le bas. |
| [ELLIPSE](#ELLIPSE) | Ellipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Ruban d'ellipse. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Ruban d'ellipse 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Processus alternatif du diagramme de flux. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Collation du diagramme de flux. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Connecteur du diagramme de flux. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Décision du diagramme de flux. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Délai du diagramme de flux. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Affichage du diagramme de flux. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Document du diagramme de flux. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Extraction du diagramme de flux. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Entrée‑sortie du diagramme de flux. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Stockage interne du diagramme de flux. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Disque magnétique du diagramme de flux. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Tambour magnétique du diagramme de flux. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Bande magnétique du diagramme de flux. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Entrée manuelle du diagramme de flux. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Opération manuelle du diagramme de flux. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Fusion du diagramme de flux. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Diagramme de flux multi‑document. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Stockage hors ligne du diagramme de flux. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Connecteur hors page du diagramme de flux. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Stockage en ligne du diagramme de flux. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Diagramme de flux ou. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Processus prédéfini du diagramme de flux |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Préparation du diagramme de flux. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Processus du diagramme de flux. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Carte perforée du diagramme de flux. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Ruban perforé du diagramme de flux. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Tri du diagramme de flux. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Jonction de sommation du diagramme de flux. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Terminateur du diagramme de flux. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Coin plié. |
| [FRAME](#FRAME) | Cadre. |
| [FUNNEL](#FUNNEL) | Entonnoir. |
| [GEAR_6](#GEAR-6) | Engrenage à six dents. |
| [GEAR_9](#GEAR-9) | Engrenage à neuf dents. |
| [GROUP](#GROUP) | La forme est une forme groupée. |
| [HALF_FRAME](#HALF-FRAME) | Demi-cadre. |
| [HEART](#HEART) | Cœur. |
| [HEPTAGON](#HEPTAGON) | Heptagone. |
| [HEXAGON](#HEXAGON) | Hexagone. |
| [HOME_PLATE](#HOME-PLATE) | Plaque de base. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Défilement horizontal. |
| [IMAGE](#IMAGE) | La forme est une image. |
| [INVERSE_LINE](#INVERSE-LINE) | Ligne inverse. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Joint irrégulier 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Joint irrégulier 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Flèche gauche. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Appel de flèche gauche. |
| [LEFT_BRACE](#LEFT-BRACE) | Accolade gauche. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Crochet gauche. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Flèche circulaire gauche. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Flèche gauche-droite. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Appel de flèche gauche-droite. |
| [LEFT_RIGHT_CIRCULAR_ARROW](#LEFT-RIGHT-CIRCULAR-ARROW) | Flèche circulaire gauche‑droite. |
| [LEFT_RIGHT_RIBBON](#LEFT-RIGHT-RIBBON) | Ruban gauche‑droite. |
| [LEFT_RIGHT_UP_ARROW](#LEFT-RIGHT-UP-ARROW) | Flèche haut gauche‑droite. |
| [LEFT_UP_ARROW](#LEFT-UP-ARROW) | Flèche haut gauche. |
| [LIGHTNING_BOLT](#LIGHTNING-BOLT) | Éclair. |
| [LINE](#LINE) | Ligne. |
| [MATH_DIVIDE](#MATH-DIVIDE) | Division mathématique. |
| [MATH_EQUAL](#MATH-EQUAL) | Égalité mathématique. |
| [MATH_MINUS](#MATH-MINUS) | Soustraction mathématique. |
| [MATH_MULTIPLY](#MATH-MULTIPLY) | Multiplication mathématique. |
| [MATH_NOT_EQUAL](#MATH-NOT-EQUAL) | Inégalité mathématique. |
| [MATH_PLUS](#MATH-PLUS) | Addition mathématique. |
| [MIN_VALUE](#MIN-VALUE) | Réservé à l'usage du système. |
| [MOON](#MOON) | Lune. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Trapèze non isocèle. |
| [NON_PRIMITIVE](#NON-PRIMITIVE) | Une forme dessinée par l'utilisateur et composée de plusieurs segments et/ou sommets (courbe, forme libre ou griffonnage). |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Flèche droite à encoches. |
| [NO_SMOKING](#NO-SMOKING) | NoSmoking. |
| [OCTAGON](#OCTAGON) | Octogone. |
| [OLE_CONTROL](#OLE-CONTROL) | La forme est un contrôle ActiveX. |
| [OLE_OBJECT](#OLE-OBJECT) | La forme est un objet OLE. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallélogramme. |
| [PENTAGON](#PENTAGON) | Pentagone. |
| [PIE](#PIE) | Tarte. |
| [PLAQUE](#PLAQUE) | Plaque. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Onglets de plaque. |
| [PLUS](#PLUS) | Plus. |
| [QUAD_ARROW](#QUAD-ARROW) | Flèche quadruple. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Appel de flèche quadruple. |
| [RECTANGLE](#RECTANGLE) | Rectangle. |
| [RIBBON](#RIBBON) | Ruban. |
| [RIBBON_2](#RIBBON-2) | Ruban 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Appel de flèche droite |
| [RIGHT_BRACE](#RIGHT-BRACE) | Accolade droite. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Crochet droit. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Triangle droit. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Rectangle arrondi. |
| [SEAL](#SEAL) | Sceau. |
| [SEAL_10](#SEAL-10) | Étoile à dix branches. |
| [SEAL_12](#SEAL-12) | Étoile à douze branches. |
| [SEAL_16](#SEAL-16) | Étoile à seize branches. |
| [SEAL_24](#SEAL-24) | Étoile à 24 pointes. |
| [SEAL_32](#SEAL-32) | Étoile à 32 pointes. |
| [SEAL_4](#SEAL-4) | Étoile à quatre pointes. |
| [SEAL_6](#SEAL-6) | Étoile à six pointes. |
| [SEAL_7](#SEAL-7) | Étoile à sept pointes. |
| [SEAL_8](#SEAL-8) | Étoile à huit pointes. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rectangle à coin unique arrondi. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Objet rectangle à coin unique découpé. |
| [SMILEY_FACE](#SMILEY-FACE) | Visage souriant. |
| [SQUARE_TABS](#SQUARE-TABS) | Onglets carrés. |
| [STAR](#STAR) | Étoile. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Une forme de connecteur droit. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Flèche droite à bandes. |
| [SUN](#SUN) | Soleil. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Flèche en forme de swoosh. |
| [TEARDROP](#TEARDROP) | Goutte. |
| [TEXT_ARCH_DOWN_CURVE](#TEXT-ARCH-DOWN-CURVE) | Courbe d'arc vers le bas, objet WordArt. |
| [TEXT_ARCH_DOWN_POUR](#TEXT-ARCH-DOWN-POUR) | Remplissage d'arc vers le bas, objet WordArt. |
| [TEXT_ARCH_UP_CURVE](#TEXT-ARCH-UP-CURVE) | Courbe d'arc vers le haut, objet WordArt. |
| [TEXT_ARCH_UP_POUR](#TEXT-ARCH-UP-POUR) | Remplissage d'arc vers le haut, objet WordArt. |
| [TEXT_BOX](#TEXT-BOX) | La forme est une zone de texte. |
| [TEXT_BUTTON_CURVE](#TEXT-BUTTON-CURVE) | Courbe de bouton, objet WordArt. |
| [TEXT_BUTTON_POUR](#TEXT-BUTTON-POUR) | Remplissage de bouton, objet WordArt. |
| [TEXT_CAN_DOWN](#TEXT-CAN-DOWN) | Boîte vers le bas, objet WordArt. |
| [TEXT_CAN_UP](#TEXT-CAN-UP) | Boîte vers le haut, objet WordArt. |
| [TEXT_CASCADE_DOWN](#TEXT-CASCADE-DOWN) | Cascade vers le bas, objet WordArt. |
| [TEXT_CASCADE_UP](#TEXT-CASCADE-UP) | Cascade vers le haut, objet WordArt. |
| [TEXT_CHEVRON](#TEXT-CHEVRON) | Chevron, objet WordArt. |
| [TEXT_CHEVRON_INVERTED](#TEXT-CHEVRON-INVERTED) | Chevron inversé, objet WordArt. |
| [TEXT_CIRCLE_CURVE](#TEXT-CIRCLE-CURVE) | Courbe circulaire, objet WordArt. |
| [TEXT_CIRCLE_POUR](#TEXT-CIRCLE-POUR) | Remplissage circulaire, objet WordArt. |
| [TEXT_CURVE](#TEXT-CURVE) | Courbe de texte. |
| [TEXT_CURVE_DOWN](#TEXT-CURVE-DOWN) | Courbe vers le bas, objet WordArt. |
| [TEXT_CURVE_UP](#TEXT-CURVE-UP) | Courbe vers le haut, objet WordArt. |
| [TEXT_DEFLATE](#TEXT-DEFLATE) | Déflater, objet WordArt. |
| [TEXT_DEFLATE_BOTTOM](#TEXT-DEFLATE-BOTTOM) | Déflater en bas, objet WordArt. |
| [TEXT_DEFLATE_INFLATE](#TEXT-DEFLATE-INFLATE) | Déflater gonfler, objet WordArt. |
| [TEXT_DEFLATE_INFLATE_DEFLATE](#TEXT-DEFLATE-INFLATE-DEFLATE) | Déflater gonfler déflater, objet WordArt. |
| [TEXT_DEFLATE_TOP](#TEXT-DEFLATE-TOP) | Déflater en haut, objet WordArt. |
| [TEXT_FADE_DOWN](#TEXT-FADE-DOWN) | Fondu vers le bas, objet WordArt. |
| [TEXT_FADE_LEFT](#TEXT-FADE-LEFT) | Fondu à gauche, objet WordArt. |
| [TEXT_FADE_RIGHT](#TEXT-FADE-RIGHT) | Fondu à droite, objet WordArt. |
| [TEXT_FADE_UP](#TEXT-FADE-UP) | Fondu vers le haut, objet WordArt. |
| [TEXT_HEXAGON](#TEXT-HEXAGON) | Texte hexagone. |
| [TEXT_INFLATE](#TEXT-INFLATE) | Gonfler, objet WordArt. |
| [TEXT_INFLATE_BOTTOM](#TEXT-INFLATE-BOTTOM) | Gonfler en bas, objet WordArt. |
| [TEXT_INFLATE_TOP](#TEXT-INFLATE-TOP) | Gonfler en haut, objet WordArt. |
| [TEXT_OCTAGON](#TEXT-OCTAGON) | Texte octogone. |
| [TEXT_ON_CURVE](#TEXT-ON-CURVE) | Texte sur courbe. |
| [TEXT_ON_RING](#TEXT-ON-RING) | Texte sur anneau. |
| [TEXT_PLAIN_TEXT](#TEXT-PLAIN-TEXT) | Texte brut, objet WordArt. |
| [TEXT_RING](#TEXT-RING) | Texte anneau. |
| [TEXT_RING_INSIDE](#TEXT-RING-INSIDE) | Anneau intérieur, objet WordArt. |
| [TEXT_RING_OUTSIDE](#TEXT-RING-OUTSIDE) | Anneau extérieur, objet WordArt. |
| [TEXT_SIMPLE](#TEXT-SIMPLE) | Texte simple. |
| [TEXT_SLANT_DOWN](#TEXT-SLANT-DOWN) | Inclinaison vers le bas, objet WordArt. |
| [TEXT_SLANT_UP](#TEXT-SLANT-UP) | Inclinaison vers le haut, objet WordArt. |
| [TEXT_STOP](#TEXT-STOP) | Arrêt, objet WordArt. |
| [TEXT_TRIANGLE](#TEXT-TRIANGLE) | Triangle, objet WordArt. |
| [TEXT_TRIANGLE_INVERTED](#TEXT-TRIANGLE-INVERTED) | Triangle inversé, objet WordArt. |
| [TEXT_WAVE](#TEXT-WAVE) | Vague de texte. |
| [TEXT_WAVE_1](#TEXT-WAVE-1) | Vague 1, objet WordArt. |
| [TEXT_WAVE_2](#TEXT-WAVE-2) | Vague 2, objet WordArt. |
| [TEXT_WAVE_3](#TEXT-WAVE-3) | Vague 3, objet WordArt. |
| [TEXT_WAVE_4](#TEXT-WAVE-4) | Vague 4, objet WordArt. |
| [THICK_ARROW](#THICK-ARROW) | Flèche épaisse. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Rectangle à un seul coin découpé et arrondi. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rectangle à coins arrondis du même côté. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Rectangle à coins du même côté découpés. |
| [TRAPEZOID](#TRAPEZOID) | Trapèze. |
| [TRIANGLE](#TRIANGLE) | Triangle. |
| [UP_ARROW](#UP-ARROW) | Flèche vers le haut. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Annotation flèche vers le haut. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Flèche haut-bas. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Annotation flèche haut-bas. |
| [UTURN_ARROW](#UTURN-ARROW) | Flèche en U. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Défilement vertical. |
| [WAVE](#WAVE) | Vague. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Annotation coin d'ellipse. |
| [WEDGE_PIE](#WEDGE-PIE) | Quart de tarte. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Annotation coin de rectangle. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Annotation coin de rectangle R. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String shapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int shapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Appel de bordure accentuée 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Appel de bordure accentuée 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Appel de bordure accentuée 3.

### ACCENT_BORDER_CALLOUT_90 {#ACCENT-BORDER-CALLOUT-90}
```
public static int ACCENT_BORDER_CALLOUT_90
```


Appel de bordure accentuée 90.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Une forme d'appel accentué avec une flèche.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Une forme d'appel accentué avec deux flèches.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Une forme d'appel accentué avec trois flèches.

### ACCENT_CALLOUT_90 {#ACCENT-CALLOUT-90}
```
public static int ACCENT_CALLOUT_90
```


Appel accentué 90.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Bouton d'action retour précédent.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Bouton d'action début.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Bouton d'action vierge.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Bouton d'action document.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Bouton d'action fin.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Bouton d'action avancer suivant.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Bouton d'action d'aide.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Bouton d'action accueil.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Bouton d'action information.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Bouton d'action film.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Bouton d'action retour.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Bouton d'action son.

### ARC {#ARC}
```
public static int ARC
```


Arc.

### ARROW {#ARROW}
```
public static int ARROW
```


Flèche.

### BALLOON {#BALLOON}
```
public static int BALLOON
```


Bulle.

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Flèche courbée.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Une forme de connecteur coudé avec deux segments.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Une forme de connecteur coudé avec trois segments.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Une forme de connecteur coudé avec quatre segments.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Une forme de connecteur coudé avec cinq segments.

### BENT_UP_ARROW {#BENT-UP-ARROW}
```
public static int BENT_UP_ARROW
```


Flèche courbée vers le haut.

### BEVEL {#BEVEL}
```
public static int BEVEL
```


Biseau.

### BLOCK_ARC {#BLOCK-ARC}
```
public static int BLOCK_ARC
```


Arc de bloc.

### BORDER_CALLOUT_1 {#BORDER-CALLOUT-1}
```
public static int BORDER_CALLOUT_1
```


Appel de bordure 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Appel de bordure 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Appel de bordure 3.

### BORDER_CALLOUT_90 {#BORDER-CALLOUT-90}
```
public static int BORDER_CALLOUT_90
```


Appel de bordure 90.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Paire d'accolades

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Paire de crochets.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Une forme d'annotation avec une flèche.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Une forme d'annotation avec deux flèches.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Une forme d'annotation avec trois flèches.

### CALLOUT_90 {#CALLOUT-90}
```
public static int CALLOUT_90
```


Annotation 90.

### CAN {#CAN}
```
public static int CAN
```


Boîte.

### CHART_PLUS {#CHART-PLUS}
```
public static int CHART_PLUS
```


Graphique plus.

 **Remarks:** 

Applicable uniquement aux formes DML.

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Graphique étoile.

 **Remarks:** 

Applicable uniquement aux formes DML.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Graphique X.

 **Remarks:** 

Applicable uniquement aux formes DML.

### CHEVRON {#CHEVRON}
```
public static int CHEVRON
```


Chevron.

### CHORD {#CHORD}
```
public static int CHORD
```


Corde.

 **Remarks:** 

Applicable uniquement aux formes DML.

### CIRCULAR_ARROW {#CIRCULAR-ARROW}
```
public static int CIRCULAR_ARROW
```


Flèche circulaire.

### CLOUD {#CLOUD}
```
public static int CLOUD
```


Nuage.

 **Remarks:** 

Applicable uniquement aux formes DML.

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Annotation nuage.

### CORNER {#CORNER}
```
public static int CORNER
```


Coin.

 **Remarks:** 

Applicable uniquement aux formes DML.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Onglets d'angle.

 **Remarks:** 

Applicable uniquement aux formes DML.

### CUBE {#CUBE}
```
public static int CUBE
```


Cube.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Une forme de connecteur courbé avec deux segments.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Une forme de connecteur courbé avec trois segments.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Une forme de connecteur courbé avec quatre segments.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Une forme de connecteur courbé avec cinq segments.

### CURVED_DOWN_ARROW {#CURVED-DOWN-ARROW}
```
public static int CURVED_DOWN_ARROW
```


Flèche courbée vers le bas.

### CURVED_LEFT_ARROW {#CURVED-LEFT-ARROW}
```
public static int CURVED_LEFT_ARROW
```


Flèche courbée vers la gauche.

### CURVED_RIGHT_ARROW {#CURVED-RIGHT-ARROW}
```
public static int CURVED_RIGHT_ARROW
```


Flèche courbée vers la droite.

### CURVED_UP_ARROW {#CURVED-UP-ARROW}
```
public static int CURVED_UP_ARROW
```


Flèche courbée vers le haut

### CUSTOM_SHAPE {#CUSTOM-SHAPE}
```
public static int CUSTOM_SHAPE
```


Ce type de forme semble être destiné aux formes qui ne font pas partie de l'ensemble standard des formes automatiques dans Microsoft Word. Par exemple, si vous insérez une nouvelle forme automatique depuis ClipArt.

Vous ne pouvez pas créer de formes de ce type dans le document.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Décagone.

 **Remarks:** 

Applicable uniquement aux formes DML.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rectangle à coins diagonaux arrondis.

 **Remarks:** 

Applicable uniquement aux formes DML.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Rectangle à coins diagonaux découpés.

 **Remarks:** 

Applicable uniquement aux formes DML.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Bande diagonale.

 **Remarks:** 

Applicable uniquement aux formes DML.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Losange.

### DODECAGON {#DODECAGON}
```
public static int DODECAGON
```


Dodécagone.

 **Remarks:** 

Applicable uniquement aux formes DML.

### DONUT {#DONUT}
```
public static int DONUT
```


Beignet.

### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```


Double vague.

### DOWN_ARROW {#DOWN-ARROW}
```
public static int DOWN_ARROW
```


Flèche vers le bas.

### DOWN_ARROW_CALLOUT {#DOWN-ARROW-CALLOUT}
```
public static int DOWN_ARROW_CALLOUT
```


Appel de flèche vers le bas.

### ELLIPSE {#ELLIPSE}
```
public static int ELLIPSE
```


Ellipse.

### ELLIPSE_RIBBON {#ELLIPSE-RIBBON}
```
public static int ELLIPSE_RIBBON
```


Ruban d'ellipse.

### ELLIPSE_RIBBON_2 {#ELLIPSE-RIBBON-2}
```
public static int ELLIPSE_RIBBON_2
```


Ruban d'ellipse 2.

### FLOW_CHART_ALTERNATE_PROCESS {#FLOW-CHART-ALTERNATE-PROCESS}
```
public static int FLOW_CHART_ALTERNATE_PROCESS
```


Processus alternatif du diagramme de flux.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Collation du diagramme de flux.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Connecteur du diagramme de flux.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Décision du diagramme de flux.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Délai du diagramme de flux.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Affichage du diagramme de flux.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Document du diagramme de flux.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Extraction du diagramme de flux.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Entrée‑sortie du diagramme de flux.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Stockage interne du diagramme de flux.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Disque magnétique du diagramme de flux.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Tambour magnétique du diagramme de flux.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Bande magnétique du diagramme de flux.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Entrée manuelle du diagramme de flux.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Opération manuelle du diagramme de flux.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Fusion du diagramme de flux.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Diagramme de flux multi‑document.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Stockage hors ligne du diagramme de flux.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Connecteur hors page du diagramme de flux.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Stockage en ligne du diagramme de flux.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Diagramme de flux ou.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Processus prédéfini du diagramme de flux

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Préparation du diagramme de flux.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Processus du diagramme de flux.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Carte perforée du diagramme de flux.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Ruban perforé du diagramme de flux.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Tri du diagramme de flux.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Jonction de sommation du diagramme de flux.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Terminateur du diagramme de flux.

### FOLDED_CORNER {#FOLDED-CORNER}
```
public static int FOLDED_CORNER
```


Coin plié.

### FRAME {#FRAME}
```
public static int FRAME
```


Cadre.

 **Remarks:** 

Applicable uniquement aux formes DML.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Entonnoir.

 **Remarks:** 

Applicable uniquement aux formes DML.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Engrenage à six dents.

 **Remarks:** 

Applicable uniquement aux formes DML.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Engrenage à neuf dents.

 **Remarks:** 

Applicable uniquement aux formes DML.

### GROUP {#GROUP}
```
public static int GROUP
```


La forme est une forme groupée.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Demi-cadre.

 **Remarks:** 

Applicable uniquement aux formes DML.

### HEART {#HEART}
```
public static int HEART
```


Cœur.

### HEPTAGON {#HEPTAGON}
```
public static int HEPTAGON
```


Heptagone.

 **Remarks:** 

Applicable uniquement aux formes DML.

### HEXAGON {#HEXAGON}
```
public static int HEXAGON
```


Hexagone.

### HOME_PLATE {#HOME-PLATE}
```
public static int HOME_PLATE
```


Plaque de base.

### HORIZONTAL_SCROLL {#HORIZONTAL-SCROLL}
```
public static int HORIZONTAL_SCROLL
```


Défilement horizontal.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


La forme est une image.

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Ligne inverse.

 **Remarks:** 

Applicable uniquement aux formes DML.

### IRREGULAR_SEAL_1 {#IRREGULAR-SEAL-1}
```
public static int IRREGULAR_SEAL_1
```


Joint irrégulier 1.

### IRREGULAR_SEAL_2 {#IRREGULAR-SEAL-2}
```
public static int IRREGULAR_SEAL_2
```


Joint irrégulier 2.

### LEFT_ARROW {#LEFT-ARROW}
```
public static int LEFT_ARROW
```


Flèche gauche.

### LEFT_ARROW_CALLOUT {#LEFT-ARROW-CALLOUT}
```
public static int LEFT_ARROW_CALLOUT
```


Appel de flèche gauche.

### LEFT_BRACE {#LEFT-BRACE}
```
public static int LEFT_BRACE
```


Accolade gauche.

### LEFT_BRACKET {#LEFT-BRACKET}
```
public static int LEFT_BRACKET
```


Crochet gauche.

### LEFT_CIRCULAR_ARROW {#LEFT-CIRCULAR-ARROW}
```
public static int LEFT_CIRCULAR_ARROW
```


Flèche circulaire gauche.

 **Remarks:** 

Applicable uniquement aux formes DML.

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Flèche gauche-droite.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Appel de flèche gauche-droite.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Flèche circulaire gauche‑droite.

 **Remarks:** 

Applicable uniquement aux formes DML.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Ruban gauche‑droite.

 **Remarks:** 

Applicable uniquement aux formes DML.

### LEFT_RIGHT_UP_ARROW {#LEFT-RIGHT-UP-ARROW}
```
public static int LEFT_RIGHT_UP_ARROW
```


Flèche haut gauche‑droite.

### LEFT_UP_ARROW {#LEFT-UP-ARROW}
```
public static int LEFT_UP_ARROW
```


Flèche haut gauche.

### LIGHTNING_BOLT {#LIGHTNING-BOLT}
```
public static int LIGHTNING_BOLT
```


Éclair.

### LINE {#LINE}
```
public static int LINE
```


Ligne.

### MATH_DIVIDE {#MATH-DIVIDE}
```
public static int MATH_DIVIDE
```


Division mathématique.

 **Remarks:** 

Applicable uniquement aux formes DML.

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Égalité mathématique.

 **Remarks:** 

Applicable uniquement aux formes DML.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Soustraction mathématique.

 **Remarks:** 

Applicable uniquement aux formes DML.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Multiplication mathématique.

 **Remarks:** 

Applicable uniquement aux formes DML.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Inégalité mathématique.

 **Remarks:** 

Applicable uniquement aux formes DML.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Addition mathématique.

 **Remarks:** 

Applicable uniquement aux formes DML.

### MIN_VALUE {#MIN-VALUE}
```
public static int MIN_VALUE
```


Réservé à l'usage du système.

### MOON {#MOON}
```
public static int MOON
```


Lune.

### NON_ISOSCELES_TRAPEZOID {#NON-ISOSCELES-TRAPEZOID}
```
public static int NON_ISOSCELES_TRAPEZOID
```


Trapèze non isocèle.

 **Remarks:** 

Applicable uniquement aux formes DML.

### NON_PRIMITIVE {#NON-PRIMITIVE}
```
public static int NON_PRIMITIVE
```


Une forme dessinée par l'utilisateur et composée de plusieurs segments et/ou sommets (courbe, forme libre ou griffonnage).

Vous ne pouvez pas créer de formes de ce type dans le document.

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Flèche droite à encoches.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


NoSmoking.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Octogone.

### OLE_CONTROL {#OLE-CONTROL}
```
public static int OLE_CONTROL
```


La forme est un contrôle ActiveX.

Vous ne pouvez pas créer de formes de ce type dans le document.

### OLE_OBJECT {#OLE-OBJECT}
```
public static int OLE_OBJECT
```


La forme est un objet OLE.

Vous ne pouvez pas créer de formes de ce type dans le document.

### PARALLELOGRAM {#PARALLELOGRAM}
```
public static int PARALLELOGRAM
```


Parallélogramme.

### PENTAGON {#PENTAGON}
```
public static int PENTAGON
```


Pentagone.

### PIE {#PIE}
```
public static int PIE
```


Tarte.

 **Remarks:** 

Applicable uniquement aux formes DML.

### PLAQUE {#PLAQUE}
```
public static int PLAQUE
```


Plaque.

### PLAQUE_TABS {#PLAQUE-TABS}
```
public static int PLAQUE_TABS
```


Onglets de plaque.

 **Remarks:** 

Applicable uniquement aux formes DML.

### PLUS {#PLUS}
```
public static int PLUS
```


Plus.

### QUAD_ARROW {#QUAD-ARROW}
```
public static int QUAD_ARROW
```


Flèche quadruple.

### QUAD_ARROW_CALLOUT {#QUAD-ARROW-CALLOUT}
```
public static int QUAD_ARROW_CALLOUT
```


Appel de flèche quadruple.

### RECTANGLE {#RECTANGLE}
```
public static int RECTANGLE
```


Rectangle.

### RIBBON {#RIBBON}
```
public static int RIBBON
```


Ruban.

### RIBBON_2 {#RIBBON-2}
```
public static int RIBBON_2
```


Ruban 2.

### RIGHT_ARROW_CALLOUT {#RIGHT-ARROW-CALLOUT}
```
public static int RIGHT_ARROW_CALLOUT
```


Appel de flèche droite

### RIGHT_BRACE {#RIGHT-BRACE}
```
public static int RIGHT_BRACE
```


Accolade droite.

### RIGHT_BRACKET {#RIGHT-BRACKET}
```
public static int RIGHT_BRACKET
```


Crochet droit.

### RIGHT_TRIANGLE {#RIGHT-TRIANGLE}
```
public static int RIGHT_TRIANGLE
```


Triangle droit.

### ROUND_RECTANGLE {#ROUND-RECTANGLE}
```
public static int ROUND_RECTANGLE
```


Rectangle arrondi.

### SEAL {#SEAL}
```
public static int SEAL
```


Sceau.

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Étoile à dix branches.

 **Remarks:** 

Applicable uniquement aux formes DML.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Étoile à douze branches.

 **Remarks:** 

Applicable uniquement aux formes DML.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Étoile à seize branches.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Étoile à 24 pointes.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Étoile à 32 pointes.

### SEAL_4 {#SEAL-4}
```
public static int SEAL_4
```


Étoile à quatre pointes.

### SEAL_6 {#SEAL-6}
```
public static int SEAL_6
```


Étoile à six pointes.

 **Remarks:** 

Applicable uniquement aux formes DML.

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Étoile à sept pointes.

 **Remarks:** 

Applicable uniquement aux formes DML.

### SEAL_8 {#SEAL-8}
```
public static int SEAL_8
```


Étoile à huit pointes.

### SINGLE_CORNER_ROUNDED {#SINGLE-CORNER-ROUNDED}
```
public static int SINGLE_CORNER_ROUNDED
```


Rectangle à coin unique arrondi.

 **Remarks:** 

Applicable uniquement aux formes DML.

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Objet rectangle à coin unique découpé.

 **Remarks:** 

Applicable uniquement aux formes DML.

### SMILEY_FACE {#SMILEY-FACE}
```
public static int SMILEY_FACE
```


Visage souriant.

### SQUARE_TABS {#SQUARE-TABS}
```
public static int SQUARE_TABS
```


Onglets carrés.

 **Remarks:** 

Applicable uniquement aux formes DML.

### STAR {#STAR}
```
public static int STAR
```


Étoile.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Une forme de connecteur droit.

### STRIPED_RIGHT_ARROW {#STRIPED-RIGHT-ARROW}
```
public static int STRIPED_RIGHT_ARROW
```


Flèche droite à bandes.

### SUN {#SUN}
```
public static int SUN
```


Soleil.

### SWOOSH_ARROW {#SWOOSH-ARROW}
```
public static int SWOOSH_ARROW
```


Flèche en forme de swoosh.

 **Remarks:** 

Applicable uniquement aux formes DML.

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Goutte.

 **Remarks:** 

Applicable uniquement aux formes DML.

### TEXT_ARCH_DOWN_CURVE {#TEXT-ARCH-DOWN-CURVE}
```
public static int TEXT_ARCH_DOWN_CURVE
```


Courbe d'arc vers le bas, objet WordArt.

### TEXT_ARCH_DOWN_POUR {#TEXT-ARCH-DOWN-POUR}
```
public static int TEXT_ARCH_DOWN_POUR
```


Remplissage d'arc vers le bas, objet WordArt.

### TEXT_ARCH_UP_CURVE {#TEXT-ARCH-UP-CURVE}
```
public static int TEXT_ARCH_UP_CURVE
```


Courbe d'arc vers le haut, objet WordArt.

### TEXT_ARCH_UP_POUR {#TEXT-ARCH-UP-POUR}
```
public static int TEXT_ARCH_UP_POUR
```


Remplissage d'arc vers le haut, objet WordArt.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


La forme est une zone de texte. Notez que les formes de nombreux autres types peuvent également contenir du texte. Une forme n'a pas besoin d'être de ce type pour contenir du texte.

### TEXT_BUTTON_CURVE {#TEXT-BUTTON-CURVE}
```
public static int TEXT_BUTTON_CURVE
```


Courbe de bouton, objet WordArt.

### TEXT_BUTTON_POUR {#TEXT-BUTTON-POUR}
```
public static int TEXT_BUTTON_POUR
```


Remplissage de bouton, objet WordArt.

### TEXT_CAN_DOWN {#TEXT-CAN-DOWN}
```
public static int TEXT_CAN_DOWN
```


Boîte vers le bas, objet WordArt.

### TEXT_CAN_UP {#TEXT-CAN-UP}
```
public static int TEXT_CAN_UP
```


Boîte vers le haut, objet WordArt.

### TEXT_CASCADE_DOWN {#TEXT-CASCADE-DOWN}
```
public static int TEXT_CASCADE_DOWN
```


Cascade vers le bas, objet WordArt.

### TEXT_CASCADE_UP {#TEXT-CASCADE-UP}
```
public static int TEXT_CASCADE_UP
```


Cascade vers le haut, objet WordArt.

### TEXT_CHEVRON {#TEXT-CHEVRON}
```
public static int TEXT_CHEVRON
```


Chevron, objet WordArt.

### TEXT_CHEVRON_INVERTED {#TEXT-CHEVRON-INVERTED}
```
public static int TEXT_CHEVRON_INVERTED
```


Chevron inversé, objet WordArt.

### TEXT_CIRCLE_CURVE {#TEXT-CIRCLE-CURVE}
```
public static int TEXT_CIRCLE_CURVE
```


Courbe circulaire, objet WordArt.

### TEXT_CIRCLE_POUR {#TEXT-CIRCLE-POUR}
```
public static int TEXT_CIRCLE_POUR
```


Remplissage circulaire, objet WordArt.

### TEXT_CURVE {#TEXT-CURVE}
```
public static int TEXT_CURVE
```


Courbe de texte.

### TEXT_CURVE_DOWN {#TEXT-CURVE-DOWN}
```
public static int TEXT_CURVE_DOWN
```


Courbe vers le bas, objet WordArt.

### TEXT_CURVE_UP {#TEXT-CURVE-UP}
```
public static int TEXT_CURVE_UP
```


Courbe vers le haut, objet WordArt.

### TEXT_DEFLATE {#TEXT-DEFLATE}
```
public static int TEXT_DEFLATE
```


Déflater, objet WordArt.

### TEXT_DEFLATE_BOTTOM {#TEXT-DEFLATE-BOTTOM}
```
public static int TEXT_DEFLATE_BOTTOM
```


Déflater en bas, objet WordArt.

### TEXT_DEFLATE_INFLATE {#TEXT-DEFLATE-INFLATE}
```
public static int TEXT_DEFLATE_INFLATE
```


Déflater gonfler, objet WordArt.

### TEXT_DEFLATE_INFLATE_DEFLATE {#TEXT-DEFLATE-INFLATE-DEFLATE}
```
public static int TEXT_DEFLATE_INFLATE_DEFLATE
```


Déflater gonfler déflater, objet WordArt.

### TEXT_DEFLATE_TOP {#TEXT-DEFLATE-TOP}
```
public static int TEXT_DEFLATE_TOP
```


Déflater en haut, objet WordArt.

### TEXT_FADE_DOWN {#TEXT-FADE-DOWN}
```
public static int TEXT_FADE_DOWN
```


Fondu vers le bas, objet WordArt.

### TEXT_FADE_LEFT {#TEXT-FADE-LEFT}
```
public static int TEXT_FADE_LEFT
```


Fondu à gauche, objet WordArt.

### TEXT_FADE_RIGHT {#TEXT-FADE-RIGHT}
```
public static int TEXT_FADE_RIGHT
```


Fondu à droite, objet WordArt.

### TEXT_FADE_UP {#TEXT-FADE-UP}
```
public static int TEXT_FADE_UP
```


Fondu vers le haut, objet WordArt.

### TEXT_HEXAGON {#TEXT-HEXAGON}
```
public static int TEXT_HEXAGON
```


Texte hexagone.

### TEXT_INFLATE {#TEXT-INFLATE}
```
public static int TEXT_INFLATE
```


Gonfler, objet WordArt.

### TEXT_INFLATE_BOTTOM {#TEXT-INFLATE-BOTTOM}
```
public static int TEXT_INFLATE_BOTTOM
```


Gonfler en bas, objet WordArt.

### TEXT_INFLATE_TOP {#TEXT-INFLATE-TOP}
```
public static int TEXT_INFLATE_TOP
```


Gonfler en haut, objet WordArt.

### TEXT_OCTAGON {#TEXT-OCTAGON}
```
public static int TEXT_OCTAGON
```


Texte octogone.

### TEXT_ON_CURVE {#TEXT-ON-CURVE}
```
public static int TEXT_ON_CURVE
```


Texte sur courbe.

### TEXT_ON_RING {#TEXT-ON-RING}
```
public static int TEXT_ON_RING
```


Texte sur anneau.

### TEXT_PLAIN_TEXT {#TEXT-PLAIN-TEXT}
```
public static int TEXT_PLAIN_TEXT
```


Texte brut, objet WordArt.

### TEXT_RING {#TEXT-RING}
```
public static int TEXT_RING
```


Texte anneau.

### TEXT_RING_INSIDE {#TEXT-RING-INSIDE}
```
public static int TEXT_RING_INSIDE
```


Anneau intérieur, objet WordArt.

### TEXT_RING_OUTSIDE {#TEXT-RING-OUTSIDE}
```
public static int TEXT_RING_OUTSIDE
```


Anneau extérieur, objet WordArt.

### TEXT_SIMPLE {#TEXT-SIMPLE}
```
public static int TEXT_SIMPLE
```


Texte simple.

### TEXT_SLANT_DOWN {#TEXT-SLANT-DOWN}
```
public static int TEXT_SLANT_DOWN
```


Inclinaison vers le bas, objet WordArt.

### TEXT_SLANT_UP {#TEXT-SLANT-UP}
```
public static int TEXT_SLANT_UP
```


Inclinaison vers le haut, objet WordArt.

### TEXT_STOP {#TEXT-STOP}
```
public static int TEXT_STOP
```


Arrêt, objet WordArt.

### TEXT_TRIANGLE {#TEXT-TRIANGLE}
```
public static int TEXT_TRIANGLE
```


Triangle, objet WordArt.

### TEXT_TRIANGLE_INVERTED {#TEXT-TRIANGLE-INVERTED}
```
public static int TEXT_TRIANGLE_INVERTED
```


Triangle inversé, objet WordArt.

### TEXT_WAVE {#TEXT-WAVE}
```
public static int TEXT_WAVE
```


Vague de texte.

### TEXT_WAVE_1 {#TEXT-WAVE-1}
```
public static int TEXT_WAVE_1
```


Vague 1, objet WordArt.

### TEXT_WAVE_2 {#TEXT-WAVE-2}
```
public static int TEXT_WAVE_2
```


Vague 2, objet WordArt.

### TEXT_WAVE_3 {#TEXT-WAVE-3}
```
public static int TEXT_WAVE_3
```


Vague 3, objet WordArt.

### TEXT_WAVE_4 {#TEXT-WAVE-4}
```
public static int TEXT_WAVE_4
```


Vague 4, objet WordArt.

### THICK_ARROW {#THICK-ARROW}
```
public static int THICK_ARROW
```


Flèche épaisse.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Rectangle à un seul coin découpé et arrondi.

 **Remarks:** 

Applicable uniquement aux formes DML.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rectangle à coins arrondis du même côté.

 **Remarks:** 

Applicable uniquement aux formes DML.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Rectangle à coins du même côté découpés.

 **Remarks:** 

Applicable uniquement aux formes DML.

### TRAPEZOID {#TRAPEZOID}
```
public static int TRAPEZOID
```


Trapèze.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Triangle.

### UP_ARROW {#UP-ARROW}
```
public static int UP_ARROW
```


Flèche vers le haut.

### UP_ARROW_CALLOUT {#UP-ARROW-CALLOUT}
```
public static int UP_ARROW_CALLOUT
```


Annotation flèche vers le haut.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Flèche haut-bas.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Annotation flèche haut-bas.

### UTURN_ARROW {#UTURN-ARROW}
```
public static int UTURN_ARROW
```


Flèche en U.

### VERTICAL_SCROLL {#VERTICAL-SCROLL}
```
public static int VERTICAL_SCROLL
```


Défilement vertical.

### WAVE {#WAVE}
```
public static int WAVE
```


Vague.

### WEDGE_ELLIPSE_CALLOUT {#WEDGE-ELLIPSE-CALLOUT}
```
public static int WEDGE_ELLIPSE_CALLOUT
```


Annotation coin d'ellipse.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Quart de tarte.

 **Remarks:** 

Applicable uniquement aux formes DML.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Annotation coin de rectangle.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Annotation coin de rectangle R.

### length {#length}
```
public static int length
```


### fromName(String shapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shapeType) {#getName-int}
```
public static String getName(int shapeType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeType | int |  |

**Returns:**
java.lang.String
