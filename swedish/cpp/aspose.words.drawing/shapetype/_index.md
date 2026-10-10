---
title: "Aspose::Words::Drawing::ShapeType enum"
linktitle: "ShapeType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeType enum. Anger typen av form i ett Microsoft Word-dokument i C++."
type: docs
weight: 38000
url: /sv/cpp/aspose.words.drawing/shapetype/
---
## ShapeType enum


Anger typen av form i ett Microsoft Word-dokument.

```cpp
enum class ShapeType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Image | 75 | Formen är en bild. |
| Textruta | 202 | Formen är en textruta. Observera att former av många andra typer också kan ha text inuti dem. En form behöver inte ha denna typ för att innehålla text. |
| Grupp | -1 | Formen är en gruppform. |
| OleObject | -2 | Formen är ett OLE-objekt. Du kan inte skapa former av denna typ i dokumentet. |
| OleControl | 201 | Formen är en ActiveX-kontroll. Du kan inte skapa former av den här typen i dokumentet. |
| NonPrimitive | 0 | En form som ritas av användaren och består av flera segment och/eller hörn (kurva, fri form eller klotter). Du kan inte skapa former av den här typen i dokumentet. |
| Rektangel | 1 | Rektangel. |
| Rundrektangel | 2 | Rund rektangel. |
| Ellips | 3 | Ellips. |
| Romb | 4 | Romb. |
| Triangel | 5 | Triangel. |
| RightTriangle | 6 | Rätvinklig triangel. |
| Parallellogram | 7 | Parallellogram. |
| Trapez | 8 | Trapez. |
| Hexagon | 9 | Hexagon. |
| Octagon | 10 | Octagon. |
| Plus | 11 | Plus. |
| Stjärna | 12 | Stjärna. |
| Pil | 13 | Pil. |
| TjockPil | 14 | Tjock pil. |
| Hemplatta | 15 | Hemplatta. |
| Kub | 16 | Kub. |
| Ballong | 17 | Ballong. |
| Sigill | 18 | Sigill. |
| Båge | 19 | Båge. |
| Linje | 20 | Linje. |
| Plack | 21 | Plack. |
| Burk | 22 | Burk. |
| Munk | 23 | Munk. |
| TextEnkel | 24 | Enkel text. |
| TextOctagon | 25 | Text oktagon. |
| TextHexagon | 26 | Text hexagon. |
| TextCurve | 27 | Text kurva. |
| TextWave | 28 | Text våg. |
| TextRing | 29 | Text ring. |
| TextOnCurve | 30 | Text på kurva. |
| TextOnRing | 31 | Text på ring. |
| StraightConnector1 | 32 | En rak anslutningsform. |
| BentConnector2 | 33 | En böjd anslutningsform med två segment. |
| BentConnector3 | 34 | En böjd anslutningsform med tre segment. |
| BentConnector4 | 35 | En böjd anslutningsform med fyra segment. |
| BentConnector5 | 36 | En böjd anslutningsform med fem segment. |
| CurvedConnector2 | 37 | En böjd anslutningsform med två segment. |
| CurvedConnector3 | 38 | En böjd anslutningsform med tre segment. |
| CurvedConnector4 | 39 | En böjd anslutningsform med fyra segment. |
| CurvedConnector5 | 40 | En böjd anslutningsform med fem segment. |
| Callout1 | 41 | En förklaringsform med en pil. |
| Callout2 | 42 | En förklaringsform med två pilar. |
| Callout3 | 43 | En förklaringsform med tre pilar. |
| AccentCallout1 | 44 | En accentförklaringsform med en pil. |
| AccentCallout2 | 45 | En accentförklaringsform med två pilar. |
| AccentCallout3 | 46 | En accentförklaringsform med tre pilar. |
| BorderCallout1 | 47 | [Border](../../aspose.words/border/) förklaringsruta 1. |
| BorderCallout2 | 48 | [Border](../../aspose.words/border/) förklaringsruta 2. |
| BorderCallout3 | 49 | [Border](../../aspose.words/border/) förklaringsruta 3. |
| AccentBorderCallout1 | 50 | Accent kantförklaringsruta 1. |
| AccentBorderCallout2 | 51 | Accentrampiltips 2. |
| AccentBorderCallout3 | 52 | Accentrampiltips 3. |
| Band | 53 | Band. |
| Ribbon2 | 54 | Band 2. |
| Chevron | 55 | Chevron. |
| Pentagon | 56 | Pentagon. |
| NoSmoking | 57 | Rökförbud. |
| Seal8 | 58 | Åttapunktsstjärna. |
| Seal16 | 59 | 16-punktsstjärna. |
| Seal32 | 60 | 32-punktsstjärna. |
| WedgeRectCallout | 61 | Kilrektangelpiltips. |
| WedgeRRectCallout | 62 | Kil R rektangelpiltips. |
| WedgeEllipseCallout | 63 | Kilellips piltips. |
| Våg | 64 | Våg. |
| FoldedCorner | 65 | Vikad hörn. |
| LeftArrow | 66 | Vänster pil. |
| DownArrow | 67 | Nedåtpil. |
| UpArrow | 68 | Uppåtpil. |
| LeftRightArrow | 69 | Vänster-högerpil. |
| UpDownArrow | 70 | Upp-nerpil. |
| IrregularSeal1 | 71 | Oregelbunden sigill 1. |
| IrregularSeal2 | 72 | Oregelbunden sigill 2. |
| LightningBolt | 73 | Blixt. |
| Heart | 74 | Hjärta. |
| QuadArrow | 76 | Fyrdirektionspil. |
| LeftArrowCallout | 77 | Vänster pil-anteckning. |
| RightArrowCallout | 78 | Höger pilpuff. |
| UpArrowCallout | 79 | Upp pilpuff. |
| DownArrowCallout | 80 | Ned pilpuff. |
| LeftRightArrowCallout | 81 | Vänster höger pilpuff. |
| UpDownArrowCallout | 82 | Upp ned pilpuff. |
| QuadArrowCallout | 83 | Fyrpilpuff. |
| Bevel | 84 | Avfasning. |
| LeftBracket | 85 | Vänster hakparentes. |
| RightBracket | 86 | Höger hakparentes. |
| LeftBrace | 87 | Vänster klammerparentes. |
| RightBrace | 88 | Höger klammerparentes. |
| LeftUpArrow | 89 | Vänster upp pil. |
| BentUpArrow | 90 | Böjd uppåtpil. |
| BentArrow | 91 | Böjd pil. |
| Seal24 | 92 | 24-punkts stjärna. |
| StripedRightArrow | 93 | Randig högerpil. |
| NotchedRightArrow | 94 | Tandad högerpil. |
| BlockArc | 95 | Blockbåge. |
| SmileyFace | 96 | Smiley-ansikte. |
| VerticalScroll | 97 | Vertikal rullning. |
| HorizontalScroll | 98 | Horisontell rullning. |
| CircularArrow | 99 | Cirkulär pil. |
| CustomShape | 100 | Denna formtyp verkar vara avsedd för former som inte är en del av den standarduppsättning av auto shapes i Microsoft Word. Till exempel, om du infogar en ny auto shape från ClipArt. Du kan inte skapa former av den här typen i dokumentet. |
| UturnArrow | 101 | U-svängpil. |
| CurvedRightArrow | 102 | Böjd högerpil. |
| CurvedLeftArrow | 103 | Kurvad vänsterpil. |
| CurvedUpArrow | 104 | Kurvad uppåtpil. |
| CurvedDownArrow | 105 | Kurvad nedåtpil. |
| CloudCallout | 106 | Molnförklaring. |
| EllipseRibbon | 107 | Ellipsband. |
| EllipseRibbon2 | 108 | Ellipsband 2. |
| FlowChartProcess | 109 | Flödesschema process. |
| FlowChartDecision | 110 | Flödesschema beslut. |
| FlowChartInputOutput | 111 | Flödesschema inmatning och utmatning. |
| FlowChartPredefinedProcess | 112 | Flödesschema fördefinierad process. |
| FlowChartInternalStorage | 113 | Flödesschema intern lagring. |
| FlowChartDocument | 114 | Flödesschema dokument. |
| FlowChartMultidocument | 115 | Flödesschema flerdokument. |
| FlowChartTerminator | 116 | Flödesschema terminator. |
| FlowChartPreparation | 117 | Flödesschema förberedelse. |
| FlowChartManualInput | 118 | Flödesschema manuell inmatning. |
| FlowChartManualOperation | 119 | Flödesschema manuell operation. |
| FlowChartConnector | 120 | Flödesschema anslutning. |
| FlowChartPunchedCard | 121 | Flödesschema hålkort. |
| FlowChartPunchedTape | 122 | Flödesschema hålband. |
| FlowChartSummingJunction | 123 | Flödesschema summeringskoppling. |
| FlowChartOr | 124 | Flödesschema eller. |
| FlowChartCollate | 125 | Flödesschema samla. |
| FlowChartSort | 126 | Flödesschema sortering. |
| FlowChartExtract | 127 | Flödesschema extrahering. |
| FlowChartMerge | 128 | Flödesschema sammanslagning. |
| FlowChartOfflineStorage | 129 | Flödesschema offline-lagring. |
| FlowChartOnlineStorage | 130 | Flödesschema online-lagring. |
| FlowChartMagneticTape | 131 | Flödesschema magnetband. |
| FlowChartMagneticDisk | 132 | Flödesschema magnetisk skiva. |
| FlowChartMagneticDrum | 133 | Flödesschema magnetisk trumma. |
| FlowChartDisplay | 134 | Flödesschema visning. |
| FlowChartDelay | 135 | Flödesschema fördröjning. |
| TextPlainText | 136 | Vanlig text, WordArt-objekt. |
| TextStop | 137 | Stopp, WordArt-objekt. |
| TextTriangle | 138 | Triangel, WordArt-objekt. |
| TextTriangleInverted | 139 | Inverterad triangel, WordArt-objekt. |
| TextChevron | 140 | Chevron, WordArt-objekt. |
| TextChevronInverted | 141 | Chevron inverterad, WordArt-objekt. |
| TextRingInside | 142 | Ring inuti, WordArt-objekt. |
| TextRingOutside | 143 | Ring utanför, WordArt-objekt. |
| TextArchUpCurve | 144 | Uppåböjd båge, WordArt-objekt. |
| TextArchDownCurve | 145 | Nedåböjd båge, WordArt-objekt. |
| TextCircleCurve | 146 | Cirkelkurva, WordArt-objekt. |
| TextButtonCurve | 147 | Knappkurva, WordArt-objekt. |
| TextArchUpPour | 148 | Uppåfyllning, WordArt-objekt. |
| TextArchDownPour | 149 | Nedåfyllning, WordArt-objekt. |
| TextCirclePour | 150 | Cirkelfyllning, WordArt-objekt. |
| TextButtonPour | 151 | Knappfyllning, WordArt-objekt. |
| TextCurveUp | 152 | Kurva upp, WordArt-objekt. |
| TextCurveDown | 153 | Kurva ner, WordArt-objekt. |
| TextCascadeUp | 154 | Kaskad upp, WordArt-objekt. |
| TextCascadeDown | 155 | Kaskad ner, WordArt-objekt. |
| TextWave1 | 156 | Våg 1, WordArt-objekt. |
| TextWave2 | 157 | Våg 2, WordArt-objekt. |
| TextWave3 | 158 | Våg 3, WordArt-objekt. |
| TextWave4 | 159 | Våg 4, WordArt-objekt. |
| TextInflate | 160 | Blåsa upp, WordArt-objekt. |
| TextDeflate | 161 | Blåsa ner, WordArt-objekt. |
| TextInflateBottom | 162 | Blåsa upp botten, WordArt-objekt. |
| TextDeflateBottom | 163 | Blåsa ner botten, WordArt-objekt. |
| TextInflateTop | 164 | Blåsa upp toppen, WordArt-objekt. |
| TextDeflateTop | 165 | Komprimera upp, WordArt-objekt. |
| TextDeflateInflate | 166 | Komprimera blåsa upp, WordArt-objekt. |
| TextDeflateInflateDeflate | 167 | Komprimera blåsa upp komprimera, WordArt-objekt. |
| TextFadeRight | 168 | Tona ut åt höger, WordArt-objekt. |
| TextFadeLeft | 169 | Tona ut åt vänster, WordArt-objekt. |
| TextFadeUp | 170 | Tona ut uppåt, WordArt-objekt. |
| TextFadeDown | 171 | Tona ut nedåt, WordArt-objekt. |
| TextSlantUp | 172 | Luta upp, WordArt-objekt. |
| TextSlantDown | 173 | Luta ner, WordArt-objekt. |
| TextCanUp | 174 | Kan upp, WordArt-objekt. |
| TextCanDown | 175 | Kan ner, WordArt-objekt. |
| FlowChartAlternateProcess | 176 | Flödesschema alternativ process. |
| FlowChartOffpageConnector | 177 | Flödesschema för anslutning utanför sidan. |
| Callout90 | 178 | Anrop 90. |
| AccentCallout90 | 179 | Accent-anrop 90. |
| BorderCallout90 | 180 | [Border](../../aspose.words/border/) anrop 90. |
| AccentBorderCallout90 | 181 | Accent kant anrop 90. |
| LeftRightUpArrow | 182 | Vänster höger uppåtpil. |
| Sol | 183 | Sol. |
| Måne | 184 | Måne. |
| BracketPair | 185 | Par hakparenteser. |
| BracePair | 186 | Par klammerparenteser. |
| Seal4 | 187 | Fyrspetsig stjärna. |
| DubbelVåg | 188 | Dubbel våg. |
| ActionButtonBlank | 189 | Åtgärdsknapp tom. |
| ActionButtonHome | 190 | Åtgärdsknapp hem. |
| ActionButtonHelp | 191 | Åtgärdsknapp hjälp. |
| ActionButtonInformation | 192 | Åtgärdsknapp information. |
| ActionButtonForwardNext | 193 | Åtgärdsknapp framåt nästa. |
| ActionButtonBackPrevious | 194 | Åtgärdsknapp tillbaka föregående. |
| ActionButtonEnd | 195 | Åtgärdsknapp slut. |
| ActionButtonBeginning | 196 | Åtgärdsknapp början. |
| ActionButtonReturn | 197 | Åtgärdsknapp återvänd. |
| ActionButtonDocument | 198 | Åtgärdsknapp dokument. |
| ActionButtonSound | 199 | Åtgärdsknapp ljud. |
| ActionButtonMovie | 200 | Åtgärdsknapp film. |
| SingleCornerSnipped | 203 | Klipp ut rektangelobjekt med ett hörn. |
| TopCornersSnipped | 204 | Klipp ut rektangel med hörn på samma sida. |
| DiagonalCornersSnipped | 205 | Klipp diagonal hörn rektangel. |
| TopCornersOneRoundedOneSnipped | 206 | Klipp och runda enkel hörn rektangel. |
| SingleCornerRounded | 207 | Runda enkel hörn rektangel. |
| TopCornersRounded | 208 | Runda samma sida hörn rektangel. |
| DiagonalCornersRounded | 209 | Runda diagonal hörn rektangel. |
| Heptagon | 210 | Heptagon. |
| Moln | 211 | Moln. |
| Seal6 | 212 | Sexuddig stjärna. |
| Seal7 | 213 | Sjuuddig stjärna. |
| Seal10 | 214 | Tiouddig stjärna. |
| Seal12 | 215 | Tolvuddig stjärna. |
| SwooshArrow | 216 | Swoosh pil. |
| Tårdropp | 217 | Tårdropp. |
| SquareTabs | 218 | Fyrkantiga flikar. |
| PlaqueTabs | 219 | Plackflikar. |
| Pie | 220 | Paj. |
| WedgePie | 221 | Kilformad paj. |
| InverseLine | 222 | Omvänd linje. |
| MathPlus | 223 | [Math](../../aspose.words.math/) plus. |
| MathMinus | 224 | [Math](../../aspose.words.math/) minus. |
| MathMultiply | 225 | [Math](../../aspose.words.math/) multiplicera. |
| MathDivide | 226 | [Math](../../aspose.words.math/) dela. |
| MathEqual | 227 | [Math](../../aspose.words.math/) lika. |
| MathNotEqual | 228 | [Math](../../aspose.words.math/) inte lika. |
| NonIsoscelesTrapezoid | 229 | Icke-isosceles trapets. |
| LeftRightCircularArrow | 230 | Vänster-höger cirkulär pil. |
| LeftRightRibbon | 231 | Vänster-höger band. |
| LeftCircularArrow | 232 | Vänster cirkulär pil. |
| Frame | 233 | Ram. |
| HalvRam | 234 | Halv ram. |
| Tratt | 235 | Tratt. |
| Kugghjul6 | 236 | Sextandat kugghjul. |
| Kugghjul9 | 237 | Nio-tandat kugghjul. |
| Tiohörn | 238 | Tiohörn. |
| Tolvhörn | 239 | Tolvhörn. |
| Diagonalrand | 240 | Diagonalrand. |
| Hörn | 241 | Hörn. |
| Hörnflikar | 242 | Hörnflikar. |
| Korda | 243 | Korda. |
| DiagramPlus | 244 | Diagram plus. |
| DiagramStjärna | 245 | Diagram stjärna. |
| ChartX | 246 | Chart X. |
| MinValue | n/a | Reserverad för systemets användning. |


## Exempel



Visar hur man infogar en form med en bild från det lokala filsystemet i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Den offentliga konstruktorn för klassen "Shape" skapar en form med markup-typen "ShapeMarkupLanguage.Vml".
// Om du behöver skapa en form av en icke-primitive typ, såsom SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, eller DiagonalCornersRounded,
// vänligen använd DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Visar hur Aspose.Words identifierar former.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Heptagon, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cloud, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

builder->InsertShape(Aspose::Words::Drawing::ShapeType::MathPlus, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 0, 0, 0, Aspose::Words::Drawing::WrapType::None);

// För att korrekt identifiera formtyper måste du arbeta med former som DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
// "Strict" eller "Transitional" efterlevnad tillåter att spara formen som DML.
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeTypes.docx", saveOptions);
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.ShapeTypes.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    std::cout << System::EnumGetName(shape->get_ShapeType()) << std::endl;
}
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
