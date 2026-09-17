---
title: "Aspose::Words::Themes::ThemeColors::get_Accent3 méthode"
linktitle: "get_Accent3"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Themes::ThemeColors::get_Accent3 méthode. Spécifie la couleur Accent 3 en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.themes/themecolors/get_accent3/
---
## ThemeColors::get_Accent3 method


Spécifie la couleur Accent 3.

```cpp
System::Drawing::Color Aspose::Words::Themes::ThemeColors::get_Accent3()
```


## Exemples



Montre comment définir des couleurs et des polices personnalisées pour les thèmes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// L'objet "Theme" nous donne accès au thème du document, une source de polices et de couleurs par défaut.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// Certaines styles, comme "Heading 1" et "Subtitle", hériteront de ces polices.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// D'autres langues peuvent également avoir leurs polices personnalisées dans ce thème.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// La propriété "Colors" contient la palette de couleurs de Microsoft Word,
// qui apparaît lors du changement d’ombrage ou de couleur de police.
// Appliquez des couleurs personnalisées à la palette de couleurs afin de les rendre facilement accessibles dans Microsoft Word
// lorsque nous, par exemple, changeons la couleur de police via "Home" -> "Font" -> "Font Color",
// ou insérons une forme, puis définissons une couleur pour celle-ci via "Shape Format" -> "Shape Styles".
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

// Appliquez des couleurs personnalisées aux hyperliens dans leurs états cliqué et non cliqué.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## Voir aussi

* Class [ThemeColors](../)
* Namespace [Aspose::Words::Themes](../../)
* Library [Aspose.Words for C++](../../../)
