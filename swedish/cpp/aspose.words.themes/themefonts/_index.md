---
title: "Aspose::Words::Themes::ThemeFonts klass"
linktitle: "ThemeFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Themes::ThemeFonts klass. Representerar en samling av fonter i teckensnittsschemat, vilket möjliggör att ange olika fonter för olika språk Latin, EastAsian och ComplexScript. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.themes/themefonts/
---
## ThemeFonts class


Representerar en samling av fonter i teckensnittsschemat, vilket möjliggör att ange olika fonter för olika språk [Latin](./get_latin/), [EastAsian](./get_eastasian/) och [ComplexScript](./get_complexscript/). För att lära dig mer, besök dokumentationsartikeln [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class ThemeFonts : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_ComplexScript](./get_complexscript/)() | Anger fontnamn för ComplexScript-tecken. |
| [get_EastAsian](./get_eastasian/)() | Anger fontnamn för EastAsian-tecken. |
| [get_Latin](./get_latin/)() | Anger fontnamn för Latin-tecken. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ComplexScript](./set_complexscript/)(const System::String\&) | Sättare för [Aspose::Words::Themes::ThemeFonts::get_ComplexScript](./get_complexscript/). |
| [set_EastAsian](./set_eastasian/)(const System::String\&) | Sättare för [Aspose::Words::Themes::ThemeFonts::get_EastAsian](./get_eastasian/). |
| [set_Latin](./set_latin/)(const System::String\&) | Sättare för [Aspose::Words::Themes::ThemeFonts::get_Latin](./get_latin/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man ställer in anpassade färger och fonter för teman.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// Objektet "Theme" ger oss åtkomst till dokumenttemat, en källa till standardfonter och färger.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// Vissa stilar, såsom "Heading 1" och "Subtitle", kommer att ärva dessa fonter.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// Andra språk kan också ha sina egna anpassade fonter i detta tema.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// Egenskapen "Colors" innehåller färgpaletten från Microsoft Word,
// som visas när man ändrar skuggning eller fontfärg.
// Applicera anpassade färger på färgpaletten så att vi har enkel åtkomst till dem i Microsoft Word
// när vi, till exempel, ändrar teckensnittsfärgen via "Home" -> "Font" -> "Font Color",
// eller infogar en form och sedan ställer in en färg för den via "Shape Format" -> "Shape Styles".
System::SharedPtr<Aspose::Words::Themes::ThemeColors> colors = theme->get_Colors();
colors->set_Dark1(System::Drawing::Color::get_MidnightBlue());
colors->set_Light1(System::Drawing::Color::get_PaleGreen());
colors->set_Dark2(System::Drawing::Color::get_Indigo());
colors->set_Light2(System::Drawing::Color::get_Khaki());

colors->set_Accent1(System::Drawing::Color::get_OrangeRed());
colors->set_Accent2(System::Drawing::Color::get_LightSalmon());
colors->set_Accent3(System::Drawing::Color::get_Yellow());
colors->set_Accent4(System::Drawing::Color::get_Gold());
colors->set_Accent5(System::Drawing::Color::get_BlueViolet());
colors->set_Accent6(System::Drawing::Color::get_DarkViolet());

// Applicera anpassade färger på hyperlänkar i deras klickade och oklickade tillstånd.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## Se även

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
