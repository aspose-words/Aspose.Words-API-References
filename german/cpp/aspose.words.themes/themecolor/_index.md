---
title: "Aspose::Words::Themes::ThemeColor Enum"
linktitle: "ThemeColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Themes::ThemeColor Enum. Gibt die Themenfarben für Dokumentthemen an. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.themes/themecolor/
---
## ThemeColor enum


Gibt die Themenfarben für Dokumentthemen an. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
enum class ThemeColor
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | -1 | Keine Farbe. |
| Dark1 | 0 | Dunkle Hauptfarbe 1. |
| Light1 | 1 | Helle Hauptfarbe 1. |
| Dunkel2 | 2 | Dunkle Hauptfarbe 2. |
| Hell2 | 3 | Helle Hauptfarbe 2. |
| Akzent1 | 4 | Akzentfarbe 1. |
| Akzent2 | 5 | Akzentfarbe 2. |
| Akzent3 | 6 | Akzentfarbe 3. |
| Akzent4 | 7 | Akzentfarbe 4. |
| Akzent5 | 8 | Akzentfarbe 5. |
| Akzent6 | 9 | Akzentfarbe 6. |
| Hyperlink | 10 | Hyperlink-Farbe. |
| FollowedHyperlink | 11 | Besuchte Hyperlinkfarbe. |
| Text1 | 12 | Textfarbe 1. |
| Text2 | 13 | Textfarbe 2. |
| Hintergrund1 | 14 | Hintergrundfarbe 1. |
| Background2 | 15 | Hintergrundfarbe 2. |


## Beispiele



Zeigt, wie man mit Themen-Schriftarten und -Farben arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Definiert Schriftarten, die standardmäßig für Sprachen verwendet werden.
doc->get_Theme()->get_MinorFonts()->set_Latin(u"Algerian");
doc->get_Theme()->get_MinorFonts()->set_EastAsian(u"Aharoni");
doc->get_Theme()->get_MinorFonts()->set_ComplexScript(u"Andalus");

System::SharedPtr<Aspose::Words::Font> font = doc->get_Styles()->idx_get(u"Normal")->get_Font();
std::cout << System::String::Format(u"Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font->get_ThemeColor(), font->get_Color()) << std::endl;

// Wir können Themen-Schriftart und -Farbe anstelle von Standardwerten verwenden.
font->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Minor);
font->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent2);

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::Accent2, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// Es gibt mehrere Möglichkeiten, Schriftart und Farbe zurückzusetzen.
// 1 -  Durch Festlegen von ThemeFont.None/ThemeColor.None:
font->set_ThemeFont(Aspose::Words::Themes::ThemeFont::None);
font->set_ThemeColor(Aspose::Words::Themes::ThemeColor::None);

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::None, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// 2 -  Durch Festlegen von nicht themenbezogenen Schriftart-/Farbnamen:
font->set_Name(u"Arial");
font->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Arial", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Arial", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Arial", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Arial", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Arial", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::None, font->get_ThemeColor());
ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), font->get_Color().ToArgb());
```


Zeigt, wie man einen thematisierten Stil erstellt und verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Erstelle einen Stil mit Themen-Schriftarteigenschaften.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Siehe auch

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
