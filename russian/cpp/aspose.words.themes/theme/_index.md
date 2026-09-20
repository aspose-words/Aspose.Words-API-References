---
title: "Класс Aspose::Words::Themes::Theme"
linktitle: "Тема"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Themes::Theme class. Представляет документ Тема и предоставляет доступ к основным частям темы, включая MajorFonts, MinorFonts и Colors. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.themes/theme/
---
## Theme class


Представляет документ [Theme](./), и предоставляет доступ к основным частям темы, включая [MajorFonts](./get_majorfonts/), [MinorFonts](./get_minorfonts/) и [Colors](./get_colors/). Чтобы узнать больше, посетите статью документации [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Theme : public Aspose::Words::Drawing::Core::Dml::Themes::IThemeProvider,
              public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Colors](./get_colors/)() const | Позволяет указать набор цветов темы для документа. |
| [get_MajorFonts](./get_majorfonts/)() const | Позволяет указать набор основных шрифтов для разных языков. |
| [get_MinorFonts](./get_minorfonts/)() const | Позволяет указать набор вспомогательных шрифтов для разных языков. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Theme](./theme/)() |  |
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
