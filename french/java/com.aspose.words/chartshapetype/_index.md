---
title: "ChartShapeType"
linktitle: "ChartShapeType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de forme des éléments du graphique en Java."
type: docs
weight: 90
url: /fr/java/com.aspose.words/chartshapetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartShapeType
```

Spécifie le type de forme des éléments de graphique.

 **Examples:** 

Montre comment définir le remplissage, le trait et le formatage des infobulles pour les étiquettes de données du graphique.

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
## Champs

| Champ | Description |
| --- | --- |
| [ACCENT_BORDER_CALLOUT_1](#ACCENT-BORDER-CALLOUT-1) | Infobulle accentuée avec bordure 1. |
| [ACCENT_BORDER_CALLOUT_2](#ACCENT-BORDER-CALLOUT-2) | Infobulle accentuée avec bordure 2. |
| [ACCENT_BORDER_CALLOUT_3](#ACCENT-BORDER-CALLOUT-3) | Infobulle accentuée avec bordure 3. |
| [ACCENT_CALLOUT_1](#ACCENT-CALLOUT-1) | Infobulle accentuée 1. |
| [ACCENT_CALLOUT_2](#ACCENT-CALLOUT-2) | Infobulle accentuée 2. |
| [ACCENT_CALLOUT_3](#ACCENT-CALLOUT-3) | Infobulle accentuée 3. |
| [ACTION_BUTTON_BACK_PREVIOUS](#ACTION-BUTTON-BACK-PREVIOUS) | Bouton Retour ou précédent. |
| [ACTION_BUTTON_BEGINNING](#ACTION-BUTTON-BEGINNING) | Bouton Début. |
| [ACTION_BUTTON_BLANK](#ACTION-BUTTON-BLANK) | Bouton Vide. |
| [ACTION_BUTTON_DOCUMENT](#ACTION-BUTTON-DOCUMENT) | Bouton Document. |
| [ACTION_BUTTON_END](#ACTION-BUTTON-END) | Bouton Fin. |
| [ACTION_BUTTON_FORWARD_NEXT](#ACTION-BUTTON-FORWARD-NEXT) | Bouton Avancer ou suivant. |
| [ACTION_BUTTON_HELP](#ACTION-BUTTON-HELP) | Bouton Aide. |
| [ACTION_BUTTON_HOME](#ACTION-BUTTON-HOME) | Bouton Accueil. |
| [ACTION_BUTTON_INFORMATION](#ACTION-BUTTON-INFORMATION) | Bouton Information. |
| [ACTION_BUTTON_MOVIE](#ACTION-BUTTON-MOVIE) | Bouton Film. |
| [ACTION_BUTTON_RETURN](#ACTION-BUTTON-RETURN) | Bouton Retour. |
| [ACTION_BUTTON_SOUND](#ACTION-BUTTON-SOUND) | Bouton Son. |
| [ARC](#ARC) | Arc. |
| [ARROW](#ARROW) | Flèche. |
| [BENT_ARROW](#BENT-ARROW) | Flèche courbée. |
| [BENT_CONNECTOR_2](#BENT-CONNECTOR-2) | Connecteur courbé 2. |
| [BENT_CONNECTOR_3](#BENT-CONNECTOR-3) | Connecteur courbé 3. |
| [BENT_CONNECTOR_4](#BENT-CONNECTOR-4) | Connecteur courbé 4. |
| [BENT_CONNECTOR_5](#BENT-CONNECTOR-5) | Connecteur courbé 5. |
| [BENT_UP_ARROW](#BENT-UP-ARROW) | Flèche courbée vers le haut. |
| [BEVEL](#BEVEL) | Biseau. |
| [BLOCK_ARC](#BLOCK-ARC) | Arc de bloc. |
| [BORDER_CALLOUT_1](#BORDER-CALLOUT-1) | Encadré avec bordure 1. |
| [BORDER_CALLOUT_2](#BORDER-CALLOUT-2) | Encadré avec bordure 2. |
| [BORDER_CALLOUT_3](#BORDER-CALLOUT-3) | Encadré avec bordure 3. |
| [BRACE_PAIR](#BRACE-PAIR) | Paire d'accolades. |
| [BRACKET_PAIR](#BRACKET-PAIR) | Paire de crochets. |
| [CALLOUT_1](#CALLOUT-1) | Encadré 1. |
| [CALLOUT_2](#CALLOUT-2) | Encadré 2. |
| [CALLOUT_3](#CALLOUT-3) | Encadré 3. |
| [CAN](#CAN) | Boîte. |
| [CHART_PLUS](#CHART-PLUS) | Graphique plus. |
| [CHART_STAR](#CHART-STAR) | Graphique étoile. |
| [CHART_X](#CHART-X) | Graphique X. |
| [CHEVRON](#CHEVRON) | Chevron. |
| [CHORD](#CHORD) | Corde. |
| [CIRCULAR_ARROW](#CIRCULAR-ARROW) | Flèche circulaire. |
| [CLOUD](#CLOUD) | Nuage. |
| [CLOUD_CALLOUT](#CLOUD-CALLOUT) | Encadré nuage. |
| [CORNER](#CORNER) | Coin. |
| [CORNER_TABS](#CORNER-TABS) | Onglets d'angle. |
| [CUBE](#CUBE) | Cube. |
| [CURVED_CONNECTOR_2](#CURVED-CONNECTOR-2) | Connecteur courbe 2. |
| [CURVED_CONNECTOR_3](#CURVED-CONNECTOR-3) | Connecteur courbe 3. |
| [CURVED_CONNECTOR_4](#CURVED-CONNECTOR-4) | Connecteur courbe 4. |
| [CURVED_CONNECTOR_5](#CURVED-CONNECTOR-5) | Connecteur courbe 5. |
| [CURVED_DOWN_ARROW](#CURVED-DOWN-ARROW) | Flèche courbée vers le bas. |
| [CURVED_LEFT_ARROW](#CURVED-LEFT-ARROW) | Flèche courbée vers la gauche. |
| [CURVED_RIGHT_ARROW](#CURVED-RIGHT-ARROW) | Flèche courbée vers la droite. |
| [CURVED_UP_ARROW](#CURVED-UP-ARROW) | Flèche courbée vers le haut. |
| [DECAGON](#DECAGON) | Décagone. |
| [DEFAULT](#DEFAULT) | Indique qu'aucune forme n'est définie pour l'élément du graphique. |
| [DIAGONAL_CORNERS_ROUNDED](#DIAGONAL-CORNERS-ROUNDED) | Rectangle à coins diagonaux arrondis. |
| [DIAGONAL_CORNERS_SNIPPED](#DIAGONAL-CORNERS-SNIPPED) | Rectangle à coins diagonaux découpés. |
| [DIAGONAL_STRIPE](#DIAGONAL-STRIPE) | Bande diagonale. |
| [DIAMOND](#DIAMOND) | Losange. |
| [DODECAGON](#DODECAGON) | Dodécagone. |
| [DONUT](#DONUT) | Beignet. |
| [DOUBLE_WAVE](#DOUBLE-WAVE) | Double vague. |
| [DOWN_ARROW](#DOWN-ARROW) | Flèche vers le bas. |
| [DOWN_ARROW_CALLOUT](#DOWN-ARROW-CALLOUT) | Bulle flèche vers le bas. |
| [ELLIPSE](#ELLIPSE) | Ellipse. |
| [ELLIPSE_RIBBON](#ELLIPSE-RIBBON) | Ruban d'ellipse. |
| [ELLIPSE_RIBBON_2](#ELLIPSE-RIBBON-2) | Ruban d'ellipse 2. |
| [FLOW_CHART_ALTERNATE_PROCESS](#FLOW-CHART-ALTERNATE-PROCESS) | Flux de processus alternatif. |
| [FLOW_CHART_COLLATE](#FLOW-CHART-COLLATE) | Flux de regroupement. |
| [FLOW_CHART_CONNECTOR](#FLOW-CHART-CONNECTOR) | Flux de connecteur. |
| [FLOW_CHART_DECISION](#FLOW-CHART-DECISION) | Flux de décision. |
| [FLOW_CHART_DELAY](#FLOW-CHART-DELAY) | Flux de délai. |
| [FLOW_CHART_DISPLAY](#FLOW-CHART-DISPLAY) | Flux d'affichage. |
| [FLOW_CHART_DOCUMENT](#FLOW-CHART-DOCUMENT) | Flux de document. |
| [FLOW_CHART_EXTRACT](#FLOW-CHART-EXTRACT) | Flux d'extraction. |
| [FLOW_CHART_INPUT_OUTPUT](#FLOW-CHART-INPUT-OUTPUT) | Flux d'entrée/sortie. |
| [FLOW_CHART_INTERNAL_STORAGE](#FLOW-CHART-INTERNAL-STORAGE) | Flux de stockage interne. |
| [FLOW_CHART_MAGNETIC_DISK](#FLOW-CHART-MAGNETIC-DISK) | Flux de disque magnétique. |
| [FLOW_CHART_MAGNETIC_DRUM](#FLOW-CHART-MAGNETIC-DRUM) | Flux de tambour magnétique. |
| [FLOW_CHART_MAGNETIC_TAPE](#FLOW-CHART-MAGNETIC-TAPE) | Flux de bande magnétique. |
| [FLOW_CHART_MANUAL_INPUT](#FLOW-CHART-MANUAL-INPUT) | Flux d'entrée manuelle. |
| [FLOW_CHART_MANUAL_OPERATION](#FLOW-CHART-MANUAL-OPERATION) | Flux d'opération manuelle. |
| [FLOW_CHART_MERGE](#FLOW-CHART-MERGE) | Flux de fusion. |
| [FLOW_CHART_MULTIDOCUMENT](#FLOW-CHART-MULTIDOCUMENT) | Flux multi-documents. |
| [FLOW_CHART_OFFLINE_STORAGE](#FLOW-CHART-OFFLINE-STORAGE) | Flux de stockage hors ligne. |
| [FLOW_CHART_OFFPAGE_CONNECTOR](#FLOW-CHART-OFFPAGE-CONNECTOR) | Flux de connecteur hors page. |
| [FLOW_CHART_ONLINE_STORAGE](#FLOW-CHART-ONLINE-STORAGE) | Flux de stockage en ligne. |
| [FLOW_CHART_OR](#FLOW-CHART-OR) | Flux OU. |
| [FLOW_CHART_PREDEFINED_PROCESS](#FLOW-CHART-PREDEFINED-PROCESS) | Flux de processus prédéfini. |
| [FLOW_CHART_PREPARATION](#FLOW-CHART-PREPARATION) | Flux de préparation. |
| [FLOW_CHART_PROCESS](#FLOW-CHART-PROCESS) | Flux de processus. |
| [FLOW_CHART_PUNCHED_CARD](#FLOW-CHART-PUNCHED-CARD) | Flux de carte perforée. |
| [FLOW_CHART_PUNCHED_TAPE](#FLOW-CHART-PUNCHED-TAPE) | Flux de ruban perforé. |
| [FLOW_CHART_SORT](#FLOW-CHART-SORT) | Flux de tri. |
| [FLOW_CHART_SUMMING_JUNCTION](#FLOW-CHART-SUMMING-JUNCTION) | Flux de jonction de sommation. |
| [FLOW_CHART_TERMINATOR](#FLOW-CHART-TERMINATOR) | Flux de terminaison. |
| [FOLDED_CORNER](#FOLDED-CORNER) | Coin plié. |
| [FRAME](#FRAME) | Cadre. |
| [FUNNEL](#FUNNEL) | Entonnoir. |
| [GEAR_6](#GEAR-6) | Engrenage à six dents. |
| [GEAR_9](#GEAR-9) | Engrenage à neuf dents. |
| [HALF_FRAME](#HALF-FRAME) | Demi-cadre. |
| [HEART](#HEART) | Cœur. |
| [HEPTAGON](#HEPTAGON) | Heptagone. |
| [HEXAGON](#HEXAGON) | Hexagone. |
| [HOME_PLATE](#HOME-PLATE) | Plaque de base. |
| [HORIZONTAL_SCROLL](#HORIZONTAL-SCROLL) | Défilement horizontal. |
| [INVERSE_LINE](#INVERSE-LINE) | Ligne inverse. |
| [IRREGULAR_SEAL_1](#IRREGULAR-SEAL-1) | Joint irrégulier 1. |
| [IRREGULAR_SEAL_2](#IRREGULAR-SEAL-2) | Joint irrégulier 2. |
| [LEFT_ARROW](#LEFT-ARROW) | Flèche gauche. |
| [LEFT_ARROW_CALLOUT](#LEFT-ARROW-CALLOUT) | Annotation flèche gauche. |
| [LEFT_BRACE](#LEFT-BRACE) | Accolade gauche. |
| [LEFT_BRACKET](#LEFT-BRACKET) | Crochet gauche. |
| [LEFT_CIRCULAR_ARROW](#LEFT-CIRCULAR-ARROW) | Flèche circulaire gauche. |
| [LEFT_RIGHT_ARROW](#LEFT-RIGHT-ARROW) | Flèche gauche et droite. |
| [LEFT_RIGHT_ARROW_CALLOUT](#LEFT-RIGHT-ARROW-CALLOUT) | Annotation flèche gauche et droite. |
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
| [MOON](#MOON) | Lune. |
| [NON_ISOSCELES_TRAPEZOID](#NON-ISOSCELES-TRAPEZOID) | Trapèze non isocèle. |
| [NOTCHED_RIGHT_ARROW](#NOTCHED-RIGHT-ARROW) | Flèche droite à encoches. |
| [NO_SMOKING](#NO-SMOKING) | Interdiction de fumer. |
| [OCTAGON](#OCTAGON) | Octogone. |
| [PARALLELOGRAM](#PARALLELOGRAM) | Parallélogramme. |
| [PENTAGON](#PENTAGON) | Pentagone. |
| [PIE](#PIE) | Tarte. |
| [PLAQUE](#PLAQUE) | Plaque. |
| [PLAQUE_TABS](#PLAQUE-TABS) | Onglets de plaque. |
| [PLUS](#PLUS) | Plus. |
| [QUAD_ARROW](#QUAD-ARROW) | Flèche quadruple. |
| [QUAD_ARROW_CALLOUT](#QUAD-ARROW-CALLOUT) | Flèche quadruple d'appel. |
| [RECTANGLE](#RECTANGLE) | Rectangle. |
| [RIBBON](#RIBBON) | Ruban. |
| [RIBBON_2](#RIBBON-2) | Ruban 2. |
| [RIGHT_ARROW_CALLOUT](#RIGHT-ARROW-CALLOUT) | Bulle flèche droite. |
| [RIGHT_BRACE](#RIGHT-BRACE) | Accolade droite. |
| [RIGHT_BRACKET](#RIGHT-BRACKET) | Crochet droit. |
| [RIGHT_TRIANGLE](#RIGHT-TRIANGLE) | Triangle droit. |
| [ROUND_RECTANGLE](#ROUND-RECTANGLE) | Rectangle arrondi. |
| [SEAL_10](#SEAL-10) | Étoile à dix pointes. |
| [SEAL_12](#SEAL-12) | Étoile à douze pointes. |
| [SEAL_16](#SEAL-16) | Étoile à seize pointes. |
| [SEAL_24](#SEAL-24) | Étoile à vingt-quatre pointes. |
| [SEAL_32](#SEAL-32) | Étoile à trente-deux pointes. |
| [SEAL_4](#SEAL-4) | Étoile à quatre pointes. |
| [SEAL_6](#SEAL-6) | Étoile à six pointes. |
| [SEAL_7](#SEAL-7) | Étoile à sept pointes. |
| [SEAL_8](#SEAL-8) | Étoile à huit pointes. |
| [SINGLE_CORNER_ROUNDED](#SINGLE-CORNER-ROUNDED) | Rectangle à coin unique arrondi. |
| [SINGLE_CORNER_SNIPPED](#SINGLE-CORNER-SNIPPED) | Objet rectangle à coin unique découpé. |
| [SMILEY_FACE](#SMILEY-FACE) | Visage souriant. |
| [SQUARE_TABS](#SQUARE-TABS) | Onglets carrés. |
| [STAR](#STAR) | Étoile. |
| [STRAIGHT_CONNECTOR_1](#STRAIGHT-CONNECTOR-1) | Connecteur droit 1. |
| [STRIPED_RIGHT_ARROW](#STRIPED-RIGHT-ARROW) | Flèche droite à bandes. |
| [SUN](#SUN) | Soleil. |
| [SWOOSH_ARROW](#SWOOSH-ARROW) | Flèche en forme de swoosh. |
| [TEARDROP](#TEARDROP) | Goutte. |
| [TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED](#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED) | Rectangle à un seul coin découpé et arrondi. |
| [TOP_CORNERS_ROUNDED](#TOP-CORNERS-ROUNDED) | Rectangle à coins arrondis du même côté. |
| [TOP_CORNERS_SNIPPED](#TOP-CORNERS-SNIPPED) | Rectangle à coins du même côté découpés. |
| [TRAPEZOID](#TRAPEZOID) | Trapèze. |
| [TRIANGLE](#TRIANGLE) | Triangle. |
| [UP_ARROW](#UP-ARROW) | Flèche vers le haut. |
| [UP_ARROW_CALLOUT](#UP-ARROW-CALLOUT) | Flèche d'annotation vers le haut. |
| [UP_DOWN_ARROW](#UP-DOWN-ARROW) | Flèche haut et bas. |
| [UP_DOWN_ARROW_CALLOUT](#UP-DOWN-ARROW-CALLOUT) | Flèche d'annotation haut et bas. |
| [UTURN_ARROW](#UTURN-ARROW) | Flèche en U. |
| [VERTICAL_SCROLL](#VERTICAL-SCROLL) | Défilement vertical. |
| [WAVE](#WAVE) | Vague. |
| [WEDGE_ELLIPSE_CALLOUT](#WEDGE-ELLIPSE-CALLOUT) | Coin d'annotation elliptique. |
| [WEDGE_PIE](#WEDGE-PIE) | Quart de tarte. |
| [WEDGE_RECT_CALLOUT](#WEDGE-RECT-CALLOUT) | Coin d'annotation rectangle. |
| [WEDGE_R_RECT_CALLOUT](#WEDGE-R-RECT-CALLOUT) | Coin d'annotation rectangle arrondi. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String chartShapeTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartShapeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartShapeType)](#toString-int) |  |
### ACCENT_BORDER_CALLOUT_1 {#ACCENT-BORDER-CALLOUT-1}
```
public static int ACCENT_BORDER_CALLOUT_1
```


Infobulle accentuée avec bordure 1.

### ACCENT_BORDER_CALLOUT_2 {#ACCENT-BORDER-CALLOUT-2}
```
public static int ACCENT_BORDER_CALLOUT_2
```


Infobulle accentuée avec bordure 2.

### ACCENT_BORDER_CALLOUT_3 {#ACCENT-BORDER-CALLOUT-3}
```
public static int ACCENT_BORDER_CALLOUT_3
```


Infobulle accentuée avec bordure 3.

### ACCENT_CALLOUT_1 {#ACCENT-CALLOUT-1}
```
public static int ACCENT_CALLOUT_1
```


Infobulle accentuée 1.

### ACCENT_CALLOUT_2 {#ACCENT-CALLOUT-2}
```
public static int ACCENT_CALLOUT_2
```


Infobulle accentuée 2.

### ACCENT_CALLOUT_3 {#ACCENT-CALLOUT-3}
```
public static int ACCENT_CALLOUT_3
```


Infobulle accentuée 3.

### ACTION_BUTTON_BACK_PREVIOUS {#ACTION-BUTTON-BACK-PREVIOUS}
```
public static int ACTION_BUTTON_BACK_PREVIOUS
```


Bouton Retour ou précédent.

### ACTION_BUTTON_BEGINNING {#ACTION-BUTTON-BEGINNING}
```
public static int ACTION_BUTTON_BEGINNING
```


Bouton Début.

### ACTION_BUTTON_BLANK {#ACTION-BUTTON-BLANK}
```
public static int ACTION_BUTTON_BLANK
```


Bouton Vide.

### ACTION_BUTTON_DOCUMENT {#ACTION-BUTTON-DOCUMENT}
```
public static int ACTION_BUTTON_DOCUMENT
```


Bouton Document.

### ACTION_BUTTON_END {#ACTION-BUTTON-END}
```
public static int ACTION_BUTTON_END
```


Bouton Fin.

### ACTION_BUTTON_FORWARD_NEXT {#ACTION-BUTTON-FORWARD-NEXT}
```
public static int ACTION_BUTTON_FORWARD_NEXT
```


Bouton Avancer ou suivant.

### ACTION_BUTTON_HELP {#ACTION-BUTTON-HELP}
```
public static int ACTION_BUTTON_HELP
```


Bouton Aide.

### ACTION_BUTTON_HOME {#ACTION-BUTTON-HOME}
```
public static int ACTION_BUTTON_HOME
```


Bouton Accueil.

### ACTION_BUTTON_INFORMATION {#ACTION-BUTTON-INFORMATION}
```
public static int ACTION_BUTTON_INFORMATION
```


Bouton Information.

### ACTION_BUTTON_MOVIE {#ACTION-BUTTON-MOVIE}
```
public static int ACTION_BUTTON_MOVIE
```


Bouton Film.

### ACTION_BUTTON_RETURN {#ACTION-BUTTON-RETURN}
```
public static int ACTION_BUTTON_RETURN
```


Bouton Retour.

### ACTION_BUTTON_SOUND {#ACTION-BUTTON-SOUND}
```
public static int ACTION_BUTTON_SOUND
```


Bouton Son.

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

### BENT_ARROW {#BENT-ARROW}
```
public static int BENT_ARROW
```


Flèche courbée.

### BENT_CONNECTOR_2 {#BENT-CONNECTOR-2}
```
public static int BENT_CONNECTOR_2
```


Connecteur courbé 2.

### BENT_CONNECTOR_3 {#BENT-CONNECTOR-3}
```
public static int BENT_CONNECTOR_3
```


Connecteur courbé 3.

### BENT_CONNECTOR_4 {#BENT-CONNECTOR-4}
```
public static int BENT_CONNECTOR_4
```


Connecteur courbé 4.

### BENT_CONNECTOR_5 {#BENT-CONNECTOR-5}
```
public static int BENT_CONNECTOR_5
```


Connecteur courbé 5.

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


Encadré avec bordure 1.

### BORDER_CALLOUT_2 {#BORDER-CALLOUT-2}
```
public static int BORDER_CALLOUT_2
```


Encadré avec bordure 2.

### BORDER_CALLOUT_3 {#BORDER-CALLOUT-3}
```
public static int BORDER_CALLOUT_3
```


Encadré avec bordure 3.

### BRACE_PAIR {#BRACE-PAIR}
```
public static int BRACE_PAIR
```


Paire d'accolades.

### BRACKET_PAIR {#BRACKET-PAIR}
```
public static int BRACKET_PAIR
```


Paire de crochets.

### CALLOUT_1 {#CALLOUT-1}
```
public static int CALLOUT_1
```


Encadré 1.

### CALLOUT_2 {#CALLOUT-2}
```
public static int CALLOUT_2
```


Encadré 2.

### CALLOUT_3 {#CALLOUT-3}
```
public static int CALLOUT_3
```


Encadré 3.

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

### CHART_STAR {#CHART-STAR}
```
public static int CHART_STAR
```


Graphique étoile.

### CHART_X {#CHART-X}
```
public static int CHART_X
```


Graphique X.

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

### CLOUD_CALLOUT {#CLOUD-CALLOUT}
```
public static int CLOUD_CALLOUT
```


Encadré nuage.

### CORNER {#CORNER}
```
public static int CORNER
```


Coin.

### CORNER_TABS {#CORNER-TABS}
```
public static int CORNER_TABS
```


Onglets d'angle.

### CUBE {#CUBE}
```
public static int CUBE
```


Cube.

### CURVED_CONNECTOR_2 {#CURVED-CONNECTOR-2}
```
public static int CURVED_CONNECTOR_2
```


Connecteur courbe 2.

### CURVED_CONNECTOR_3 {#CURVED-CONNECTOR-3}
```
public static int CURVED_CONNECTOR_3
```


Connecteur courbe 3.

### CURVED_CONNECTOR_4 {#CURVED-CONNECTOR-4}
```
public static int CURVED_CONNECTOR_4
```


Connecteur courbe 4.

### CURVED_CONNECTOR_5 {#CURVED-CONNECTOR-5}
```
public static int CURVED_CONNECTOR_5
```


Connecteur courbe 5.

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


Flèche courbée vers le haut.

### DECAGON {#DECAGON}
```
public static int DECAGON
```


Décagone.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Indique qu'aucune forme n'est définie pour l'élément du graphique.

### DIAGONAL_CORNERS_ROUNDED {#DIAGONAL-CORNERS-ROUNDED}
```
public static int DIAGONAL_CORNERS_ROUNDED
```


Rectangle à coins diagonaux arrondis.

### DIAGONAL_CORNERS_SNIPPED {#DIAGONAL-CORNERS-SNIPPED}
```
public static int DIAGONAL_CORNERS_SNIPPED
```


Rectangle à coins diagonaux découpés.

### DIAGONAL_STRIPE {#DIAGONAL-STRIPE}
```
public static int DIAGONAL_STRIPE
```


Bande diagonale.

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


Bulle flèche vers le bas.

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


Flux de processus alternatif.

### FLOW_CHART_COLLATE {#FLOW-CHART-COLLATE}
```
public static int FLOW_CHART_COLLATE
```


Flux de regroupement.

### FLOW_CHART_CONNECTOR {#FLOW-CHART-CONNECTOR}
```
public static int FLOW_CHART_CONNECTOR
```


Flux de connecteur.

### FLOW_CHART_DECISION {#FLOW-CHART-DECISION}
```
public static int FLOW_CHART_DECISION
```


Flux de décision.

### FLOW_CHART_DELAY {#FLOW-CHART-DELAY}
```
public static int FLOW_CHART_DELAY
```


Flux de délai.

### FLOW_CHART_DISPLAY {#FLOW-CHART-DISPLAY}
```
public static int FLOW_CHART_DISPLAY
```


Flux d'affichage.

### FLOW_CHART_DOCUMENT {#FLOW-CHART-DOCUMENT}
```
public static int FLOW_CHART_DOCUMENT
```


Flux de document.

### FLOW_CHART_EXTRACT {#FLOW-CHART-EXTRACT}
```
public static int FLOW_CHART_EXTRACT
```


Flux d'extraction.

### FLOW_CHART_INPUT_OUTPUT {#FLOW-CHART-INPUT-OUTPUT}
```
public static int FLOW_CHART_INPUT_OUTPUT
```


Flux d'entrée/sortie.

### FLOW_CHART_INTERNAL_STORAGE {#FLOW-CHART-INTERNAL-STORAGE}
```
public static int FLOW_CHART_INTERNAL_STORAGE
```


Flux de stockage interne.

### FLOW_CHART_MAGNETIC_DISK {#FLOW-CHART-MAGNETIC-DISK}
```
public static int FLOW_CHART_MAGNETIC_DISK
```


Flux de disque magnétique.

### FLOW_CHART_MAGNETIC_DRUM {#FLOW-CHART-MAGNETIC-DRUM}
```
public static int FLOW_CHART_MAGNETIC_DRUM
```


Flux de tambour magnétique.

### FLOW_CHART_MAGNETIC_TAPE {#FLOW-CHART-MAGNETIC-TAPE}
```
public static int FLOW_CHART_MAGNETIC_TAPE
```


Flux de bande magnétique.

### FLOW_CHART_MANUAL_INPUT {#FLOW-CHART-MANUAL-INPUT}
```
public static int FLOW_CHART_MANUAL_INPUT
```


Flux d'entrée manuelle.

### FLOW_CHART_MANUAL_OPERATION {#FLOW-CHART-MANUAL-OPERATION}
```
public static int FLOW_CHART_MANUAL_OPERATION
```


Flux d'opération manuelle.

### FLOW_CHART_MERGE {#FLOW-CHART-MERGE}
```
public static int FLOW_CHART_MERGE
```


Flux de fusion.

### FLOW_CHART_MULTIDOCUMENT {#FLOW-CHART-MULTIDOCUMENT}
```
public static int FLOW_CHART_MULTIDOCUMENT
```


Flux multi-documents.

### FLOW_CHART_OFFLINE_STORAGE {#FLOW-CHART-OFFLINE-STORAGE}
```
public static int FLOW_CHART_OFFLINE_STORAGE
```


Flux de stockage hors ligne.

### FLOW_CHART_OFFPAGE_CONNECTOR {#FLOW-CHART-OFFPAGE-CONNECTOR}
```
public static int FLOW_CHART_OFFPAGE_CONNECTOR
```


Flux de connecteur hors page.

### FLOW_CHART_ONLINE_STORAGE {#FLOW-CHART-ONLINE-STORAGE}
```
public static int FLOW_CHART_ONLINE_STORAGE
```


Flux de stockage en ligne.

### FLOW_CHART_OR {#FLOW-CHART-OR}
```
public static int FLOW_CHART_OR
```


Flux OU.

### FLOW_CHART_PREDEFINED_PROCESS {#FLOW-CHART-PREDEFINED-PROCESS}
```
public static int FLOW_CHART_PREDEFINED_PROCESS
```


Flux de processus prédéfini.

### FLOW_CHART_PREPARATION {#FLOW-CHART-PREPARATION}
```
public static int FLOW_CHART_PREPARATION
```


Flux de préparation.

### FLOW_CHART_PROCESS {#FLOW-CHART-PROCESS}
```
public static int FLOW_CHART_PROCESS
```


Flux de processus.

### FLOW_CHART_PUNCHED_CARD {#FLOW-CHART-PUNCHED-CARD}
```
public static int FLOW_CHART_PUNCHED_CARD
```


Flux de carte perforée.

### FLOW_CHART_PUNCHED_TAPE {#FLOW-CHART-PUNCHED-TAPE}
```
public static int FLOW_CHART_PUNCHED_TAPE
```


Flux de ruban perforé.

### FLOW_CHART_SORT {#FLOW-CHART-SORT}
```
public static int FLOW_CHART_SORT
```


Flux de tri.

### FLOW_CHART_SUMMING_JUNCTION {#FLOW-CHART-SUMMING-JUNCTION}
```
public static int FLOW_CHART_SUMMING_JUNCTION
```


Flux de jonction de sommation.

### FLOW_CHART_TERMINATOR {#FLOW-CHART-TERMINATOR}
```
public static int FLOW_CHART_TERMINATOR
```


Flux de terminaison.

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

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Entonnoir.

### GEAR_6 {#GEAR-6}
```
public static int GEAR_6
```


Engrenage à six dents.

### GEAR_9 {#GEAR-9}
```
public static int GEAR_9
```


Engrenage à neuf dents.

### HALF_FRAME {#HALF-FRAME}
```
public static int HALF_FRAME
```


Demi-cadre.

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

### INVERSE_LINE {#INVERSE-LINE}
```
public static int INVERSE_LINE
```


Ligne inverse.

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


Annotation flèche gauche.

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

### LEFT_RIGHT_ARROW {#LEFT-RIGHT-ARROW}
```
public static int LEFT_RIGHT_ARROW
```


Flèche gauche et droite.

### LEFT_RIGHT_ARROW_CALLOUT {#LEFT-RIGHT-ARROW-CALLOUT}
```
public static int LEFT_RIGHT_ARROW_CALLOUT
```


Annotation flèche gauche et droite.

### LEFT_RIGHT_CIRCULAR_ARROW {#LEFT-RIGHT-CIRCULAR-ARROW}
```
public static int LEFT_RIGHT_CIRCULAR_ARROW
```


Flèche circulaire gauche‑droite.

### LEFT_RIGHT_RIBBON {#LEFT-RIGHT-RIBBON}
```
public static int LEFT_RIGHT_RIBBON
```


Ruban gauche‑droite.

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

### MATH_EQUAL {#MATH-EQUAL}
```
public static int MATH_EQUAL
```


Égalité mathématique.

### MATH_MINUS {#MATH-MINUS}
```
public static int MATH_MINUS
```


Soustraction mathématique.

### MATH_MULTIPLY {#MATH-MULTIPLY}
```
public static int MATH_MULTIPLY
```


Multiplication mathématique.

### MATH_NOT_EQUAL {#MATH-NOT-EQUAL}
```
public static int MATH_NOT_EQUAL
```


Inégalité mathématique.

### MATH_PLUS {#MATH-PLUS}
```
public static int MATH_PLUS
```


Addition mathématique.

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

### NOTCHED_RIGHT_ARROW {#NOTCHED-RIGHT-ARROW}
```
public static int NOTCHED_RIGHT_ARROW
```


Flèche droite à encoches.

### NO_SMOKING {#NO-SMOKING}
```
public static int NO_SMOKING
```


Interdiction de fumer.

### OCTAGON {#OCTAGON}
```
public static int OCTAGON
```


Octogone.

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


Flèche quadruple d'appel.

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


Bulle flèche droite.

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

### SEAL_10 {#SEAL-10}
```
public static int SEAL_10
```


Étoile à dix pointes.

### SEAL_12 {#SEAL-12}
```
public static int SEAL_12
```


Étoile à douze pointes.

### SEAL_16 {#SEAL-16}
```
public static int SEAL_16
```


Étoile à seize pointes.

### SEAL_24 {#SEAL-24}
```
public static int SEAL_24
```


Étoile à vingt-quatre pointes.

### SEAL_32 {#SEAL-32}
```
public static int SEAL_32
```


Étoile à trente-deux pointes.

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

### SEAL_7 {#SEAL-7}
```
public static int SEAL_7
```


Étoile à sept pointes.

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

### SINGLE_CORNER_SNIPPED {#SINGLE-CORNER-SNIPPED}
```
public static int SINGLE_CORNER_SNIPPED
```


Objet rectangle à coin unique découpé.

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

### STAR {#STAR}
```
public static int STAR
```


Étoile.

### STRAIGHT_CONNECTOR_1 {#STRAIGHT-CONNECTOR-1}
```
public static int STRAIGHT_CONNECTOR_1
```


Connecteur droit 1.

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

### TEARDROP {#TEARDROP}
```
public static int TEARDROP
```


Goutte.

### TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED {#TOP-CORNERS-ONE-ROUNDED-ONE-SNIPPED}
```
public static int TOP_CORNERS_ONE_ROUNDED_ONE_SNIPPED
```


Rectangle à un seul coin découpé et arrondi.

### TOP_CORNERS_ROUNDED {#TOP-CORNERS-ROUNDED}
```
public static int TOP_CORNERS_ROUNDED
```


Rectangle à coins arrondis du même côté.

### TOP_CORNERS_SNIPPED {#TOP-CORNERS-SNIPPED}
```
public static int TOP_CORNERS_SNIPPED
```


Rectangle à coins du même côté découpés.

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


Flèche d'annotation vers le haut.

### UP_DOWN_ARROW {#UP-DOWN-ARROW}
```
public static int UP_DOWN_ARROW
```


Flèche haut et bas.

### UP_DOWN_ARROW_CALLOUT {#UP-DOWN-ARROW-CALLOUT}
```
public static int UP_DOWN_ARROW_CALLOUT
```


Flèche d'annotation haut et bas.

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


Coin d'annotation elliptique.

### WEDGE_PIE {#WEDGE-PIE}
```
public static int WEDGE_PIE
```


Quart de tarte.

### WEDGE_RECT_CALLOUT {#WEDGE-RECT-CALLOUT}
```
public static int WEDGE_RECT_CALLOUT
```


Coin d'annotation rectangle.

### WEDGE_R_RECT_CALLOUT {#WEDGE-R-RECT-CALLOUT}
```
public static int WEDGE_R_RECT_CALLOUT
```


Coin d'annotation rectangle arrondi.

### length {#length}
```
public static int length
```


### fromName(String chartShapeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartShapeTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartShapeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartShapeType) {#getName-int}
```
public static String getName(int chartShapeType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| chartShapeType | int |  |

**Returns:**
java.lang.String
