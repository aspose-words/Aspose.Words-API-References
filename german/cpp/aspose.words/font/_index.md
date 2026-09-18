---
title: "Aspose::Words::Font Klasse"
linktitle: "Font"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font Klasse. Enthält Schriftattribute (Schriftname, Schriftgröße, Farbe usw.) für ein Objekt. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words/font/
---
## Font class


Enthält Schriftattribute (Schriftname, Schriftgröße, Farbe usw.) für ein Objekt. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Setzt die Schriftformatierung auf die Standardwerte zurück. |
| [get_AllCaps](./get_allcaps/)() | True, wenn die Schrift als durchgehend Großbuchstaben formatiert ist. |
| [get_AutoColor](./get_autocolor/)() | Gibt die aktuell berechnete Farbe des Textes (schwarz oder weiß) zurück, die für 'auto color' verwendet wird. Wenn die Farbe nicht 'auto' ist, wird [Color](./get_color/) zurückgegeben. |
| [get_Bidi](./get_bidi/)() | Gibt an, ob der Inhalt dieses Laufs rechts-nach-links-Eigenschaften haben soll. |
| [get_Bold](./get_bold/)() | Wahr, wenn die Schriftart fett formatiert ist. |
| [get_BoldBi](./get_boldbi/)() | True, wenn der rechts-nach-links-Text fett formatiert ist. |
| [get_Border](./get_border/)() | Gibt ein [Border](../border/) Objekt zurück, das den Rand für die Schrift festlegt. |
| [get_Color](./get_color/)() | Liest oder setzt die Farbe der Schrift. |
| [get_ComplexScript](./get_complexscript/)() | Gibt an, ob der Inhalt dieses Laufs als komplexer Skripttext behandelt werden soll, unabhängig von den Unicode‑Zeichenwerten, wenn die Formatierung dieses Laufs bestimmt wird. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | True, wenn die Schrift als doppelter Durchstrich formatiert ist. |
| [get_Emboss](./get_emboss/)() | True, wenn die Schrift als erhaben formatiert ist. |
| [get_EmphasisMark](./get_emphasismark/)() | Liest oder setzt das Betonungszeichen, das auf diese Formatierung angewendet wird. |
| [get_Engrave](./get_engrave/)() | True, wenn die Schrift als graviert formatiert ist. |
| [get_Fill](./get_fill/)() | Liest die Füllformatierung für die [Font](./). |
| [get_Hidden](./get_hidden/)() | True, wenn die Schrift als versteckter Text formatiert ist. |
| [get_HighlightColor](./get_highlightcolor/)() | Liest oder setzt die Hervorhebungs‑ (Marker‑)Farbe. |
| [get_Italic](./get_italic/)() | True, wenn die Schrift als kursiv formatiert ist. |
| [get_ItalicBi](./get_italicbi/)() | True, wenn der rechts-nach-links-Text kursiv formatiert ist. |
| [get_Kerning](./get_kerning/)() | Liest oder setzt die Schriftgröße, bei der das Kerning beginnt. |
| [get_LineSpacing](./get_linespacing/)() | Gibt den Zeilenabstand dieser Schrift zurück (in Punkten). |
| [get_LocaleId](./get_localeid/)() | Liest oder setzt die Gebietsschema‑Kennung (Sprache) der formatierten Zeichen. |
| [get_LocaleIdBi](./get_localeidbi/)() | Liest oder setzt die Gebietsschema‑Kennung (Sprache) der formatierten rechts-nach-links‑Zeichen. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Liest oder setzt die Gebietsschema‑Kennung (Sprache) der formatierten asiatischen Zeichen. |
| [get_Name](./get_name/)() | Liest oder setzt den Namen der Schrift. |
| [get_NameAscii](./get_nameascii/)() | Gibt die Schriftart zurück oder legt sie fest, die für lateinischen Text verwendet wird (Zeichen mit Zeichen­codes von 0 (null) bis 127). |
| [get_NameBi](./get_namebi/)() | Gibt den Namen der Schriftart zurück oder legt ihn fest in einem Rechts-nach-Links‑Sprachdokument. |
| [get_NameFarEast](./get_namefareast/)() | Gibt einen ostasiatischen Schriftartnamen zurück oder legt ihn fest. |
| [get_NameOther](./get_nameother/)() | Gibt die Schriftart zurück oder legt sie fest, die für Zeichen mit Zeichen­codes von 128 bis 255 verwendet wird. |
| [get_NoProofing](./get_noproofing/)() | Wahr, wenn die formatierten Zeichen nicht rechtschreibgeprüft werden sollen. |
| [get_NumberSpacing](./get_numberspacing/)() | Liest oder legt den Abstandstyp der angezeigten Ziffer fest. |
| [get_Outline](./get_outline/)() | Wahr, wenn die Schriftart als Kontur formatiert ist. |
| [get_Position](./get_position/)() | Liest oder legt die Position des Textes (in Punkten) relativ zur Grundlinie fest. Eine positive Zahl hebt den Text an, und eine negative Zahl senkt ihn. |
| [get_Scaling](./get_scaling/)() | Liest oder legt die Skalierung der Zeichenbreite in Prozent fest. |
| [get_Shading](./get_shading/)() | Gibt ein [Shading](../shading/)-Objekt zurück, das sich auf die Schattierungsformatierung der Schriftart bezieht. |
| [get_Shadow](./get_shadow/)() | Wahr, wenn die Schriftart als schattiert formatiert ist. |
| [get_Size](./get_size/)() | Liest oder legt die Schriftgröße in Punkten fest. |
| [get_SizeBi](./get_sizebi/)() | Liest oder legt die Schriftgröße in Punkten fest, die in einem Rechts-nach-Links‑Dokument verwendet wird. |
| [get_SmallCaps](./get_smallcaps/)() | Wahr, wenn die Schriftart als Kapitälchen formatiert ist. |
| [get_SnapToGrid](./get_snaptogrid/)() | Gibt an, ob die aktuelle Schriftart bei der Layout‑Erstellung die Dokumentgitter‑Einstellungen für Zeichen pro Zeile verwenden soll. |
| [get_Spacing](./get_spacing/)() | Gibt den Abstand (in Punkten) zwischen Zeichen zurück oder legt ihn fest. |
| [get_StrikeThrough](./get_strikethrough/)() | Wahr, wenn die Schriftart als durchgestrichener Text formatiert ist. |
| [get_Style](./get_style/)() | Liest oder legt den Zeichenstil fest, der auf diese Formatierung angewendet wird. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Liest oder legt den lokalinvarianten Stil‑Bezeichner des auf diese Formatierung angewendeten Zeichenstils fest. |
| [get_StyleName](./get_stylename/)() | Liest oder legt den Namen des auf diese Formatierung angewendeten Zeichenstils fest. |
| [get_Subscript](./get_subscript/)() | Wahr, wenn die Schriftart als Tiefstellung formatiert ist. |
| [get_Superscript](./get_superscript/)() | Wahr, wenn die Schriftart als Hochstellung formatiert ist. |
| [get_TextEffect](./get_texteffect/)() | Liest oder legt den Schriftanimationseffekt fest. |
| [get_ThemeColor](./get_themecolor/)() | Liest oder legt die Themenfarbe im angewendeten Farbschema fest, die mit diesem [Font](./)-Objekt verknüpft ist. |
| [get_ThemeFont](./get_themefont/)() | Liest oder legt die Themen‑Schriftart im angewendeten Schriftschema fest, die mit diesem [Font](./)-Objekt verknüpft ist. |
| [get_ThemeFontAscii](./get_themefontascii/)() | Ruft ab oder legt fest die Themen‑Schriftart, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) im angewendeten Schriftschema verwendet wird, das diesem [Font](./)-Objekt zugeordnet ist. |
| [get_ThemeFontBi](./get_themefontbi/)() | Ruft ab oder legt fest die Themen‑Schriftart im angewendeten Schriftschema, das diesem [Font](./)-Objekt in einem Rechts‑nach‑Links‑Sprachdokument zugeordnet ist. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Ruft ab oder legt fest die ostasiatische Themen‑Schriftart im angewendeten Schriftschema, das diesem [Font](./)-Objekt zugeordnet ist. |
| [get_ThemeFontOther](./get_themefontother/)() | Ruft ab oder legt fest die Themen‑Schriftart, die für Zeichen mit Zeichen­codes von 128 bis 255 im angewendeten Schriftschema verwendet wird, das diesem [Font](./)-Objekt zugeordnet ist. |
| [get_TintAndShade](./get_tintandshade/)() | Liest oder setzt einen Double-Wert, der eine Farbe aufhellt oder abdunkelt. |
| [get_Underline](./get_underline/)() | Ruft ab oder legt fest den Typ der Unterstreichung, die auf die Schriftart angewendet wird. |
| [get_UnderlineColor](./get_underlinecolor/)() | Ruft ab oder legt fest die Farbe der Unterstreichung, die auf die Schriftart angewendet wird. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Prüft, ob ein bestimmter DrawingML‑Texteffekt angewendet wird. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | Setter für [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | Setter für [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | Setter für [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | Setter für [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | Setter für [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | Setter für [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | Setter für [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | Setter für [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | Setter für [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | Setter für [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | Setter für [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | Setter für [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | Setter für [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | Setter für [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Setter für [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | Setter für [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | Setter für [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | Setter für [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | Setter für [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | Setter für [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Setter für [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Setter für [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Setter für [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Setter für [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | Setter für [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Setter für [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Setter für [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Setter für [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Setter für [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Setter für [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Setter für [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Gibt an, ob die aktuelle Schriftart bei der Layout‑Erstellung die Dokumentgitter‑Einstellungen für Zeichen pro Zeile verwenden soll. |
| [set_Spacing](./set_spacing/)(double) | Setter für [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Setter für [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter für [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Setter für [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Setter für [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Setter für [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Setter für [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Setter für [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Setter für [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Setter für [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Setter für [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Setter für [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Setter für [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Setter für [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Setter für [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Setter für [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Setter für [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Hinweise


Sie erstellen keine Instanzen der Klasse [Font](./) direkt. Sie verwenden einfach [Font](./), um auf die Schriftarteigenschaften der verschiedenen Objekte wie [Run](../run/), [Paragraph](../paragraph/), [Style](../style/) und [DocumentBuilder](../documentbuilder/) zuzugreifen.

## Beispiele



Zeigt, wie man eine von einem Rahmen umgebene Zeichenkette in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Zeigt, wie man einen Text‑Run mit seiner Schriftarteigenschaft formatiert.
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


Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle einen benutzerdefinierten Absatzstil.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Erstelle eine Liste und stelle sicher, dass die Absätze, die diesen Stil verwenden, diese Liste verwenden.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Wende den Absatzstil auf den aktuellen Absatz des DocumentBuilder an und füge dann etwas Text hinzu.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Ändere den Stil des DocumentBuilder zu einem, das keine Listformatierung hat, und schreibe einen weiteren Absatz.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
