---
title: "Aspose::Words::Themes::ThemeColors class"
linktitle: "ThemeColors"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Themes::ThemeColors class. Stellt das Farbschema des Dokument‑Themes dar, das zwölf Farben enthält. Das ThemeColors‑Objekt enthält sechs Akzentfarben, zwei dunkle Farben, zwei helle Farben und jeweils eine Farbe für einen Hyperlink und einen besuchten Hyperlink in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Stellt das Farbschema des Dokument‑Themes dar, das zwölf Farben enthält. Das [ThemeColors](./)-Objekt enthält sechs Akzentfarben, zwei dunkle Farben, zwei helle Farben und jeweils eine Farbe für einen Hyperlink und einen besuchten Hyperlink.

```cpp
class ThemeColors : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Gibt die Farbe Accent 1 an. |
| [get_Accent2](./get_accent2/)() | Gibt die Farbe Accent 2 an. |
| [get_Accent3](./get_accent3/)() | Gibt die Farbe Accent 3 an. |
| [get_Accent4](./get_accent4/)() | Gibt die Farbe Accent 4 an. |
| [get_Accent5](./get_accent5/)() | Gibt die Farbe Accent 5 an. |
| [get_Accent6](./get_accent6/)() | Gibt die Farbe Accent 6 an. |
| [get_Dark1](./get_dark1/)() | Gibt die Farbe Dark 1 an. |
| [get_Dark2](./get_dark2/)() | Gibt die Farbe Dark 2 an. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Gibt die Farbe für einen angeklickten Hyperlink an. |
| [get_Hyperlink](./get_hyperlink/)() | Gibt die Farbe für einen Hyperlink an. |
| [get_Light1](./get_light1/)() | Gibt die Farbe Light 1 an. |
| [get_Light2](./get_light2/)() | Gibt die Farbe Light 2 an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Setter für [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
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
