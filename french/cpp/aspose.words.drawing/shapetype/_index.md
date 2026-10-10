---
title: "Aspose::Words::Drawing::ShapeType enum"
linktitle: "ShapeType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeType enum. Spécifie le type de forme dans un document Microsoft Word en C++."
type: docs
weight: 38000
url: /fr/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


Spécifie le type de forme dans un document Microsoft Word.

```cpp
enum class ShapeType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Image | 75 | La forme est une image. |
| ZoneDeTexte | 202 | La forme est une zone de texte. Notez que les formes de nombreux autres types peuvent également contenir du texte à l'intérieur. Une forme n'a pas besoin d'être de ce type pour contenir du texte. |
| Group | -1 | La forme est un groupe de formes. |
| OleObject | -2 | La forme est un objet OLE. Vous ne pouvez pas créer de formes de ce type dans le document. |
| OleControl | 201 | La forme est un contrôle ActiveX. Vous ne pouvez pas créer de formes de ce type dans le document. |
| NonPrimitive | 0 | Une forme dessinée par l'utilisateur et composée de plusieurs segments et/ou sommets (courbe, forme libre ou griffonnage). Vous ne pouvez pas créer de formes de ce type dans le document. |
| Rectangle | 1 | Rectangle. |
| RoundRectangle | 2 | Rectangle arrondi. |
| Ellipse | 3 | Ellipse. |
| Diamond | 4 | Losange. |
| Triangle | 5 | Triangle. |
| RightTriangle | 6 | Triangle rectangle. |
| Parallelogram | 7 | Parallélogramme. |
| Trapezoid | 8 | Trapèze. |
| Hexagon | 9 | Hexagone. |
| Octagon | 10 | Octogone. |
| Plus | 11 | Plus. |
| Étoile | 12 | Étoile. |
| Flèche | 13 | Flèche. |
| FlècheÉpaisse | 14 | Flèche épaisse. |
| PlaqueAccueil | 15 | Plaque d'accueil. |
| Cube | 16 | Cube. |
| Ballon | 17 | Ballon. |
| Sceau | 18 | Sceau. |
| Arc | 19 | Arc. |
| Ligne | 20 | Ligne. |
| Plaque | 21 | Plaque. |
| Boîte | 22 | Boîte. |
| Beignet | 23 | Beignet. |
| TextSimple | 24 | Texte simple. |
| TextOctagon | 25 | Texte octogone. |
| TextHexagon | 26 | Texte hexagone. |
| TextCurve | 27 | Texte courbe. |
| TextWave | 28 | Texte vague. |
| TextRing | 29 | Texte anneau. |
| TextOnCurve | 30 | Texte sur courbe. |
| TextOnRing | 31 | Texte sur anneau. |
| StraightConnector1 | 32 | Une forme de connecteur droit. |
| BentConnector2 | 33 | Une forme de connecteur coudé avec deux segments. |
| BentConnector3 | 34 | Une forme de connecteur coudé avec trois segments. |
| BentConnector4 | 35 | Une forme de connecteur coudé avec quatre segments. |
| BentConnector5 | 36 | Une forme de connecteur coudé avec cinq segments. |
| CurvedConnector2 | 37 | Une forme de connecteur courbé avec deux segments. |
| CurvedConnector3 | 38 | Une forme de connecteur courbé avec trois segments. |
| CurvedConnector4 | 39 | Une forme de connecteur courbé avec quatre segments. |
| CurvedConnector5 | 40 | Une forme de connecteur courbé avec cinq segments. |
| Callout1 | 41 | Une forme d'annotation avec une flèche. |
| Callout2 | 42 | Une forme d'annotation avec deux flèches. |
| Callout3 | 43 | Une forme d'annotation avec trois flèches. |
| AccentCallout1 | 44 | Une forme d'annotation accentuée avec une flèche. |
| AccentCallout2 | 45 | Une forme d'annotation accentuée avec deux flèches. |
| AccentCallout3 | 46 | Une forme d'annotation accentuée avec trois flèches. |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) annotation 1. |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) annotation 2. |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) annotation 3. |
| AccentBorderCallout1 | 50 | Appel de bordure accentuée 1. |
| AccentBorderCallout2 | 51 | Appel de bordure accentuée 2. |
| AccentBorderCallout3 | 52 | Appel de bordure accentuée 3. |
| Ruban | 53 | Ruban. |
| Ribbon2 | 54 | Ruban 2. |
| Chevron | 55 | Chevron. |
| Pentagone | 56 | Pentagone. |
| NoSmoking | 57 | Interdiction de fumer. |
| Seal8 | 58 | Étoile à huit pointes. |
| Seal16 | 59 | Étoile à 16 pointes. |
| Seal32 | 60 | Étoile à 32 pointes. |
| WedgeRectCallout | 61 | Appel de coin rectangulaire. |
| WedgeRRectCallout | 62 | Coin R rect annotation. |
| WedgeEllipseCallout | 63 | Coin ellipse annotation. |
| Wave | 64 | Vague. |
| FoldedCorner | 65 | Coin plié. |
| LeftArrow | 66 | Flèche gauche. |
| DownArrow | 67 | Flèche bas. |
| UpArrow | 68 | Flèche haut. |
| LeftRightArrow | 69 | Flèche gauche droite. |
| UpDownArrow | 70 | Flèche haut bas. |
| IrregularSeal1 | 71 | Sceau irrégulier 1. |
| IrregularSeal2 | 72 | Sceau irrégulier 2. |
| LightningBolt | 73 | Éclair. |
| Heart | 74 | Cœur. |
| QuadArrow | 76 | Flèche quadruple. |
| LeftArrowCallout | 77 | Appel de flèche gauche. |
| RightArrowCallout | 78 | Appel de flèche droite. |
| UpArrowCallout | 79 | Appel de flèche haut. |
| DownArrowCallout | 80 | Appel de flèche bas. |
| LeftRightArrowCallout | 81 | Appel de flèche gauche droite. |
| UpDownArrowCallout | 82 | Appel de flèche haut bas. |
| QuadArrowCallout | 83 | Appel de flèche quadruple. |
| Biseau | 84 | Biseau. |
| LeftBracket | 85 | Crochet gauche. |
| RightBracket | 86 | Crochet droit. |
| LeftBrace | 87 | Accolade gauche. |
| RightBrace | 88 | Accolade droite. |
| LeftUpArrow | 89 | Flèche vers la gauche et vers le haut. |
| BentUpArrow | 90 | Flèche courbée vers le haut. |
| BentArrow | 91 | Flèche courbée. |
| Seal24 | 92 | Étoile à 24 pointes. |
| StripedRightArrow | 93 | Flèche droite à bandes. |
| NotchedRightArrow | 94 | Flèche droite à encoches. |
| BlockArc | 95 | Arc en bloc. |
| SmileyFace | 96 | Visage souriant. |
| VerticalScroll | 97 | Défilement vertical. |
| HorizontalScroll | 98 | Défilement horizontal. |
| CircularArrow | 99 | Flèche circulaire. |
| CustomShape | 100 | Ce type de forme semble être destiné aux formes qui ne font pas partie de l'ensemble standard des formes automatiques dans Microsoft Word. Par exemple, si vous insérez une nouvelle forme automatique à partir de ClipArt. Vous ne pouvez pas créer de formes de ce type dans le document. |
| UturnArrow | 101 | Flèche en U. |
| CurvedRightArrow | 102 | Flèche courbée vers la droite. |
| CurvedLeftArrow | 103 | Flèche courbée vers la gauche. |
| CurvedUpArrow | 104 | Flèche courbée vers le haut. |
| CurvedDownArrow | 105 | Flèche courbée vers le bas. |
| CloudCallout | 106 | Annotation nuage. |
| EllipseRibbon | 107 | Ruban ellipse. |
| EllipseRibbon2 | 108 | Ruban ellipse 2. |
| FlowChartProcess | 109 | Processus de diagramme de flux. |
| FlowChartDecision | 110 | Décision de diagramme de flux. |
| FlowChartInputOutput | 111 | Entrée/sortie du diagramme de flux. |
| FlowChartPredefinedProcess | 112 | Processus prédéfini de diagramme de flux. |
| FlowChartInternalStorage | 113 | Stockage interne du diagramme de flux. |
| FlowChartDocument | 114 | Document de diagramme de flux. |
| FlowChartMultidocument | 115 | Document multi de diagramme de flux. |
| FlowChartTerminator | 116 | Terminaison du diagramme de flux. |
| FlowChartPreparation | 117 | Préparation du diagramme de flux. |
| FlowChartManualInput | 118 | Entrée manuelle du diagramme de flux. |
| FlowChartManualOperation | 119 | Opération manuelle du diagramme de flux. |
| FlowChartConnector | 120 | Connecteur du diagramme de flux. |
| FlowChartPunchedCard | 121 | Carte perforée du diagramme de flux. |
| FlowChartPunchedTape | 122 | Ruban perforé du diagramme de flux. |
| FlowChartSummingJunction | 123 | Jonction de sommation du diagramme de flux. |
| FlowChartOr | 124 | Ou du diagramme de flux. |
| FlowChartCollate | 125 | Collation du diagramme de flux. |
| FlowChartSort | 126 | Tri du diagramme de flux. |
| FlowChartExtract | 127 | Extraction du diagramme de flux. |
| FlowChartMerge | 128 | Fusion du diagramme de flux. |
| FlowChartOfflineStorage | 129 | Stockage hors ligne du diagramme de flux. |
| FlowChartOnlineStorage | 130 | Stockage en ligne du diagramme de flux. |
| FlowChartMagneticTape | 131 | Bande magnétique du diagramme de flux. |
| FlowChartMagneticDisk | 132 | Disque magnétique du diagramme de flux. |
| FlowChartMagneticDrum | 133 | Tambour magnétique du diagramme de flux. |
| FlowChartDisplay | 134 | Affichage du diagramme de flux. |
| FlowChartDelay | 135 | Délai du diagramme de flux. |
| TextPlainText | 136 | Texte brut, objet WordArt. |
| TextStop | 137 | Arrêt, objet WordArt. |
| TextTriangle | 138 | Triangle, objet WordArt. |
| TextTriangleInverted | 139 | Triangle inversé, objet WordArt. |
| TextChevron | 140 | Chevron, objet WordArt. |
| TextChevronInverted | 141 | Chevron inversé, objet WordArt. |
| TextRingInside | 142 | Anneau à l'intérieur, objet WordArt. |
| TextRingOutside | 143 | Anneau à l'extérieur, objet WordArt. |
| TextArchUpCurve | 144 | Arc vers le haut, objet WordArt. |
| TextArchDownCurve | 145 | Arc vers le bas, objet WordArt. |
| TextCircleCurve | 146 | Courbe circulaire, objet WordArt. |
| TextButtonCurve | 147 | Courbe de bouton, objet WordArt. |
| TextArchUpPour | 148 | Arc vers le haut, objet WordArt. |
| TextArchDownPour | 149 | Arc vers le bas, objet WordArt. |
| TextCirclePour | 150 | Cercle déversé, objet WordArt. |
| TextButtonPour | 151 | Bouton pour, objet WordArt. |
| TextCurveUp | 152 | Courbe vers le haut, objet WordArt. |
| TextCurveDown | 153 | Courbe vers le bas, objet WordArt. |
| TextCascadeUp | 154 | Cascade vers le haut, objet WordArt. |
| TextCascadeDown | 155 | Cascade vers le bas, objet WordArt. |
| TextWave1 | 156 | Vague 1, objet WordArt. |
| TextWave2 | 157 | Vague 2, objet WordArt. |
| TextWave3 | 158 | Vague 3, objet WordArt. |
| TextWave4 | 159 | Vague 4, objet WordArt. |
| TextInflate | 160 | Gonfler, objet WordArt. |
| TextDeflate | 161 | Dégonfler, objet WordArt. |
| TextInflateBottom | 162 | Gonfler en bas, objet WordArt. |
| TextDeflateBottom | 163 | Réduire le bas, objet WordArt. |
| TextInflateTop | 164 | Gonfler le haut, objet WordArt. |
| TextDeflateTop | 165 | Réduire le haut, objet WordArt. |
| TextDeflateInflate | 166 | Réduire gonfler, objet WordArt. |
| TextDeflateInflateDeflate | 167 | Réduire gonfler réduire, objet WordArt. |
| TextFadeRight | 168 | Fondu à droite, objet WordArt. |
| TextFadeLeft | 169 | Fondu à gauche, objet WordArt. |
| TextFadeUp | 170 | Fondu vers le haut, objet WordArt. |
| TextFadeDown | 171 | Fondu vers le bas, objet WordArt. |
| TextSlantUp | 172 | Incliner vers le haut, objet WordArt. |
| TextSlantDown | 173 | Incliner vers le bas, objet WordArt. |
| TextCanUp | 174 | Can haut, objet WordArt. |
| TextCanDown | 175 | Can bas, objet WordArt. |
| FlowChartAlternateProcess | 176 | Processus alternatif de diagramme de flux. |
| FlowChartOffpageConnector | 177 | Connecteur de diagramme de flux hors page. |
| Callout90 | 178 | Encadré 90. |
| AccentCallout90 | 179 | Encadré accentué 90. |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) encadré 90. |
| AccentBorderCallout90 | 181 | Encadré de bordure accentué 90. |
| LeftRightUpArrow | 182 | Flèche gauche droite haut. |
| Sun | 183 | Soleil. |
| Moon | 184 | Lune. |
| BracketPair | 185 | Paire de crochets. |
| BracePair | 186 | Paire d'accolades. |
| Seal4 | 187 | Étoile à quatre pointes. |
| DoubleWave | 188 | Double vague. |
| ActionButtonBlank | 189 | Bouton d'action vide. |
| ActionButtonHome | 190 | Bouton d'action accueil. |
| ActionButtonHelp | 191 | Bouton d'action aide. |
| ActionButtonInformation | 192 | Bouton d'action informations. |
| ActionButtonForwardNext | 193 | Bouton d'action suivant. |
| ActionButtonBackPrevious | 194 | Bouton d'action retour précédent. |
| ActionButtonEnd | 195 | Bouton d'action fin. |
| ActionButtonBeginning | 196 | Bouton d'action début. |
| ActionButtonReturn | 197 | Bouton d'action retour. |
| ActionButtonDocument | 198 | Bouton d'action document. |
| ActionButtonSound | 199 | Bouton d'action son. |
| ActionButtonMovie | 200 | Bouton d'action film. |
| SingleCornerSnipped | 203 | Rogner l'objet rectangle à coin unique. |
| CoinsSupérieursDécoupés | 204 | Découper le rectangle à coins du même côté. |
| CoinsDiagonauxDécoupés | 205 | Découper le rectangle à coins diagonaux. |
| CoinsSupérieursUnArrondiUnDécoupé | 206 | Découper et arrondir le rectangle à coin unique. |
| CoinUniqueArrondi | 207 | Arrondir le rectangle à coin unique. |
| CoinsSupérieursArrondis | 208 | Arrondir le rectangle à coins du même côté. |
| CoinsDiagonauxArrondis | 209 | Arrondir le rectangle à coins diagonaux. |
| Heptagone | 210 | Heptagone. |
| Nuage | 211 | Nuage. |
| Sceau6 | 212 | Étoile à six branches. |
| Sceau7 | 213 | Étoile à sept branches. |
| Sceau10 | 214 | Étoile à dix branches. |
| Sceau12 | 215 | Étoile à douze branches. |
| FlècheSwoosh | 216 | Flèche en forme de swoosh. |
| Goutte | 217 | Goutte. |
| Onglets carrés | 218 | Onglets carrés. |
| Onglets plaque | 219 | Onglets plaque. |
| Camembert | 220 | Camembert. |
| Camembert secteur | 221 | Camembert secteur. |
| Ligne inversée | 222 | Ligne inversée. |
| MathPlus | 223 | [Math](../../aspose.words.math/) plus. |
| MathMinus | 224 | [Math](../../aspose.words.math/) moins. |
| MathMultiply | 225 | [Math](../../aspose.words.math/) multiplier. |
| MathDivide | 226 | [Math](../../aspose.words.math/) diviser. |
| MathEqual | 227 | [Math](../../aspose.words.math/) égal. |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) pas égal. |
| Trapèze non isocèle | 229 | Trapèze non isocèle. |
| Flèche circulaire gauche-droite | 230 | Flèche circulaire gauche-droite. |
| Ruban gauche-droite | 231 | Ruban gauche-droite. |
| LeftCircularArrow | 232 | Flèche circulaire gauche. |
| Frame | 233 | Cadre. |
| HalfFrame | 234 | Demi-cadre. |
| Funnel | 235 | Entonnoir. |
| Gear6 | 236 | Engrenage à six dents. |
| Gear9 | 237 | Engrenage à neuf dents. |
| Decagon | 238 | Décagone. |
| Dodecagon | 239 | Dodécagone. |
| DiagonalStripe | 240 | Bande diagonale. |
| Corner | 241 | Coin. |
| CornerTabs | 242 | Onglets d'angle. |
| Chord | 243 | Corde. |
| ChartPlus | 244 | Graphique plus. |
| ChartStar | 245 | Graphique étoile. |
| ChartX | 246 | Graphique X. |
| MinValue | n/a | Réservé à l'usage du système. |


## Exemples



Montre comment insérer une forme avec une image depuis le système de fichiers local dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Le constructeur public de la classe "Shape" créera une forme avec le type de balisage "ShapeMarkupLanguage.Vml".
// Si vous devez créer une forme d'un type non primitif, tel que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, ou DiagonalCornersRounded,
// veuillez utiliser DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Montre comment Aspose.Words identifie les formes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// Pour identifier correctement les types de formes, vous devez travailler avec les formes en tant que DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// "Strict" ou "Transitional" conformité permet d'enregistrer la forme en tant que DML.
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
