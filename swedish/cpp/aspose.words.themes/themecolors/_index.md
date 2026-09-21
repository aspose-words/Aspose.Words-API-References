---
title: "Aspose::Words::Themes::ThemeColors class"
linktitle: "ThemeColors"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Themes::ThemeColors class. Representerar färgschemat för dokumenttemat som innehåller tolv färger. ThemeColors-objektet innehåller sex accentfärger, två mörka färger, två ljusa färger och en färg för varje hyperlänk och besökt hyperlänk i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Representerar färgschemat för dokumenttemat som innehåller tolv färger. [ThemeColors](./)-objektet innehåller sex accentfärger, två mörka färger, två ljusa färger och en färg för varje hyperlänk och besökt hyperlänk.

```cpp
class ThemeColors : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Anger färg Accent 1. |
| [get_Accent2](./get_accent2/)() | Anger färg Accent 2. |
| [get_Accent3](./get_accent3/)() | Anger färg Accent 3. |
| [get_Accent4](./get_accent4/)() | Anger färg Accent 4. |
| [get_Accent5](./get_accent5/)() | Anger färg Accent 5. |
| [get_Accent6](./get_accent6/)() | Anger färg Accent 6. |
| [get_Dark1](./get_dark1/)() | Anger färg Dark 1. |
| [get_Dark2](./get_dark2/)() | Anger färg Dark 2. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Anger färg för en klickad hyperlänk. |
| [get_Hyperlink](./get_hyperlink/)() | Anger färg för en hyperlänk. |
| [get_Light1](./get_light1/)() | Anger färg Light 1. |
| [get_Light2](./get_light2/)() | Anger färg Light 2. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Sättare för [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
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
