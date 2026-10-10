---
title: "Aspose::Words::Drawing::ShapeType enum"
linktitle: "ShapeType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeType enum. Gibt den Typ einer Form in einem Microsoft Word-Dokument in C++ an."
type: docs
weight: 38000
url: /de/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


Gibt den Typ einer Form in einem Microsoft Word-Dokument an.

```cpp
enum class ShapeType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Image | 75 | Die Form ist ein Bild. |
| Textfeld | 202 | Die Form ist ein Textfeld. Beachten Sie, dass Formen vieler anderer Typen ebenfalls Text enthalten können. Eine Form muss nicht diesen Typ haben, um Text zu enthalten. |
| Gruppe | -1 | Die Form ist eine Gruppenform. |
| OleObject | -2 | Die Form ist ein OLE-Objekt. Sie können keine Formen dieses Typs im Dokument erstellen. |
| OleControl | 201 | Die Form ist ein ActiveX-Steuerelement. Sie können keine Formen dieses Typs im Dokument erstellen. |
| NonPrimitive | 0 | Eine vom Benutzer gezeichnete Form, die aus mehreren Segmenten und/oder Scheitelpunkten (Kurve, Freiform oder Kritzelei) besteht. Sie können keine Formen dieses Typs im Dokument erstellen. |
| Rechteck | 1 | Rechteck. |
| AbgerundetesRechteck | 2 | Abgerundetes Rechteck. |
| Ellipse | 3 | Ellipse. |
| Raute | 4 | Raute. |
| Dreieck | 5 | Dreieck. |
| Rechtwinkeldreieck | 6 | Rechtwinkliges Dreieck. |
| Parallelogramm | 7 | Parallelogramm. |
| Trapez | 8 | Trapez. |
| Sechseck | 9 | Sechseck. |
| Achteck | 10 | Achteck. |
| Plus | 11 | Plus. |
| Stern | 12 | Stern. |
| Pfeil | 13 | Pfeil. |
| DickerPfeil | 14 | Dicker Pfeil. |
| HeimPlatte | 15 | Heimplatte. |
| Würfel | 16 | Würfel. |
| Ballon | 17 | Ballon. |
| Siegel | 18 | Siegel. |
| Bogen | 19 | Bogen. |
| Linie | 20 | Linie. |
| Plakette | 21 | Plakette. |
| Dose | 22 | Dose. |
| Krapfen | 23 | Krapfen. |
| EinfacherText | 24 | Einfacher Text. |
| TextOctagon | 25 | Text-Achtseit. |
| TextHexagon | 26 | Text-Sechseck. |
| TextCurve | 27 | Text-Kurve. |
| TextWave | 28 | Text-Welle. |
| TextRing | 29 | Text-Ring. |
| TextOnCurve | 30 | Text auf Kurve. |
| TextOnRing | 31 | Text auf Ring. |
| StraightConnector1 | 32 | Eine gerade Verbindungsgrafik. |
| BentConnector2 | 33 | Eine gebogene Verbindungsgrafik mit zwei Segmenten. |
| BentConnector3 | 34 | Eine gebogene Verbindungsgrafik mit drei Segmenten. |
| BentConnector4 | 35 | Eine gebogene Verbindungsgrafik mit vier Segmenten. |
| BentConnector5 | 36 | Eine gebogene Verbindungsgrafik mit fünf Segmenten. |
| CurvedConnector2 | 37 | Eine gekrümmte Verbinderform mit zwei Segmenten. |
| CurvedConnector3 | 38 | Eine gekrümmte Verbinderform mit drei Segmenten. |
| CurvedConnector4 | 39 | Eine gekrümmte Verbinderform mit vier Segmenten. |
| CurvedConnector5 | 40 | Eine gekrümmte Verbinderform mit fünf Segmenten. |
| Callout1 | 41 | Eine Beschriftungsform mit einem Pfeil. |
| Callout2 | 42 | Eine Beschriftungsform mit zwei Pfeilen. |
| Callout3 | 43 | Eine Beschriftungsform mit drei Pfeilen. |
| AccentCallout1 | 44 | Eine Akzent-Beschriftungsform mit einem Pfeil. |
| AccentCallout2 | 45 | Eine Akzent-Beschriftungsform mit zwei Pfeilen. |
| AccentCallout3 | 46 | Eine Akzent-Beschriftungsform mit drei Pfeilen. |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) Beschriftung 1. |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) Beschriftung 2. |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) Beschriftung 3. |
| AccentBorderCallout1 | 50 | Akzentrahmen-Beschriftung 1. |
| AccentBorderCallout2 | 51 | Akzentrahmen-Anmerkung 2. |
| AccentBorderCallout3 | 52 | Akzentrahmen-Anmerkung 3. |
| Ribbon | 53 | Band. |
| Ribbon2 | 54 | Band 2. |
| Chevron | 55 | Chevron. |
| Pentagon | 56 | Fünfeck. |
| NoSmoking | 57 | Rauchen verboten. |
| Seal8 | 58 | Achtzackiger Stern. |
| Seal16 | 59 | Sechzehnzackiger Stern. |
| Seal32 | 60 | Zweiunddreißigzackiger Stern. |
| WedgeRectCallout | 61 | Keilrechteck-Anmerkung. |
| WedgeRRectCallout | 62 | Keil-R-Rechteck-Anmerkung. |
| WedgeEllipseCallout | 63 | Keilellipse-Anmerkung. |
| Welle | 64 | Welle. |
| Gefaltete Ecke | 65 | Gefaltete Ecke. |
| Linkspfeil | 66 | Linkspfeil. |
| Abwärtspfeil | 67 | Abwärtspfeil. |
| Aufwärtspfeil | 68 | Aufwärtspfeil. |
| LinksRechts-Pfeil | 69 | Links-rechts-Pfeil. |
| Auf-Ab-Pfeil | 70 | Auf-ab-Pfeil. |
| Unregelmäßiges Siegel 1 | 71 | Unregelmäßiges Siegel 1. |
| Unregelmäßiges Siegel 2 | 72 | Unregelmäßiges Siegel 2. |
| Blitz | 73 | Blitz. |
| Herz | 74 | Herz. |
| Vierfachpfeil | 76 | Vierfachpfeil. |
| Linkspfeil-Anmerkung | 77 | Linker Pfeil-Callout. |
| RightArrowCallout | 78 | Rechter Pfeil-Callout. |
| UpArrowCallout | 79 | Aufwärts-Pfeil-Callout. |
| DownArrowCallout | 80 | Abwärts-Pfeil-Callout. |
| LeftRightArrowCallout | 81 | Links-rechts-Pfeil-Callout. |
| UpDownArrowCallout | 82 | Auf- und abwärts-Pfeil-Callout. |
| QuadArrowCallout | 83 | Vierfach-Pfeil-Callout. |
| Fase | 84 | Fase. |
| LeftBracket | 85 | Linke Klammer. |
| RightBracket | 86 | Rechte Klammer. |
| LeftBrace | 87 | Linke geschweifte Klammer. |
| RightBrace | 88 | Rechte geschweifte Klammer. |
| LeftUpArrow | 89 | Links-oben-Pfeil. |
| BentUpArrow | 90 | Gebogener Aufwärtspfeil. |
| BentArrow | 91 | Gebogener Pfeil. |
| Seal24 | 92 | 24-zackiger Stern. |
| StripedRightArrow | 93 | Gestreifter rechter Pfeil. |
| NotchedRightArrow | 94 | Gezackter rechter Pfeil. |
| BlockArc | 95 | Blockbogen. |
| SmileyFace | 96 | Smiley-Gesicht. |
| VerticalScroll | 97 | Vertikaler Bildlauf. |
| HorizontalScroll | 98 | Horizontaler Bildlauf. |
| CircularArrow | 99 | Kreisförmiger Pfeil. |
| CustomShape | 100 | Dieser Formtyp scheint für Formen vorgesehen zu sein, die nicht Teil des Standardsatzes der Autoformen in Microsoft Word sind. Zum Beispiel, wenn Sie eine neue Autoform aus ClipArt einfügen. Sie können Formen dieses Typs nicht im Dokument erstellen. |
| UturnArrow | 101 | U-förmiger Pfeil. |
| CurvedRightArrow | 102 | Gebogener rechter Pfeil. |
| CurvedLeftArrow | 103 | Gebogener linker Pfeil. |
| CurvedUpArrow | 104 | Gebogener Aufwärtspfeil. |
| CurvedDownArrow | 105 | Gebogener Abwärtspfeil. |
| CloudCallout | 106 | Wolken-Anmerkung. |
| EllipseRibbon | 107 | Ellipse-Band. |
| EllipseRibbon2 | 108 | Ellipse-Band 2. |
| FlowChartProcess | 109 | Flussdiagramm-Prozess. |
| FlowChartDecision | 110 | Flussdiagramm-Entscheidung. |
| FlowChartInputOutput | 111 | Flussdiagramm Eingabe Ausgabe. |
| FlowChartPredefinedProcess | 112 | Flussdiagramm vordefinierter Prozess. |
| FlowChartInternalStorage | 113 | Flussdiagramm interner Speicher. |
| FlowChartDocument | 114 | Flussdiagramm-Dokument. |
| FlowChartMultidocument | 115 | Flussdiagramm-Multidokument. |
| FlowChartTerminator | 116 | Flussdiagramm-Terminator. |
| FlowChartPreparation | 117 | Flussdiagramm-Vorbereitung. |
| FlowChartManualInput | 118 | Flussdiagramm manuelle Eingabe. |
| FlowChartManualOperation | 119 | Flussdiagramm manuelle Operation. |
| FlowChartConnector | 120 | Flussdiagramm-Verbinder. |
| FlowChartPunchedCard | 121 | Flussdiagramm-Lochkarte. |
| FlowChartPunchedTape | 122 | Flussdiagramm-Lochstreifen. |
| FlowChartSummingJunction | 123 | Flussdiagramm Summenverbindung. |
| FlowChartOr | 124 | Flussdiagramm ODER. |
| FlowChartCollate | 125 | Flussdiagramm zusammenführen. |
| FlowChartSort | 126 | Flussdiagramm sortieren. |
| FlowChartExtract | 127 | Flussdiagramm extrahieren. |
| FlowChartMerge | 128 | Flussdiagramm zusammenführen. |
| FlowChartOfflineStorage | 129 | Flussdiagramm Offline-Speicherung. |
| FlowChartOnlineStorage | 130 | Flussdiagramm Online-Speicherung. |
| FlowChartMagneticTape | 131 | Flussdiagramm Magnetband. |
| FlowChartMagneticDisk | 132 | Flussdiagramm Magnetdisk. |
| FlowChartMagneticDrum | 133 | Flussdiagramm Magnettrommel. |
| FlowChartDisplay | 134 | Flussdiagramm Anzeige. |
| FlowChartDelay | 135 | Flussdiagramm Verzögerung. |
| TextPlainText | 136 | Einfacher Text, WordArt-Objekt. |
| TextStop | 137 | Stopp, WordArt-Objekt. |
| TextTriangle | 138 | Dreieck, WordArt-Objekt. |
| TextTriangleInverted | 139 | Umgekehrtes Dreieck, WordArt-Objekt. |
| TextChevron | 140 | Chevron, WordArt-Objekt. |
| TextChevronInverted | 141 | Umgekehrtes Chevron, WordArt-Objekt. |
| TextRingInside | 142 | Ring innen, WordArt-Objekt. |
| TextRingOutside | 143 | Ring außen, WordArt-Objekt. |
| TextArchUpCurve | 144 | Bogen nach oben gekrümmt, WordArt-Objekt. |
| TextArchDownCurve | 145 | Bogen nach unten gekrümmt, WordArt-Objekt. |
| TextCircleCurve | 146 | Kreis Kurve, WordArt-Objekt. |
| TextButtonCurve | 147 | Schaltfläche Kurve, WordArt-Objekt. |
| TextArchUpPour | 148 | Bogen nach oben gießen, WordArt-Objekt. |
| TextArchDownPour | 149 | Bogen nach unten gießen, WordArt-Objekt. |
| TextCirclePour | 150 | Kreis gießen, WordArt-Objekt. |
| TextButtonPour | 151 | Schaltfläche gießen, WordArt-Objekt. |
| TextCurveUp | 152 | Kurve nach oben, WordArt-Objekt. |
| TextCurveDown | 153 | Kurve nach unten, WordArt-Objekt. |
| TextCascadeUp | 154 | Kaskade nach oben, WordArt-Objekt. |
| TextCascadeDown | 155 | Kaskade nach unten, WordArt-Objekt. |
| TextWave1 | 156 | Welle 1, WordArt-Objekt. |
| TextWave2 | 157 | Welle 2, WordArt-Objekt. |
| TextWave3 | 158 | Welle 3, WordArt-Objekt. |
| TextWave4 | 159 | Welle 4, WordArt-Objekt. |
| TextInflate | 160 | Aufblasen, WordArt-Objekt. |
| TextDeflate | 161 | Zusammenziehen, WordArt-Objekt. |
| TextInflateBottom | 162 | Unten aufblasen, WordArt-Objekt. |
| TextDeflateBottom | 163 | Unten zusammenziehen, WordArt-Objekt. |
| TextInflateTop | 164 | Aufblähen oben, WordArt-Objekt. |
| TextDeflateTop | 165 | Verkleinern oben, WordArt-Objekt. |
| TextDeflateInflate | 166 | Verkleinern/Aufblähen, WordArt-Objekt. |
| TextDeflateInflateDeflate | 167 | Verkleinern Aufblähen Verkleinern, WordArt-Objekt. |
| TextFadeRight | 168 | Ausblenden rechts, WordArt-Objekt. |
| TextFadeLeft | 169 | Ausblenden links, WordArt-Objekt. |
| TextFadeUp | 170 | Ausblenden nach oben, WordArt-Objekt. |
| TextFadeDown | 171 | Ausblenden nach unten, WordArt-Objekt. |
| TextSlantUp | 172 | Schräg nach oben, WordArt-Objekt. |
| TextSlantDown | 173 | Schräg nach unten, WordArt-Objekt. |
| TextCanUp | 174 | Kanne nach oben, WordArt-Objekt. |
| TextCanDown | 175 | Kanne nach unten, WordArt-Objekt. |
| FlowChartAlternateProcess | 176 | Flussdiagramm alternativer Prozess. |
| FlowChartOffpageConnector | 177 | Flussdiagramm-Connector außerhalb der Seite. |
| Callout90 | 178 | Hinweis 90. |
| AccentCallout90 | 179 | Akzent-Hinweis 90. |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) Hinweis 90. |
| AccentBorderCallout90 | 181 | Akzent-Rahmen Hinweis 90. |
| LeftRightUpArrow | 182 | Pfeil nach links, rechts und oben. |
| Sonne | 183 | Sonne. |
| Mond | 184 | Mond. |
| BracketPair | 185 | Klammerpaar. |
| BracePair | 186 | Geschweifte Klammerpaar. |
| Seal4 | 187 | Vierzackiger Stern. |
| DoppelteWelle | 188 | Doppelte Welle. |
| ActionButtonBlank | 189 | Aktionsschaltfläche leer. |
| ActionButtonHome | 190 | Aktionsschaltfläche Start. |
| ActionButtonHelp | 191 | Aktionsschaltfläche Hilfe. |
| ActionButtonInformation | 192 | Aktionsschaltfläche Information. |
| ActionButtonForwardNext | 193 | Aktionsschaltfläche Vorwärts Weiter. |
| ActionButtonBackPrevious | 194 | Aktionsschaltfläche Zurück Vorherige. |
| ActionButtonEnd | 195 | Aktionsschaltfläche Ende. |
| ActionButtonBeginning | 196 | Aktionsschaltfläche Anfang. |
| ActionButtonReturn | 197 | Aktionsschaltfläche Rückkehr. |
| ActionButtonDocument | 198 | Aktionsschaltfläche Dokument. |
| ActionButtonSound | 199 | Aktionsschaltfläche Ton. |
| ActionButtonMovie | 200 | Aktionsschaltfläche Film. |
| SingleCornerSnipped | 203 | Einzelnes Eck Rechteckobjekt zuschneiden. |
| TopCornersSnipped | 204 | Gleiche Seite Eck Rechteck zuschneiden. |
| DiagonalCornersSnipped | 205 | Schneide das diagonale Eckrechteck. |
| TopCornersOneRoundedOneSnipped | 206 | Schneide und runde ein einzelnes Eckrechteck. |
| SingleCornerRounded | 207 | Runde ein einzelnes Eckrechteck. |
| TopCornersRounded | 208 | Runde ein Eckrechteck auf derselben Seite. |
| DiagonalCornersRounded | 209 | Runde ein diagonales Eckrechteck. |
| Heptagon | 210 | Siebeneck. |
| Cloud | 211 | Wolke. |
| Seal6 | 212 | Sechs‑zackiger Stern. |
| Seal7 | 213 | Sieben‑zackiger Stern. |
| Seal10 | 214 | Zehn‑zackiger Stern. |
| Seal12 | 215 | Zwölf‑zackiger Stern. |
| SwooshArrow | 216 | Swoosh‑Pfeil. |
| Teardrop | 217 | Tröpfchen. |
| SquareTabs | 218 | Quadratische Registerkarten. |
| PlaqueTabs | 219 | Plaketten-Registerkarten. |
| Pie | 220 | Kuchen. |
| WedgePie | 221 | Keilkuchen. |
| InverseLine | 222 | Inverse Linie. |
| MathPlus | 223 | [Math](../../aspose.words.math/) plus. |
| MathMinus | 224 | [Math](../../aspose.words.math/) minus. |
| MathMultiply | 225 | [Math](../../aspose.words.math/) multiplizieren. |
| MathDivide | 226 | [Math](../../aspose.words.math/) teilen. |
| MathEqual | 227 | [Math](../../aspose.words.math/) gleich. |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) nicht gleich. |
| NonIsoscelesTrapezoid | 229 | Nicht-gleichschenkliges Trapez. |
| LeftRightCircularArrow | 230 | Links-rechts kreisförmiger Pfeil. |
| LeftRightRibbon | 231 | Links-rechts Band. |
| LeftCircularArrow | 232 | Linker kreisförmiger Pfeil. |
| Rahmen | 233 | Rahmen. |
| HalbRahmen | 234 | Halber Rahmen. |
| Trichter | 235 | Trichter. |
| Zahnrad6 | 236 | Sechs-zahniges Zahnrad. |
| Zahnrad9 | 237 | Neun-zahniges Zahnrad. |
| Zehneck | 238 | Zehneck. |
| Zwölfeck | 239 | Zwölfeck. |
| Diagonalstreifen | 240 | Diagonaler Streifen. |
| Ecke | 241 | Ecke. |
| EckenTabs | 242 | Ecken Tabs. |
| Sehne | 243 | Sehne. |
| DiagrammPlus | 244 | Diagramm plus. |
| DiagrammStern | 245 | Diagramm Stern. |
| ChartX | 246 | Diagramm X. |
| MinValue | n/a | Für die Systemnutzung reserviert. |


## Beispiele



Zeigt, wie man eine Form mit einem Bild aus dem lokalen Dateisystem in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Der öffentliche Konstruktor der "Shape"-Klasse erstellt eine Form mit dem Markup-Typ "ShapeMarkupLanguage.Vml".
// Wenn Sie eine Form eines nicht‑primitiven Typs erstellen müssen, wie SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// verwenden Sie bitte DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Zeigt, wie Aspose.Words Formen identifiziert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// Um Formtypen korrekt zu identifizieren, müssen Sie mit Formen als DML arbeiten.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// "Strict" oder "Transitional" Konformität ermöglicht das Speichern der Form als DML.
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
