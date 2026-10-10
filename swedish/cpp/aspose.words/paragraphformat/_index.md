---
title: "Aspose::Words::ParagraphFormat klass"
linktitle: "ParagraphFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat klass. Representerar all formatering för ett stycke. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 49000
url: /sv/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Representerar all formatering för ett stycke. För att lära dig mer, besök dokumentationsartikeln [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Återställer till standardformatering för stycket. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Hämtar eller anger en flagga som indikerar om teckenavstånd automatiskt justeras mellan regioner med latinsk text och regioner med östasiatisk text i det aktuella stycket. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Hämtar eller anger en flagga som indikerar om teckenavstånd automatiskt justeras mellan regioner med siffror och regioner med östasiatisk text i det aktuella stycket. |
| [get_Alignment](./get_alignment/)() | Hämtar eller anger textjustering för stycket. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Hämtar eller anger teckensnittets vertikala position på en rad. |
| [get_Bidi](./get_bidi/)() | Hämtar eller anger om detta är ett stycke med höger-till-vänster-riktning. |
| [get_Borders](./get_borders/)() | Hämtar samling av styckets kanter. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | Hämtar eller anger värdet (i tecken) för första raden eller hängande indrag. Använd positiva värden för att ange första radens indrag och negativa värden för att ange hängande indrag. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Hämtar eller anger vänsterindragets värde (i tecken) för de angivna styckena. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Hämtar eller anger högra indragets värde (i tecken) för de angivna styckena. |
| [get_DropCapPosition](./get_dropcapposition/)() | Hämtar eller anger positionen för en initialbokstavstext. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Hämtar eller anger en flagga som indikerar om östasiatiska radbrytningsregler tillämpas på det aktuella stycket. |
| [get_FirstLineIndent](./get_firstlineindent/)() | Hämtar eller anger värdet (i punkter) för första raden eller hängande indrag. Använd positiva värden för att ange första radens indrag och negativa värden för att ange hängande indrag. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Hämtar eller anger en flagga som indikerar om hängande interpunktion är aktiverad för det aktuella stycket. |
| [get_IsHeading](./get_isheading/)() | Sant när styckeformatet är ett av de inbyggda rubrikformaten. |
| [get_IsListItem](./get_islistitem/)() | Sant när stycket är ett objekt i en punktlista eller numrerad lista. |
| [get_KeepTogether](./get_keeptogether/)() | Sant om alla rader i stycket ska förbli på samma sida. |
| [get_KeepWithNext](./get_keepwithnext/)() | Sant om stycket ska förbli på samma sida som stycket som följer efter det. |
| [get_LeftIndent](./get_leftindent/)() | Hämtar eller anger värdet (i punkter) som representerar vänsterindrag för stycket. |
| [get_LineSpacing](./get_linespacing/)() | Hämtar eller anger radavståndet (i punkter) för stycket. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Hämtar eller anger radavståndet för stycket. |
| [get_LinesToDrop](./get_linestodrop/)() | Hämtar eller anger antalet rader i styckets text som används för att beräkna höjden på initialbokstaven. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Hämtar eller anger mängden avstånd (i rutnätslinjer) efter styckena. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Hämtar eller anger mängden avstånd (i rutnätslinjer) före styckena. |
| [get_MirrorIndents](./get_mirrorindents/)() | Hämtar eller anger en flagga som indikerar om vänster- och högra indragen har samma bredd. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | När **true**, [SpaceBefore](./get_spacebefore/) och [SpaceAfter](./get_spaceafter/) kommer att ignoreras mellan stycken med samma format. |
| [get_OutlineLevel](./get_outlinelevel/)() | Anger konturnivån för stycket i dokumentet. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | Sant om en sidbrytning tvingas före stycket. |
| [get_RightIndent](./get_rightindent/)() | Hämtar eller anger värdet (i punkter) som representerar högra indraget för stycket. |
| [get_Shading](./get_shading/)() | Returnerar ett [Shading](../shading/) objekt som hänvisar till skuggningsformateringen för stycket. |
| [get_SnapToGrid](./get_snaptogrid/)() | Anger om det aktuella stycket ska använda dokumentets rutnätslinjer per sida-inställningar vid layout av innehållet i stycket. |
| [get_SpaceAfter](./get_spaceafter/)() | Hämtar eller anger mängden avstånd (i punkter) efter stycket. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | Sant om mängden avstånd efter stycket sätts automatiskt. |
| [get_SpaceBefore](./get_spacebefore/)() | Hämtar eller anger mängden avstånd (i punkter) före stycket. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | Sant om mängden avstånd före stycket sätts automatiskt. |
| [get_Style](./get_style/)() | Hämtar eller anger styckeformatet som tillämpas på denna formatering. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Hämtar eller anger den lokalt oberoende stilidentifieraren för styckeformatet som tillämpas på denna formatering. |
| [get_StyleName](./get_stylename/)() | Hämtar eller anger namnet på styckeformatet som tillämpas på denna formatering. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Anger om det aktuella stycket ska undantas från eventuell avstavning som tillämpas i dokumentinställningarna. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Anger om raderna i det aktuella stycket ska undantas från radnumrering som tillämpas i den överordnade sektionen. |
| [get_TabStops](./get_tabstops/)() | Hämtar samlingen av anpassade tabbstopp som definierats för detta objekt. |
| [get_WidowControl](./get_widowcontrol/)() | Sant om den första och sista raden i stycket ska förbli på samma sida som resten av stycket. |
| [get_WordWrap](./get_wordwrap/)() | Om den här egenskapen är **false** kan latinsk text i mitten av ett ord radbrytas i det aktuella stycket. Annars radbryts latinsk text efter hela ord. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Sättare för [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | Sättare för [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/). |
| [set_Bidi](./set_bidi/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | Sättare för [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Sättare för [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Sättare för [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Sättare för [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Sättare för [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Sättare för [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Sättare för [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Sättare för [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Sättare för [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man konstruerar ett Aspose.Words-dokument för hand.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ett tomt dokument innehåller ett avsnitt, en kropp och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och sluta med ett dokumentnod utan barn.
doc->RemoveAllChildren();

// Detta dokument har nu inga sammansatta barnnoder som vi kan lägga till innehåll i.
// Om vi vill redigera det måste vi återfylla dess nodsamling.
// Först, skapa ett nytt avsnitt och lägg sedan till det som ett barn till rot-dokumentnoden.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Ställ in några sidinställningsegenskaper för avsnittet.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Ett avsnitt behöver en kropp, som kommer att innehålla och visa allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Skapa ett stycke, ställ in några formateringsegenskaper och lägg sedan till det som ett barn till kroppen.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Slutligen, lägg till lite innehåll för att skapa dokumentet. Skapa ett run,
// ställ in dess utseende och innehåll, och lägg sedan till det som ett barn till stycket.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
