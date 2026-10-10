---
title: "Aspose::Words::PageSetup-klass"
linktitle: "PageSetup"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup-klass. Representerar sidinställningsegenskaperna för ett avsnitt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 46000
url: /sv/cpp/aspose.words/pagesetup/
---
## PageSetup class


Representerar sidinställningsegenskaperna för ett avsnitt. För att lära dig mer, besök dokumentationsartikeln [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) i dokumentationen.

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Återställer sidinställningarna till standardpappersstorlek, marginaler och orientering. |
| [get_Bidi](./get_bidi/)() | Anger att detta avsnitt innehåller tvåvägs (komplexa skript) text. |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Anger var sidramen är placerad i förhållande till korsande texter och objekt. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Anger på vilka sidor sidramen skrivs ut. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Hämtar eller anger ett värde som indikerar om den angivna sidramen mäts från sidans kant eller från den omgivande texten. |
| [get_Borders](./get_borders/)() | Hämtar en samling av sidramarna. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Anger om sidramen inkluderar eller exkluderar sidfoten. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Anger om sidramen inkluderar eller exkluderar sidhuvudet. |
| [get_BottomMargin](./get_bottommargin/)() | Returnerar eller anger avståndet (i punkter) mellan sidans nedre kant och den nedre gränsen för brödtexten. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Hämtar eller anger separator‑tecknet som visas mellan kapitelnummret och sidnumret. |
| [get_CharactersPerLine](./get_charactersperline/)() | Hämtar eller anger antalet tecken per rad i dokumentrutnätet. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | Sant om ett annat sidhuvud eller sidfot används på första sidan. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Tillhandahåller alternativ som styr numrering och placering av slutnoter i detta avsnitt. |
| [get_FirstPageTray](./get_firstpagetray/)() | Hämtar pappersfacket (behållaren) som ska användas för den första sidan i ett avsnitt. Värdet är implementation (skrivare) specifikt. |
| [get_FooterDistance](./get_footerdistance/)() | Returnerar eller anger avståndet (i punkter) mellan sidfoten och sidans nederkant. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Tillhandahåller alternativ som styr numrering och placering av fotnoter i detta avsnitt. |
| [get_Gutter](./get_gutter/)() | Hämtar eller anger mängden extra utrymme som läggs till marginalen för dokumentbindning. |
| [get_HeaderDistance](./get_headerdistance/)() | Returnerar eller anger avståndet (i punkter) mellan sidhuvudet och sidans överkant. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Hämtar eller anger rubriknivåstilen som tillämpas på kapiteltitlarna i dokumentet. |
| [get_LayoutMode](./get_layoutmode/)() | Hämtar eller anger layoutläget för detta avsnitt. |
| [get_LeftMargin](./get_leftmargin/)() | Returnerar eller anger avståndet (i punkter) mellan sidans vänstra kant och den vänstra gränsen för brödtexten. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Returnerar eller anger det numeriska steget för radnummer. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Hämtar eller anger avståndet mellan radnumrens högra kant och dokumentets vänstra kant. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Hämtar eller anger hur radnumrering sker, det vill säga om den startar om i början av en ny sida eller ett nytt avsnitt eller fortsätter kontinuerligt. |
| [get_LinesPerPage](./get_linesperpage/)() | Hämtar eller anger antalet rader per sida i dokumentrutnätet. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Hämtar eller anger startradnumret. |
| [get_Margins](./get_margins/)() | Returnerar eller anger förinställda [Margins](../margins/) för sidan. |
| [get_MultiplePages](./get_multiplepages/)() const | För dokument med flera sidor hämtas eller anges hur ett dokument skrivs ut eller renderas så att det kan bindas som en häfte. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | Sant om dokumentet har olika sidhuvuden och sidfötter för udda och jämna sidor. |
| [get_Orientation](./get_orientation/)() | Returnerar eller anger sidans orientering. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Hämtar pappersfacket (behållaren) som ska användas för alla sidor utom den första i ett avsnitt. Värdet är implementation (skrivare) specifikt. |
| [get_PageHeight](./get_pageheight/)() | Returnerar eller anger sidans höjd i punkter. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Hämtar eller anger sidnumreringsformatet. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Hämtar eller anger startsidnumret för avsnittet. |
| [get_PageWidth](./get_pagewidth/)() | Returnerar eller anger sidans bredd i punkter. |
| [get_PaperSize](./get_papersize/)() | Returnerar eller anger papperstorleken. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | Sant om sidnumrering startas om i början av avsnittet. |
| [get_RightMargin](./get_rightmargin/)() | Returnerar eller anger avståndet (i punkter) mellan sidans högra kant och kroppstextens högra gräns. |
| [get_RtlGutter](./get_rtlgutter/)() | Hämtar eller anger om Microsoft Word använder marginaler för avsnittet baserat på ett språk som skrivs från höger till vänster eller från vänster till höger. |
| [get_SectionStart](./get_sectionstart/)() | Returnerar eller anger typen av avsnittsbrytning för det angivna objektet. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Returnerar eller anger antalet sidor som ska inkluderas i varje häfte. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | Sant om slutnoter skrivs ut i slutet av nästa avsnitt som inte undertrycker slutnoter. Undertryckta slutnoter skrivs ut före slutnoterna i det avsnittet. |
| [get_TextColumns](./get_textcolumns/)() | Returnerar en samling som representerar uppsättningen av textkolumner. |
| [get_TextOrientation](./get_textorientation/)() | Tillåter att ange [TextOrientation](./get_textorientation/) för hela sidan. Standardvärdet är [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | Returnerar eller anger avståndet (i punkter) mellan sidans övre kant och kroppstextens övre gräns. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Returnerar eller anger vertikal justering av text på varje sida i ett dokument eller avsnitt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | Sättare för [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | Sättare för [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | Sättare för [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | Sättare för [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | Sättare för [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | Sättare för [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | Sättare för [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | Sättare för [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | Sättare för [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | Sättare för [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Ställer in pappersfacket (behållare) som ska användas för den första sidan i ett avsnitt. Värdet är implementationsspecifikt (skrivare). |
| [set_FooterDistance](./set_footerdistance/)(double) | Sättare för [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | Sättare för [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | Sättare för [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Sättare för [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Sättare för [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Sättare för [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Sättare för [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Sättare för [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Sättare för [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Sättare för [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Sättare för [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | Sättare för [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Sättare för [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Sättare för [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Sättare för [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Ställer in pappersfacket (behållare) som ska användas för alla sidor utom den första i ett avsnitt. Värdet är implementationsspecifikt (skrivare). |
| [set_PageHeight](./set_pageheight/)(double) | Sättare för [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Sättare för [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Sättare för [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Sättare för [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Sättare för [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Sättare för [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Sättare för [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Sättare för [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Sättare för [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Sättare för [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | Sant om slutnoter skrivs ut i slutet av nästa avsnitt som inte undertrycker slutnoter. Undertryckta slutnoter skrivs ut före slutnoterna i det avsnittet. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Sättare för [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Sättare för [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Sättare för [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## Anmärkningar


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Exempel



Visar hur man tillämpar och återställer sidinställningar för sektioner i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ändra sidinställningarnas egenskaper för byggarens aktuella sektion och lägg till text.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Om vi startar en ny sektion med en dokumentbyggare,
// kommer den att ärva byggarens aktuella sidinställningsegenskaper.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Vi kan återställa dess sidinställningsegenskaper till deras standardvärden med metoden "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
