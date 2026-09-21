---
title: "Aspose::Words::Font-klass"
linktitle: "Typsnitt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font-klass. Innehåller teckensnittsattribut (teckensnittsnamn, teckensnittsstorlek, färg och så vidare) för ett objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words/font/
---
## Font class


Innehåller teckensnittsattribut (teckensnittsnamn, teckensnittsstorlek, färg osv.) för ett objekt. För att läsa mer, besök artikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) i dokumentationen.

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Återställer till standardformatering för teckensnitt. |
| [get_AllCaps](./get_allcaps/)() | Sant om teckensnittet är formaterat med enbart versaler. |
| [get_AutoColor](./get_autocolor/)() | Returnerar den aktuella beräknade färgen på texten (svart eller vit) som ska användas för 'auto color'. Om färgen inte är 'auto' returneras då [Color](./get_color/). |
| [get_Bidi](./get_bidi/)() | Anger om innehållet i detta körningssegment ska ha höger-till-vänster-egenskaper. |
| [get_Bold](./get_bold/)() | Sant om teckensnittet är formaterat som fetstil. |
| [get_BoldBi](./get_boldbi/)() | Sant om höger-till-vänster-texten är formaterad som fetstil. |
| [get_Border](./get_border/)() | Returnerar ett [Border](../border/)‑objekt som specificerar kant för teckensnittet. |
| [get_Color](./get_color/)() | Hämtar eller anger färgen på teckensnittet. |
| [get_ComplexScript](./get_complexscript/)() | Anger om innehållet i detta körningssegment ska behandlas som komplex skripttext oavsett deras Unicode-teckenvärden när formateringen för segmentet bestäms. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | Sant om teckensnittet är formaterat med dubbel genomstrykning. |
| [get_Emboss](./get_emboss/)() | Sant om teckensnittet är formaterat som präglat. |
| [get_EmphasisMark](./get_emphasismark/)() | Hämtar eller anger betoningstecknet som tillämpas på denna formatering. |
| [get_Engrave](./get_engrave/)() | Sant om teckensnittet är formaterat som gravyr. |
| [get_Fill](./get_fill/)() | Hämtar fyllningsformatering för [Font](./). |
| [get_Hidden](./get_hidden/)() | Sant om teckensnittet är formaterat som dold text. |
| [get_HighlightColor](./get_highlightcolor/)() | Hämtar eller anger markeringsfärgen (marker). |
| [get_Italic](./get_italic/)() | Sant om teckensnittet är formaterat som kursiv. |
| [get_ItalicBi](./get_italicbi/)() | Sant om höger-till-vänster-texten är formaterad som kursiv. |
| [get_Kerning](./get_kerning/)() | Hämtar eller anger teckensnittsstorleken då kerning påbörjas. |
| [get_LineSpacing](./get_linespacing/)() | Returnerar radavståndet för detta teckensnitt (i punkter). |
| [get_LocaleId](./get_localeid/)() | Hämtar eller anger lokalidentifieraren (språk) för de formaterade tecknen. |
| [get_LocaleIdBi](./get_localeidbi/)() | Hämtar eller anger lokalidentifieraren (språk) för de formaterade höger-till-vänster-tecknen. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Hämtar eller anger lokalidentifieraren (språk) för de formaterade asiatiska tecknen. |
| [get_Name](./get_name/)() | Hämtar eller anger namnet på teckensnittet. |
| [get_NameAscii](./get_nameascii/)() | Returnerar eller anger teckensnittet som används för latinsk text (tecken med teckenkoder från 0 (noll) till 127). |
| [get_NameBi](./get_namebi/)() | Returnerar eller anger namnet på teckensnittet i ett språkdokument som skrivs från höger till vänster. |
| [get_NameFarEast](./get_namefareast/)() | Returnerar eller anger ett östasiatiskt teckensnittsnamn. |
| [get_NameOther](./get_nameother/)() | Returnerar eller anger teckensnittet som används för tecken med teckenkoder från 128 till 255. |
| [get_NoProofing](./get_noproofing/)() | Sant när de formaterade tecknen inte ska rättas stavningsmässigt. |
| [get_NumberSpacing](./get_numberspacing/)() | Hämtar eller anger avståndstypen för det tal som visas. |
| [get_Outline](./get_outline/)() | Sant om teckensnittet är formaterat som kontur. |
| [get_Position](./get_position/)() | Hämtar eller anger textens position (i punkter) relativt baslinjen. Ett positivt tal höjer texten, och ett negativt tal sänker den. |
| [get_Scaling](./get_scaling/)() | Hämtar eller anger teckenbreddsökning i procent. |
| [get_Shading](./get_shading/)() | Returnerar ett [Shading](../shading/)‑objekt som hänvisar till skuggformateringen för teckensnittet. |
| [get_Shadow](./get_shadow/)() | Sant om teckensnittet är formaterat som skuggat. |
| [get_Size](./get_size/)() | Hämtar eller anger teckensnittsstorleken i punkter. |
| [get_SizeBi](./get_sizebi/)() | Hämtar eller anger teckensnittsstorleken i punkter som används i ett språkdokument som skrivs från höger till vänster. |
| [get_SmallCaps](./get_smallcaps/)() | Sant om teckensnittet är formaterat som små versaler. |
| [get_SnapToGrid](./get_snaptogrid/)() | Anger om det aktuella teckensnittet ska använda dokumentrutnätets tecken per rad‑inställningar vid layout. |
| [get_Spacing](./get_spacing/)() | Returnerar eller anger avståndet (i punkter) mellan tecken. |
| [get_StrikeThrough](./get_strikethrough/)() | Sant om teckensnittet är formaterat som genomstruken text. |
| [get_Style](./get_style/)() | Hämtar eller anger teckenstilen som tillämpas på denna formatering. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Hämtar eller anger den lokalt oberoende stilidentifieraren för teckenstilen som tillämpas på denna formatering. |
| [get_StyleName](./get_stylename/)() | Hämtar eller anger namnet på teckenstilen som tillämpas på denna formatering. |
| [get_Subscript](./get_subscript/)() | Sant om teckensnittet är formaterat som nedsänkt. |
| [get_Superscript](./get_superscript/)() | Sant om teckensnittet är formaterat som upphöjt. |
| [get_TextEffect](./get_texteffect/)() | Hämtar eller anger teckensnittets animeringseffekt. |
| [get_ThemeColor](./get_themecolor/)() | Hämtar eller anger temafärgen i det tillämpade färgschemat som är associerat med detta [Font](./)‑objekt. |
| [get_ThemeFont](./get_themefont/)() | Hämtar eller anger temateckensnittet i det tillämpade teckensnittsschemat som är associerat med detta [Font](./)‑objekt. |
| [get_ThemeFontAscii](./get_themefontascii/)() | Hämtar eller anger temafonten som används för latinsk text (tecken med teckenkoder från 0 (noll) till 127) i det tillämpade teckensnittsschemat som är associerat med detta [Font](./)‑objekt. |
| [get_ThemeFontBi](./get_themefontbi/)() | Hämtar eller anger temafonten i det tillämpade teckensnittsschemat som är associerat med detta [Font](./)‑objekt i ett dokument med språk som skrivs från höger till vänster. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Hämtar eller anger den östasiatiska temafonten i det tillämpade teckensnittsschemat som är associerat med detta [Font](./)‑objekt. |
| [get_ThemeFontOther](./get_themefontother/)() | Hämtar eller anger temafonten som används för tecken med teckenkoder från 128 till 255 i det tillämpade teckensnittsschemat som är associerat med detta [Font](./)‑objekt. |
| [get_TintAndShade](./get_tintandshade/)() | Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en färg. |
| [get_Underline](./get_underline/)() | Hämtar eller anger typen av understrykning som tillämpas på teckensnittet. |
| [get_UnderlineColor](./get_underlinecolor/)() | Hämtar eller anger färgen på understrykningen som tillämpas på teckensnittet. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Kontrollerar om en viss DrawingML‑texteffekt har tillämpats. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | Sättare för [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | Sättare för [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | Sättare för [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | Sättare för [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | Sättare för [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | Sättare för [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | Sättare för [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | Sättare för [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | Sättare för [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | Sättare för [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | Sättare för [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | Sättare för [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | Sättare för [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | Sättare för [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Sättare för [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | Sättare för [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | Sättare för [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | Sättare för [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | Sättare för [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Sättare för [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Sättare för [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Sättare för [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Sättare för [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | Sättare för [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Sättare för [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Sättare för [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Sättare för [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Sättare för [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Sättare för [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Sättare för [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Anger om det aktuella teckensnittet ska använda dokumentrutnätets tecken per rad‑inställningar vid layout. |
| [set_Spacing](./set_spacing/)(double) | Sättare för [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Sättare för [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Sättare för [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Sättare för [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Sättare för [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Sättare för [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Sättare för [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Sättare för [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Sättare för [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Sättare för [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Sättare för [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Inställare för [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Inställare för [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Inställare för [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Inställare för [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Inställare för [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Inställare för [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Anmärkningar


Du skapar inte instanser av klassen [Font](./) direkt. Du använder bara [Font](./) för att komma åt teckensnittsegenskaperna för de olika objekten såsom [Run](../run/), [Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/).

## Exempel



Visar hur man infogar en sträng omgiven av en kant i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Visar hur man formaterar en run av text med dess font‑egenskap.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


Visar hur man skapar och använder en styckestil med listformatering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en anpassad styckeformatmall.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Skapa en lista och se till att styckena som använder detta format använder denna lista.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Applicera styckeformatet på DocumentBuilders aktuella stycke och lägg sedan till lite text.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Ändra DocumentBuilders stil till en som inte har någon listformatering och skriv ett annat stycke.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
