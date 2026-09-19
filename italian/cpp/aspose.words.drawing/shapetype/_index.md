---
title: "Aspose::Words::Drawing::ShapeType enum"
linktitle: "ShapeType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeType enum. Specifica il tipo di forma in un documento Microsoft Word in C++."
type: docs
weight: 38000
url: /it/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


Specifica il tipo di forma in un documento Microsoft Word.

```cpp
enum class ShapeType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Immagine | 75 | La forma è un'immagine. |
| CasellaDiTesto | 202 | La forma è una casella di testo. Nota che le forme di molti altri tipi possono anche contenere testo al loro interno. Una forma non deve avere questo tipo per contenere testo. |
| Group | -1 | La forma è una forma di gruppo. |
| OleObject | -2 | La forma è un oggetto OLE. Non è possibile creare forme di questo tipo nel documento. |
| OleControl | 201 | La forma è un controllo ActiveX. Non è possibile creare forme di questo tipo nel documento. |
| NonPrimitive | 0 | Una forma disegnata dall'utente e composta da più segmenti e/o vertici (curva, forma libera o scarabocchio). Non è possibile creare forme di questo tipo nel documento. |
| Rectangle | 1 | Rettangolo. |
| RoundRectangle | 2 | Rettangolo arrotondato. |
| Ellipse | 3 | Ellisse. |
| Diamond | 4 | Diamante. |
| Triangle | 5 | Triangolo. |
| RightTriangle | 6 | Triangolo rettangolo. |
| Parallelogram | 7 | Parallelogramma. |
| Trapezoid | 8 | Trapezio. |
| Hexagon | 9 | Esagono. |
| Octagon | 10 | Ottagono. |
| Più | 11 | Più. |
| Stella | 12 | Stella. |
| Freccia | 13 | Freccia. |
| FrecciaSpessa | 14 | Freccia spessa. |
| CasaBase | 15 | Casa base. |
| Cubo | 16 | Cubo. |
| Palloncino | 17 | Palloncino. |
| Sigillo | 18 | Sigillo. |
| Arco | 19 | Arco. |
| Linea | 20 | Linea. |
| Targa | 21 | Targa. |
| Lattina | 22 | Lattina. |
| Ciambella | 23 | Ciambella. |
| TextSimple | 24 | Testo semplice. |
| TextOctagon | 25 | Testo ottagono. |
| TextHexagon | 26 | Testo esagono. |
| TextCurve | 27 | Testo curva. |
| TextWave | 28 | Testo onda. |
| TextRing | 29 | Testo anello. |
| TextOnCurve | 30 | Testo su curva. |
| TextOnRing | 31 | Testo su anello. |
| StraightConnector1 | 32 | Una forma di connettore dritto. |
| BentConnector2 | 33 | Una forma di connettore curvo con due segmenti. |
| BentConnector3 | 34 | Una forma di connettore curvo con tre segmenti. |
| BentConnector4 | 35 | Una forma di connettore curvo con quattro segmenti. |
| BentConnector5 | 36 | Una forma di connettore piegato con cinque segmenti. |
| CurvedConnector2 | 37 | Una forma di connettore curvo con due segmenti. |
| CurvedConnector3 | 38 | Una forma di connettore curvo con tre segmenti. |
| CurvedConnector4 | 39 | Una forma di connettore curvo con quattro segmenti. |
| CurvedConnector5 | 40 | Una forma di connettore curvo con cinque segmenti. |
| Callout1 | 41 | Una forma di callout con una freccia. |
| Callout2 | 42 | Una forma di callout con due frecce. |
| Callout3 | 43 | Una forma di callout con tre frecce. |
| AccentCallout1 | 44 | Una forma di accent callout con una freccia. |
| AccentCallout2 | 45 | Una forma di accent callout con due frecce. |
| AccentCallout3 | 46 | Una forma di accent callout con tre frecce. |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) callout 1. |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) callout 2. |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) callout 3. |
| AccentBorderCallout1 | 50 | Richiamo bordo accentato 1. |
| AccentBorderCallout2 | 51 | Richiamo bordo accentato 2. |
| AccentBorderCallout3 | 52 | Richiamo bordo accentato 3. |
| Nastro | 53 | Nastro. |
| Ribbon2 | 54 | Nastro 2. |
| Chevron | 55 | Chevron. |
| Pentagono | 56 | Pentagono. |
| Divieto di fumo | 57 | Divieto di fumo. |
| Seal8 | 58 | Stella a otto punte. |
| Seal16 | 59 | Stella a 16 punte. |
| Seal32 | 60 | Stella a 32 punte. |
| WedgeRectCallout | 61 | Richiamo a cuneo rettangolare. |
| WedgeRRectCallout | 62 | Richiamo rettangolare a cuneo R. |
| WedgeEllipseCallout | 63 | Richiamo ellittico a cuneo. |
| Wave | 64 | Onda. |
| FoldedCorner | 65 | Angolo piegato. |
| LeftArrow | 66 | Freccia sinistra. |
| DownArrow | 67 | Freccia giù. |
| UpArrow | 68 | Freccia su. |
| LeftRightArrow | 69 | Freccia sinistra destra. |
| UpDownArrow | 70 | Freccia su giù. |
| IrregularSeal1 | 71 | Sigillo irregolare 1. |
| IrregularSeal2 | 72 | Sigillo irregolare 2. |
| LightningBolt | 73 | Fulmine. |
| Heart | 74 | Cuore. |
| QuadArrow | 76 | Freccia quadrata. |
| LeftArrowCallout | 77 | Freccia di richiamo sinistra. |
| RightArrowCallout | 78 | Freccia di richiamo destra. |
| UpArrowCallout | 79 | Freccia di richiamo verso l'alto. |
| DownArrowCallout | 80 | Freccia di richiamo verso il basso. |
| LeftRightArrowCallout | 81 | Freccia di richiamo sinistra-destra. |
| UpDownArrowCallout | 82 | Freccia di richiamo su-giù. |
| QuadArrowCallout | 83 | Freccia di richiamo quadrata. |
| Smusso | 84 | Smusso. |
| LeftBracket | 85 | Parentesi quadra sinistra. |
| RightBracket | 86 | Parentesi quadra destra. |
| LeftBrace | 87 | Graffa sinistra. |
| RightBrace | 88 | Graffa destra. |
| LeftUpArrow | 89 | Freccia verso sinistra. |
| BentUpArrow | 90 | Freccia piegata verso l'alto. |
| BentArrow | 91 | Freccia piegata. |
| Seal24 | 92 | Stella a 24 punte. |
| StripedRightArrow | 93 | Freccia a strisce verso destra. |
| NotchedRightArrow | 94 | Freccia dentata verso destra. |
| BlockArc | 95 | Arco a blocco. |
| SmileyFace | 96 | Faccina sorridente. |
| VerticalScroll | 97 | Scorrimento verticale. |
| HorizontalScroll | 98 | Scorrimento orizzontale. |
| CircularArrow | 99 | Freccia circolare. |
| CustomShape | 100 | Questo tipo di forma sembra essere destinato a forme che non fanno parte del set standard di forme automatiche in Microsoft Word. Ad esempio, se inserisci una nuova forma automatica da ClipArt. Non è possibile creare forme di questo tipo nel documento. |
| UturnArrow | 101 | Freccia a U. |
| CurvedRightArrow | 102 | Freccia curva verso destra. |
| CurvedLeftArrow | 103 | Freccia curva verso sinistra. |
| CurvedUpArrow | 104 | Freccia curva verso l'alto. |
| CurvedDownArrow | 105 | Freccia curva verso il basso. |
| CloudCallout | 106 | Didascalia nuvola. |
| EllipseRibbon | 107 | Nastro ellittico. |
| EllipseRibbon2 | 108 | Nastro ellittico 2. |
| FlowChartProcess | 109 | Processo di diagramma di flusso. |
| FlowChartDecision | 110 | Decisione di diagramma di flusso. |
| FlowChartInputOutput | 111 | Ingresso/uscita di diagramma di flusso. |
| FlowChartPredefinedProcess | 112 | Processo predefinito di diagramma di flusso. |
| FlowChartInternalStorage | 113 | Archiviazione interna del diagramma di flusso. |
| FlowChartDocument | 114 | Documento di diagramma di flusso. |
| FlowChartMultidocument | 115 | Documento multi di diagramma di flusso. |
| FlowChartTerminator | 116 | Terminatore di diagramma di flusso. |
| FlowChartPreparation | 117 | Preparazione di diagramma di flusso. |
| FlowChartManualInput | 118 | Input manuale di diagramma di flusso. |
| FlowChartManualOperation | 119 | Operazione manuale di diagramma di flusso. |
| FlowChartConnector | 120 | Connettore di diagramma di flusso. |
| FlowChartPunchedCard | 121 | Scheda perforata di diagramma di flusso. |
| FlowChartPunchedTape | 122 | Nastro perforato di diagramma di flusso. |
| FlowChartSummingJunction | 123 | Giunzione di somma di diagramma di flusso. |
| FlowChartOr | 124 | Diagramma di flusso o. |
| FlowChartCollate | 125 | Collazione di diagramma di flusso. |
| FlowChartSort | 126 | Ordinamento diagramma di flusso. |
| FlowChartExtract | 127 | Estrazione diagramma di flusso. |
| FlowChartMerge | 128 | Unione diagramma di flusso. |
| FlowChartOfflineStorage | 129 | Archiviazione diagramma di flusso offline. |
| FlowChartOnlineStorage | 130 | Archiviazione diagramma di flusso online. |
| FlowChartMagneticTape | 131 | Nastro magnetico del diagramma di flusso. |
| FlowChartMagneticDisk | 132 | Disco magnetico del diagramma di flusso. |
| FlowChartMagneticDrum | 133 | Tamburo magnetico del diagramma di flusso. |
| FlowChartDisplay | 134 | Visualizzazione diagramma di flusso. |
| FlowChartDelay | 135 | Ritardo diagramma di flusso. |
| TextPlainText | 136 | Testo semplice, oggetto WordArt. |
| TextStop | 137 | Arresta, oggetto WordArt. |
| TextTriangle | 138 | Triangolo, oggetto WordArt. |
| TextTriangleInverted | 139 | Triangolo invertito, oggetto WordArt. |
| TextChevron | 140 | Chevron, oggetto WordArt. |
| TextChevronInverted | 141 | Chevron invertito, oggetto WordArt. |
| TextRingInside | 142 | Anello interno, oggetto WordArt. |
| TextRingOutside | 143 | Anello esterno, oggetto WordArt. |
| TextArchUpCurve | 144 | Arco verso l'alto, oggetto WordArt. |
| TextArchDownCurve | 145 | Arco verso il basso, oggetto WordArt. |
| TextCircleCurve | 146 | Curva circolare, oggetto WordArt. |
| TextButtonCurve | 147 | Curva a pulsante, oggetto WordArt. |
| TextArchUpPour | 148 | Versamento verso l'alto, oggetto WordArt. |
| TextArchDownPour | 149 | Versamento verso il basso, oggetto WordArt. |
| TextCirclePour | 150 | Versamento circolare, oggetto WordArt. |
| TextButtonPour | 151 | Versamento pulsante, oggetto WordArt. |
| TextCurveUp | 152 | Curva verso l'alto, oggetto WordArt. |
| TextCurveDown | 153 | Curva verso il basso, oggetto WordArt. |
| TextCascadeUp | 154 | Cascata verso l'alto, oggetto WordArt. |
| TextCascadeDown | 155 | Cascata verso il basso, oggetto WordArt. |
| TextWave1 | 156 | Onda 1, oggetto WordArt. |
| TextWave2 | 157 | Onda 2, oggetto WordArt. |
| TextWave3 | 158 | Onda 3, oggetto WordArt. |
| TextWave4 | 159 | Onda 4, oggetto WordArt. |
| TextInflate | 160 | Gonfia, oggetto WordArt. |
| TextDeflate | 161 | Sgonfia, oggetto WordArt. |
| TextInflateBottom | 162 | Gonfia dal basso, oggetto WordArt. |
| TextDeflateBottom | 163 | Sgonfia in basso, oggetto WordArt. |
| TextInflateTop | 164 | Gonfia in alto, oggetto WordArt. |
| TextDeflateTop | 165 | Sgonfia in alto, oggetto WordArt. |
| TextDeflateInflate | 166 | Sgonfia gonfia, oggetto WordArt. |
| TextDeflateInflateDeflate | 167 | Sgonfia gonfia sgonfia, oggetto WordArt. |
| TextFadeRight | 168 | Dissolvi a destra, oggetto WordArt. |
| TextFadeLeft | 169 | Dissolvi a sinistra, oggetto WordArt. |
| TextFadeUp | 170 | Dissolvi verso l'alto, oggetto WordArt. |
| TextFadeDown | 171 | Dissolvi verso il basso, oggetto WordArt. |
| TextSlantUp | 172 | Inclina verso l'alto, oggetto WordArt. |
| TextSlantDown | 173 | Inclina verso il basso, oggetto WordArt. |
| TextCanUp | 174 | Can su, oggetto WordArt. |
| TextCanDown | 175 | Can giù, oggetto WordArt. |
| FlowChartAlternateProcess | 176 | Processo alternativo del diagramma di flusso. |
| FlowChartOffpageConnector | 177 | Connettore fuori pagina del diagramma di flusso. |
| Callout90 | 178 | Callout 90. |
| AccentCallout90 | 179 | Accent callout 90. |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) callout 90. |
| AccentBorderCallout90 | 181 | Accent border callout 90. |
| LeftRightUpArrow | 182 | Freccia sinistra destra su. |
| Sun | 183 | Sole. |
| Moon | 184 | Luna. |
| BracketPair | 185 | Coppia di parentesi. |
| BracePair | 186 | Coppia di parentesi graffe. |
| Seal4 | 187 | Stella a quattro punte. |
| DoubleWave | 188 | Doppia onda. |
| ActionButtonBlank | 189 | Pulsante azione vuoto. |
| ActionButtonHome | 190 | Pulsante azione home. |
| ActionButtonHelp | 191 | Pulsante azione aiuto. |
| ActionButtonInformation | 192 | Pulsante azione informazioni. |
| ActionButtonForwardNext | 193 | Pulsante azione avanti successivo. |
| ActionButtonBackPrevious | 194 | Pulsante azione indietro precedente. |
| ActionButtonEnd | 195 | Pulsante azione fine. |
| ActionButtonBeginning | 196 | Pulsante azione inizio. |
| ActionButtonReturn | 197 | Pulsante azione ritorno. |
| ActionButtonDocument | 198 | Pulsante azione documento. |
| ActionButtonSound | 199 | Pulsante azione suono. |
| ActionButtonMovie | 200 | Pulsante azione video. |
| SingleCornerSnipped | 203 | Ritaglia oggetto rettangolo a singolo angolo. |
| TopCornersSnipped | 204 | Taglia il rettangolo con angolo sullo stesso lato. |
| DiagonalCornersSnipped | 205 | Taglia il rettangolo con angolo diagonale. |
| TopCornersOneRoundedOneSnipped | 206 | Taglia e arrotonda il rettangolo con un singolo angolo. |
| SingleCornerRounded | 207 | Arrotonda il rettangolo con un singolo angolo. |
| TopCornersRounded | 208 | Arrotonda il rettangolo con angolo sullo stesso lato. |
| DiagonalCornersRounded | 209 | Arrotonda il rettangolo con angolo diagonale. |
| Heptagon | 210 | Ettagono. |
| Cloud | 211 | Nuvola. |
| Seal6 | 212 | Stella a sei punte. |
| Seal7 | 213 | Stella a sette punte. |
| Seal10 | 214 | Stella a dieci punte. |
| Seal12 | 215 | Stella a dodici punte. |
| SwooshArrow | 216 | Freccia swoosh. |
| Goccia | 217 | Goccia. |
| TabQuadrati | 218 | Tab quadrati. |
| TabPlacca | 219 | Tab placca. |
| Torta | 220 | Torta. |
| TortaSpicchio | 221 | Torta a spicchio. |
| LineaInversa | 222 | Linea inversa. |
| MathPlus | 223 | [Math](../../aspose.words.math/) più. |
| MathMinus | 224 | [Math](../../aspose.words.math/) meno. |
| MathMultiply | 225 | [Math](../../aspose.words.math/) per. |
| MathDivide | 226 | [Math](../../aspose.words.math/) diviso. |
| MathEqual | 227 | [Math](../../aspose.words.math/) uguale. |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) non uguale. |
| TrapezioNonIsoscele | 229 | Trapezio non isoscele. |
| FrecciaCircolareSinistraDestra | 230 | Freccia circolare sinistra-destra. |
| NastroSinistraDestra | 231 | Nastro sinistra-destra. |
| LeftCircularArrow | 232 | Freccia circolare sinistra. |
| Cornice | 233 | Cornice. |
| HalfFrame | 234 | Mezza cornice. |
| Imbuto | 235 | Imbuto. |
| Gear6 | 236 | Ingranaggio a sei denti. |
| Gear9 | 237 | Ingranaggio a nove denti. |
| Decagono | 238 | Decagono. |
| Dodecagono | 239 | Dodecagono. |
| DiagonalStripe | 240 | Striscia diagonale. |
| Angolo | 241 | Angolo. |
| CornerTabs | 242 | Schede d'angolo. |
| Corda | 243 | Corda. |
| ChartPlus | 244 | Chart plus. |
| ChartStar | 245 | Chart star. |
| ChartX | 246 | Chart X. |
| MinValue | n/a | Riservato per l'uso del sistema. |


## Esempi



Mostra come inserire una forma con un'immagine dal file system locale in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Il costruttore pubblico della classe "Shape" creerà una forma con il tipo di markup "ShapeMarkupLanguage.Vml".
// Se è necessario creare una forma di tipo non primitivo, come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// Utilizzare DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Mostra come Aspose.Words identifica le forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// Per identificare correttamente i tipi di forma è necessario lavorare con le forme come DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// La conformità "Strict" o "Transitional" consente di salvare la forma come DML.
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
