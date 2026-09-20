---
title: "Aspose::Words::Themes::ThemeFonts::get_Latin метод"
linktitle: "get_Latin"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Themes::ThemeFonts::get_Latin метод. Указывает имя шрифта для латинских символов в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.themes/themefonts/get_latin/
---
## ThemeFonts::get_Latin method


Указывает имя шрифта для символов Latin.

```cpp
System::String Aspose::Words::Themes::ThemeFonts::get_Latin()
```


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

* Class [ThemeFonts](../)
* Namespace [Aspose::Words::Themes](../../)
* Library [Aspose.Words for C++](../../../)
