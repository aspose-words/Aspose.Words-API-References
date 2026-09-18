---
title: "Aspose::Words::Themes::ThemeFonts class"
linktitle: "ThemeFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Themes::ThemeFonts class. Stellt eine Sammlung von Schriftarten im Schriftschema dar, die es ermöglicht, verschiedene Schriftarten für verschiedene Sprachen Latin, EastAsian und ComplexScript anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.themes/themefonts/
---
## ThemeFonts class


Stellt eine Sammlung von Schriftarten im Schriftschema dar, die es ermöglicht, verschiedene Schriftarten für verschiedene Sprachen [Latin](./get_latin/), [EastAsian](./get_eastasian/) und [ComplexScript](./get_complexscript/) anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class ThemeFonts : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_ComplexScript](./get_complexscript/)() | Gibt den Schriftartnamen für ComplexScript‑Zeichen an. |
| [get_EastAsian](./get_eastasian/)() | Gibt den Schriftartnamen für EastAsian‑Zeichen an. |
| [get_Latin](./get_latin/)() | Gibt den Schriftartnamen für Latin‑Zeichen an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ComplexScript](./set_complexscript/)(const System::String\&) | Setter für [Aspose::Words::Themes::ThemeFonts::get_ComplexScript](./get_complexscript/). |
| [set_EastAsian](./set_eastasian/)(const System::String\&) | Setter für [Aspose::Words::Themes::ThemeFonts::get_EastAsian](./get_eastasian/). |
| [set_Latin](./set_latin/)(const System::String\&) | Setter für [Aspose::Words::Themes::ThemeFonts::get_Latin](./get_latin/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man benutzerdefinierte Farben und Schriftarten für Themen festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// Das \"Theme\"‑Objekt gibt uns Zugriff auf das Dokumententhema, eine Quelle für Standard‑Schriftarten und -Farben.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// Einige Formatvorlagen, wie "Heading 1" und "Subtitle", erben diese Schriftarten.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// Andere Sprachen können ebenfalls ihre eigenen Schriftarten in diesem Design haben.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// Die Eigenschaft "Colors" enthält die Farbpalette von Microsoft Word,
// die erscheint, wenn Schattierung oder Schriftfarbe geändert wird.
// Wenden Sie benutzerdefinierte Farben auf die Farbpalette an, damit wir in Microsoft Word einfachen Zugriff darauf haben
// wenn wir zum Beispiel die Schriftfarbe über "Home" -> "Font" -> "Font Color" ändern,
// oder eine Form einfügen und dann über "Shape Format" -> "Shape Styles" eine Farbe dafür festlegen.
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

// Wenden Sie benutzerdefinierte Farben auf Hyperlinks in ihren angeklickten und nicht angeklickten Zuständen an.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
