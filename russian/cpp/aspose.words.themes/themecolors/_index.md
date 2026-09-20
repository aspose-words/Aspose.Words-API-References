---
title: "Aspose::Words::Themes::ThemeColors class"
linktitle: "ThemeColors"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Themes::ThemeColors class. Представляет схему цветов темы документа, содержащую двенадцать цветов. Объект ThemeColors содержит шесть акцентных цветов, два темных цвета, два светлых цвета и цвет для каждой гиперссылки и посещённой гиперссылки в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Представляет схему цветов темы документа, содержащую двенадцать цветов. Объект [ThemeColors](./) содержит шесть акцентных цветов, два темных цвета, два светлых цвета и цвет для каждой гиперссылки и посещённой гиперссылки.

```cpp
class ThemeColors : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Указывает цвет Accent 1. |
| [get_Accent2](./get_accent2/)() | Указывает цвет Accent 2. |
| [get_Accent3](./get_accent3/)() | Указывает цвет Accent 3. |
| [get_Accent4](./get_accent4/)() | Указывает цвет Accent 4. |
| [get_Accent5](./get_accent5/)() | Указывает цвет Accent 5. |
| [get_Accent6](./get_accent6/)() | Указывает цвет Accent 6. |
| [get_Dark1](./get_dark1/)() | Указывает цвет Dark 1. |
| [get_Dark2](./get_dark2/)() | Указывает цвет Dark 2. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Указывает цвет для щелкнутой гиперссылки. |
| [get_Hyperlink](./get_hyperlink/)() | Указывает цвет для гиперссылки. |
| [get_Light1](./get_light1/)() | Указывает цвет Light 1. |
| [get_Light2](./get_light2/)() | Указывает цвет Light 2. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как задавать пользовательские цвета и шрифты для тем.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// Объект "Theme" предоставляет доступ к теме документа, источнику шрифтов и цветов по умолчанию.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// Некоторые стили, такие как "Heading 1" и "Subtitle", наследуют эти шрифты.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// Для других языков также могут быть заданы пользовательские шрифты в этой теме.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// Свойство "Colors" содержит палитру цветов из Microsoft Word,
// которая появляется при изменении заливки или цвета шрифта.
// Примените пользовательские цвета к палитре, чтобы иметь к ним простой доступ в Microsoft Word
// когда мы, например, меняем цвет шрифта через "Home" -> "Font" -> "Font Color",
// или вставляем форму и затем задаём ей цвет через "Shape Format" -> "Shape Styles".
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

// Примените пользовательские цвета к гиперссылкам в их состояниях «нажата» и «не нажата».
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## См. также

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
